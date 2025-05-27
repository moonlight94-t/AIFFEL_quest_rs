# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 최원영
- 리뷰어 : 김영숙


# PRT(Peer Review Template)
- [X]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
    - 10M의 parameter를 갖는 pre-trained bert model을 작성하였습니다.
    
         ![image](https://github.com/user-attachments/assets/0046b449-593c-428b-9cd2-ab9154008b74)

   - 70 epoch의 훈련과 validation을 수행했습니다.
     ![image](https://github.com/user-attachments/assets/e914b5d8-3569-4813-9278-412fb513228f)

     ![image](https://github.com/user-attachments/assets/b0f4404a-f1f8-4d50-a2d5-a4e69aa13e34)

    
- [X]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭을 왜 핵심적이라고 생각하는지 확인
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드의 기능, 존재 이유, 작동 원리 등을 기술했는지 확인
    - dynamic mask를 적용했습니다
      ![image](https://github.com/user-attachments/assets/60bd5846-64b7-4b57-be6d-16edc571daae)
      ![image](https://github.com/user-attachments/assets/839cf779-26e4-4ef2-a27f-dd0ee3fcbd16)


        
- [X]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 프로젝트 평가 기준에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
    - CosineSchedule에 restart를 추가하였습니다. 
      ![image](https://github.com/user-attachments/assets/251f6092-e9aa-45a4-83b5-76d64eb6d890)

        
- [X]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - dynamic mask와 learning late shedule에 따라 loss/accuracy의 변화에 대해서 회고를 작성하였습니다. 
        - ![image](https://github.com/user-attachments/assets/eb74e4b3-964c-4503-af46-7e89b286f4d9)

        
- [X]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화/모듈화했는지 확인
        -dynamic mask를 고려하여 코드를 변경하였습니다
        - ![image](https://github.com/user-attachments/assets/9ef6a0a0-fb52-4851-817d-3bb7667c1a6c)



# 회고(참고 링크 및 코드 개선)
```
# 리뷰어의 회고를 작성합니다.
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
```
