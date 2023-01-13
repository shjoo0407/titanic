# titanic 생존자 예측 문제
1. 데이터 셋 확인
2. EDA
3. 특성 공학(Feature Engineering)
4. 모델 개발 및 학습
5. 모델 예측 및 평가

### 1. 데이터 셋 확인
- 데이터가 어떻게 구성되어 있는 지 확인한다.
- null date를 확인하고 수정한다.
---
총 12개의 칼럼으로 이루어져 있으며, 학습에 사용해야 할 feature는 11개.

- PassengerId : 탑승객의 ID.
- Pclass : *등석
- Name : 이름
- Sex : 성별
- Age : 나이
- Sibsp : 자매, 배우자와 같이 승선해 있는 사람의 수
- Parch : 탑승한 부모 / 아이들의 수
- Ticket : 티켓 번호
- Fare : 여객 요금
- Cabin : 선실 번호
- Embarked : 승선한 장소

### 2. EDA
- 데이터가 어떤식으로 분포되어 있는 지 적절한 시각화를 통해서 분석한다.
---
