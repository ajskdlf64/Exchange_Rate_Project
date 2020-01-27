# Exchange Rate Project

환율 관련 프로젝트


### 1차 시도
 - 선형회귀를 이용해 many - to - one Modeling
 - 예측 시점이 뒤로 갈수록 RMSE가 매우 높아짐.
 - [5 -> 1](https://github.com/ajskdlf64/Project-Exchange-Rate/blob/master/03.%20Model%201%20%20(USD%2C%20Regression%2C%20%20Linear%20Regression%2C%20Sklearn%2C%205_1).ipynb)
 - [10 -> 10](https://github.com/ajskdlf64/Project-Exchange-Rate/blob/master/05.%20Model%203%20%20(USD%2C%20Regression%2C%20%20Linear%20Regression%2C%20Sklearn%2C%2010_10).ipynb)
 - [20 -> 20](https://github.com/ajskdlf64/Project-Exchange-Rate/blob/master/08.%20Model%206%20%20(USD%2C%20Regression%2C%20%20Linear%20Regression%2C%20Sklearn%2C%2020_20).ipynb)
 - [120 -> 120](https://github.com/ajskdlf64/Project-Exchange-Rate/blob/master/07.%20Model%205%20%20(USD%2C%20Regression%2C%20%20Linear%20Regression%2C%20Sklearn%2C%20120_120).ipynb)

### 2차 시도
 - 가상 데이터를 사용한 Modeling
 - ex) 2019년 10월 ~ 2019년 12월의 60개의 데이터를 이용하여 2020년 1월 1일을 맞춤.
       2019년 10월 ~ 2019년 12월의 59개의 데이터와 가상의 1월 1일 데이터를 이용해 1월 2일을 맞춤.
       2019년 10월 ~ 2019년 12월의 58개의 데이터와 가상의 1월 1일, 2일 데이터를 이용해 1월 3일을 맞춤.
       .......
       이렇게 60일까지 예측
 - 1년까지 가기에는 성능이 매우 떨어지나, 3개월(시장일 기준 60일) 정도는 흐름을 파악할 수 있음.
 - [Virtual Model](https://github.com/ajskdlf64/Project-Exchange-Rate/blob/master/99%20Final%20Model%201.ipynb)

### 3차 시도
 - 과거 60개의 데이터를 이용해 1~60일을 각각 60개의 모델로 예측
 - 10일이 지난 시점부터 예측력이 현저하게 떨어짐.
 - [1 ~ 60 Model](https://github.com/ajskdlf64/Project-Exchange-Rate/blob/master/22.%20Final%20Regression%20Model%20(sklearn%20Linear%20Regression).ipynb)

### 4차 시도
 - 보다 정확한 예측을 위해 국제수지, GDP, 이자율, S&P500, NASDAQ, KOSPI200 등의 다양한 Feature를 이용한 DB 
 - [DB Structure](https://github.com/ajskdlf64/Project-Exchange-Rate/blob/master/999.%20DataBase%20Structure.ipynb)

### 예정
 - (예정) PCA 진행
 - (예정) 알고리즘 변경 : LightGBM, XGBoost
 - (예정) 하이브리드 신경망 (SVM + NN)
 - (예정) 데이콘 우승자 코드 확인
 - (예정) 오토인코더
 - (예정) Self-Attention
 - (예정) 모든 데이터를 전일 대비 등락률로
 - (예정) CNN, DNN 적용 고민...
 - (예정) 주기를 변경...일주일 10일 2일 5일...
 - (예정) 모델은 최대한 빠르고 쉽게 단층 구조...
 - (예정)