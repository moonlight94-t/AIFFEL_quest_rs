# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 최현영
- 리뷰어 : 강희봉

# PRT(Peer Review Template)
- [x]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 전처리에 ordinal_map 사용 그리고 숫자 mapping 등 추가적으로 처리한 부분이 보임   
![image](https://github.com/user-attachments/assets/816fcc19-8b86-409e-bd5a-8aeaaef9774c)   
![image](https://github.com/user-attachments/assets/1b834b20-b226-4691-abe8-fd3b2e408290)
![image](https://github.com/user-attachments/assets/532e0f13-c33b-4ca3-9ac1-d78a9bd241ce)
    - meta data 오류로 인해 github에 새로 올라온 노트북에 학습과정 기록이 정상적으로 남아있지않아 loss출력이 보이지 않으나 모델 학습은 이루어진 것으로 보임   
![image](https://github.com/user-attachments/assets/67f88800-e6c3-41e8-a0d8-b3cf76f5aacd)
![image](https://github.com/user-attachments/assets/ebfc4948-dafc-4d48-a55d-7c004376aea0)

    - 완전하진 않지만 원문의 일부 내용이 표현된 번역문 생성 확인   
         ![image](https://github.com/user-attachments/assets/c9a47391-ae72-4b97-ae8e-30ba5254a191)   

    
- [x]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 이번 프로젝트 코드도 중요하지만 분석이 핵심이라고 보는데 전체 과정과 흐름을 한눈에 볼 수 있게 정리해 흐름을 쉽게 파악할 수 있었음.
      ![image](https://github.com/user-attachments/assets/bfed0ce1-896f-4d77-b94b-17feb2f38fb3)
        
- [x]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - Bleu score 구현   
    ![image](https://github.com/user-attachments/assets/6f5ad8d7-b109-4e5d-a951-c5da05d57dc4)   
    - 숫자 및 OOV 대체 Copy 구현   
    ![image](https://github.com/user-attachments/assets/88cf19d4-edc1-49d0-8d7b-96096da1cb83)   
    - 학습 과정에 학습률 스케쥴링, early stop, eval step 추가 구현   
    ![image](https://github.com/user-attachments/assets/b7f473da-f300-4180-95b9-ed4e03bfe61c)   
    - Luong Attention 모델    
    ![image](https://github.com/user-attachments/assets/c4869621-80e1-4ffb-ab4f-bf7dfd007046)   

- [x]  **4. 회고를 잘 작성했나요?**
    - 따로 회고란을 만들어 작성하진 않았지만 결과물에 대한 분석에서 아쉬운 부분과 필요한 부분과 시도해 볼 수 있는 부분들을 작성하여 회고를 대체하였다고 생각됨
![image](https://github.com/user-attachments/assets/d0f53bab-4c17-42db-ba1b-b570afa8fa56)
        
- [x]  **5. 코드가 간결하고 효율적인가요?**
    - 주석이나 string 많이 없이도 보기에 무리가 없게 깔끔하게 작성됨 

# 회고(참고 링크 및 코드 개선)
- 데이터를 많은 부분에서 관찰하여 다양하게 전처리한 부분과 loung 어텐션 모델을 이용한 시도등 다양한 방법을 사용하여 여러 가지를 해본 부분이 인상적입니다.
- 생각만하고 시도하지 못했던 숫자 특수토큰 후처리를 시도한 부분도 잘봤습니다. 진행 과정에서 있던 문제점 및 해결을 위한 고민들을 볼 수 있어서 좋았습니다.
- 짧은 문장에 대한 문제점을 분석을 보면서 나도 전처리에서는 짧은 문장을 처리해주긴했는데 토크나이저 처리 이후 unknown token 만 남아 있는 짧은 문장도 있지 않았을까라는 생각이 들었습니다. 다음 프로젝트나 NLP 처리할때는 해당 부분도 고려해야겠다는 생각이 들었습니다. 
