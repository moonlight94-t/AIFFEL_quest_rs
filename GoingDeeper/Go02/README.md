# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 최한영
- 리뷰어 : 박수연


# PRT(Peer Review Template)
- [X]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
        - 중요! 해당 조건을 만족하는 부분을 캡쳐해 근거로 첨부

        ![결과](./review-images/result.png)
        ![svm 성능 향상](./review-images/svm-성능.png)

- [ ]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭을 왜 핵심적이라고 생각하는지 확인
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드의 기능, 존재 이유, 작동 원리 등을 기술했는지 확인
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        
- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 프로젝트 평가 기준에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        
- [X]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        ![회고](./review-images/회고.png)
- [X]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화/모듈화했는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부

        모델을 효율적으로 사용하기 위해 함수화하여 코드를 작성하였습니다.
        ![함수화](./review-images/함수화.png)


# 회고(참고 링크 및 코드 개선)
```
vocab 사이즈에 따라 클래스별 분류를 그래프 분포로 확인할 수 있어서 인상깊었습니다. 
vacab size를 높였을 때 기대되는 부분을 회고로 작성되어서 좋았습니다. 
tree 기반 모델들이 성능이 좋지 않았던 이유가 작성되어 있어서 이해하기 쉬웠습니다. 
svm의 성능이 높았던 이유가 잘 설명되어서 이해하기 좋았습니다. 
마지막에 가장 성능이 좋았던 svm의 성능을 더 높이기 위해 실험한 부분도 매우 인상깊었습니다. 
```
