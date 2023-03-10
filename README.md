# Titanic 생존자 예측 문제
1. 데이터 셋 확인
2. EDA
3. 특성 공학(Feature Engineering)
4. 모델 개발 및 학습
5. 모델 예측 및 평가

### 1. 데이터 셋 확인
- 데이터가 어떻게 구성되어 있는 지 확인한다.
- null date를 확인하고 수정한다.

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
1. pclass가 높을 수록 생존률이 높았으며 62%,48%,24% 였다.
2. 여자가 남자보다 생존률이 높았다.
3. 나이가 높을 수록 pclass가 높은 경향을 보였으며 미세하게 생존률도 높았다.
4. s,c,q 세 탑승장마다 총 탑승인원, 성비, 생존률, pclass를 확인하였다.
5. sibsp 와 parch를 합쳐 탑승한 가족의 수를 구했다.
6. fare칼럼은 로그를 취해 비대칭성을 해결했다. (전처리단계)

### 3. Feature Engineering
- train 데이터에는 Age, Cabin, Embarked
- test 데이터에는 Age, Cabin에서 결측치를 발견
- str extract 정규표현식 사용해서 성을 따로 추출한다.
- 나이에 따라 initial이 다르기 때문에 Age 결측치들은 initial을 보고 평균값으로 대체.
- embarked는 S로 채움.

### 4. 모델 개발 및 학습
- train, test set 분리. 
- validation 나누기(validation size = 0.2%)
- RandomForest 모델 학습 및 검증
- NN모델 학습 및 검증

### 5. 모델 학습 결과 (kaggle 제출 기준)
- RandomForest 모델은 0.74162
- NN 모델은 0.75837



