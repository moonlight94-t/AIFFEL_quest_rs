# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 최원영
- 리뷰어 : 김영숙


# PRT(Peer Review Template)
- [X]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
        - 중요! 해당 조건을 만족하는 부분을 캡쳐해 근거로 첨부
        - PPO 훈련 후, beam과 greedy로 문장생성 비교하였습니다.
          ![image](https://github.com/user-attachments/assets/ea3a2fab-aa13-46c7-8d1d-29dbda63c090)
          ![image](https://github.com/user-attachments/assets/74c88ea9-cc91-4224-a2f8-73b12d048dd0)

    
- [X]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭을 왜 핵심적이라고 생각하는지 확인
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드의 기능, 존재 이유, 작동 원리 등을 기술했는지 확인
    - 모델 구조 출력 및 lora config에 설명하였습니다. 
         ![image](https://github.com/user-attachments/assets/6443f6c2-29b1-4ef2-ade8-7886d37f1f2f)
         ![image](https://github.com/user-attachments/assets/28df5b1a-a626-4cc5-9516-d4d1039865dd)


        
- [X]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 프로젝트 평가 기준에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
    - ko_alpaca 데이타셋으로 훈련하였습니다. 
         ![image](https://github.com/user-attachments/assets/ba2633cb-0289-4ff0-b0c1-c9f654ef929d)
    - skt/ko-got-trinity-1.2B 모델을 foundation model로 사용했스빈다.
          ![image](https://github.com/user-attachments/assets/c7fcebef-6683-44e3-bc85-f5c88766e711)

        
- [X]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
    - 중간중간 회고를 작성하였습니다. 
        - ![image](https://github.com/user-attachments/assets/b9603098-5b78-4449-9c94-ade5475b11c7)

        
- [X]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화/모듈화했는지 확인
        - 함수화하여 사용했습니다. 
        - ![image](https://github.com/user-attachments/assets/e6f93220-f5d9-4ad0-90a0-1099c8033f51)



# 회고(참고 링크 및 코드 개선)
```
# 리뷰어의 회고를 작성합니다.
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
```
