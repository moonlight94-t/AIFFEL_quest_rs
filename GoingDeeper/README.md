# AIFFEL Going Deeper
이 저장소는 다양한 자연어처리(NLP) 및 대형언어모델(LLM) 관련 실험들을 정리한 결과물입니다.

## 실험 목록

### Go03: WEBT, Embedding 편향성 분석
word2vec embedding을 학습 후, 각 영화 장르에 대해 상업영화/예술영화 간의 편향성을 **Word Embedding Bias Test (WEBT)**를 통해 정량적으로 측정했습니다. 편향성 측정에 사용된 키워드는 각 장르의 대표 단어에 대해 KNN 기반 이웃 단어 탐색을 통해 자동 선정했습니다.

### Go05: Lexical Data Augmentation 기반 챗봇 학습 및 성능 평가
**동의어 치환**, **문장 순서 변경**, **질문-응답 구분 증강** 등의 다양한 lexical data augmentation 기법을 적용하여, 챗봇 모델의 학습 효율과 성능에 미치는 영향을 실험적으로 분석했습니다.

### Go07: Dynamic Masking Task로 변경한 BERT Pretraining
기존의 **static masking**이 아닌 **dynamic masking**을 적용하여, BERT 사전학습의 효율성과 표현 정확성에 미치는 영향을 실험적으로 평가했습니다.  
또한, 학습률 스케줄링 전략으로 **cosine restart scheduler**를 도입하여, 학습 안정성과 수렴 속도에 미치는 영향도 함께 분석했습니다.

### Go08: BERT NSMC Fine-tuning (LoRA, Sequence Bucketing 적용)
한국어 감성분석(NSMC)을 위한 BERT 파인튜닝 실험으로, 파라미터 효율화를 위한 LoRA(Low-Rank Adaptation)와 입력 길이 기반 bucketting 기법을 적용했습니다.

### Go09: 강화학습 기반 LLM Alignment 실험 (PPO vs DPO)
SFT(Supervised Fine-Tuning), RM(Reward Model), Actor 모델을 학습하고 PPO(Proximal Policy Optimization) 및 DPO(Direct Preference Optimization) 기반 강화학습 기법의 차이를 비교 실험했습니다.

---

각 실험의 상세 내용은 해당 디렉토리 ipynb 파일의 하단 분석 내용을 참고해 주세요.