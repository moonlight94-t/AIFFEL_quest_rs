# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 최현영
- 리뷰어 : 이주연


# PRT(Peer Review Template)
- [X]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
        - 중요! 해당 조건을 만족하는 부분을 캡쳐해 근거로 첨부
    ```python
    sentence_generation('밥 먹었어?')
    sentence_generation('이제 주말이야')
    ```
    
- [X]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭을 왜 핵심적이라고 생각하는지 확인
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드의 기능, 존재 이유, 작동 원리 등을 기술했는지 확인
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
    ```python
     def transformer(vocab_size,
                    num_layers,
                    units,
                    d_model,
                    num_heads,
                    dropout,
                    name="transformer"):
      inputs = tf.keras.Input(shape=(None,), name="inputs")
      dec_inputs = tf.keras.Input(shape=(None,), name="dec_inputs")
    
      # 인코더에서 패딩을 위한 마스크
      enc_padding_mask = tf.keras.layers.Lambda(
          create_padding_mask, output_shape=(1, 1, None),
          name='enc_padding_mask')(inputs)
    
      # 디코더에서 미래의 토큰을 마스크 하기 위해서 사용합니다.
      # 내부적으로 패딩 마스크도 포함되어져 있습니다.
      look_ahead_mask = tf.keras.layers.Lambda(
          create_real_mask,
          output_shape=(1, None, None, None),
          name='look_ahead_mask')(dec_inputs)
    
      # 두 번째 어텐션 블록에서 인코더의 벡터들을 마스킹
      # 디코더에서 패딩을 위한 마스크
      dec_padding_mask = tf.keras.layers.Lambda(
          create_padding_mask, output_shape=(1, 1, None),
          name='dec_padding_mask')(inputs)
    
      # 인코더
      enc_outputs = encoder(
          vocab_size=vocab_size,
          num_layers=num_layers,
          units=units,
          d_model=d_model,
          num_heads=num_heads,
          dropout=dropout,
      )(inputs=[inputs, enc_padding_mask])
    
      # 디코더
      dec_outputs = decoder(
          vocab_size=vocab_size,
          num_layers=num_layers,
          units=units,
          d_model=d_model,
          num_heads=num_heads,
          dropout=dropout,
      )(inputs=[dec_inputs, enc_outputs, look_ahead_mask, dec_padding_mask])
    
      # 완전연결층
      final_outputs = tf.keras.layers.Lambda(lambda x: tf.linalg.diag_part(x),output_shape=(None, d_model))(dec_outputs)
      outputs = tf.keras.layers.Dense(units=vocab_size, name="outputs")(final_outputs)
    ``` 
    
        
- [X]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 프로젝트 평가 기준에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
    ```python
     col_idx = tf.range(seq_len)[tf.newaxis, :]  # (1, S)
    # mask index per context step: shape (S, 1)
    mask_step = tf.range(1, seq_len + 1)[:, tf.newaxis]  # (S, 1)
    
    # Broadcast: col_idx < step
    # 각 i에 대해 col < i 이면 0, else 1
    base_mask = tf.cast(col_idx >= mask_step, tf.float32)  # (S, S)
    masks = tf.repeat(base_mask[:, tf.newaxis, :], repeats=seq_len, axis=1)
    ``` 
    
- [X]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
    ```python
     import matplotlib.pyplot as plt
    
    # history에서 metric 추출
    acc = history.history.get('accuracy')
    loss = history.history.get('loss')
    
    
    # plot
    plt.figure(figsize=(12, 5))
    
    # Accuracy Plot
    plt.subplot(1, 2, 1)
    plt.plot(acc, label='Train Acc')
    plt.title('Accuracy')
    plt.xlabel('Epoch')
    plt.ylabel('Accuracy')
    plt.legend()
    
    # Loss Plot
    plt.subplot(1, 2, 2)
    plt.plot(loss, label='Train Loss')
    plt.title('Loss')
    plt.xlabel('Epoch')
    plt.ylabel('Loss')
    plt.legend()
    
    plt.tight_
    ``` 
        
- [X]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화/모듈화했는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
    ```python
     def transformer(vocab_size,
                    num_layers,
                    units,
                    d_model,
                    num_heads,
                    dropout,
                    name="transformer"):
      inputs = tf.keras.Input(shape=(None,), name="inputs")
      dec_inputs = tf.keras.Input(shape=(None,), name="dec_inputs")
    
      # 인코더에서 패딩을 위한 마스크
      enc_padding_mask = tf.keras.layers.Lambda(
          create_padding_mask, output_shape=(1, 1, None),
          name='enc_padding_mask')(inputs)
    
      # 디코더에서 미래의 토큰을 마스크 하기 위해서 사용합니다.
      # 내부적으로 패딩 마스크도 포함되어져 있습니다.
      look_ahead_mask = tf.keras.layers.Lambda(
          create_real_mask,
          output_shape=(1, None, None, None),
          name='look_ahead_mask')(dec_inputs)
    
      # 두 번째 어텐션 블록에서 인코더의 벡터들을 마스킹
      # 디코더에서 패딩을 위한 마스크
      dec_padding_mask = tf.keras.layers.Lambda(
          create_padding_mask, output_shape=(1, 1, None),
          name='dec_padding_mask')(inputs)
    
      # 인코더
      enc_outputs = encoder(
          vocab_size=vocab_size,
          num_layers=num_layers,
          units=units,
          d_model=d_model,
          num_heads=num_heads,
          dropout=dropout,
      )(inputs=[inputs, enc_padding_mask])
    
      # 디코더
      dec_outputs = decoder(
          vocab_size=vocab_size,
          num_layers=num_layers,
          units=units,
          d_model=d_model,
          num_heads=num_heads,
          dropout=dropout,
      )(inputs=[dec_inputs, enc_outputs, look_ahead_mask, dec_padding_mask])
    
      # 완전연결층
      final_outputs = tf.keras.layers.Lambda(lambda x: tf.linalg.diag_part(x),output_shape=(None, d_model))(dec_outputs)
      outputs = tf.keras.layers.Dense(units=vocab_size, name="outputs")(final_outputs)
    
    
      return tf.keras.Model(inputs=[inputs, dec_inputs], outputs=outputs, name=name)            
    ``` 


# 회고(참고 링크 및 코드 개선)
```
# 리뷰어의 회고를 작성합니다.
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.

#깔끔하게 정리된 코드였습니다. 전처리과정과 dropout 수치를 통해 accuracy를 높이는 부분을 볼 수 있어 좋았습니다.

```
