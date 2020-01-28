# Exchange Rate Project

환율 관련 프로젝트

### 1. DB 구축

- 한국수출입은행의 Open API를 활용하여 2010년 ~ 2019년까지의 환율 데이터 DB 구축.
- [DB Code](https://github.com/ajskdlf64/Project-Exchange-Rate/blob/master/Jupyter%20Notebook/01.%20Exchange%20Rate%20(exchange%20bank%20open%20api).ipynb)



### 2. EDA

- 탐색적 데이터 분석을 통한 데이터 특성 파악.
- [EDA Code](https://github.com/ajskdlf64/Project-Exchange-Rate/blob/master/Jupyter%20Notebook/02.%20EDA.ipynb)



### 3. Many to One Model

 - 선형회귀를 이용해 many - to - one Modeling
 - 예측 시점이 뒤로 갈수록 RMSE가 매우 높아짐.
 - [INPUT 5 DAYS -> FEATURE 1 DAYS](https://github.com/ajskdlf64/Project-Exchange-Rate/blob/master/Jupyter%20Notebook/03.%20Model%201%20%20(USD%2C%20Regression%2C%20%20Linear%20Regression%2C%20Sklearn%2C%205_1).ipynb)
 - [INPUT 10 DAYS -> FEATURE 5 DAYS](https://github.com/ajskdlf64/Project-Exchange-Rate/blob/master/Jupyter%20Notebook/04.%20Model%202%20%20(USD%2C%20Regression%2C%20%20Linear%20Regression%2C%20Sklearn%2C%2010_5).ipynb)
 - [INPUT 20 DAYS -> FEATURE 20 DAYS](https://github.com/ajskdlf64/Project-Exchange-Rate/blob/master/Jupyter%20Notebook/08.%20Model%206%20%20(USD%2C%20Regression%2C%20%20Linear%20Regression%2C%20Sklearn%2C%2020_20).ipynb)
 - [INPUT 120 DAYS -> FEATURE 120 DAYS](https://github.com/ajskdlf64/Project-Exchange-Rate/blob/master/Jupyter%20Notebook/07.%20Model%205%20%20(USD%2C%20Regression%2C%20%20Linear%20Regression%2C%20Sklearn%2C%20120_120).ipynb)



### 4. Virtual Data Model

 - 가상 데이터를 사용한 Modeling
 - ex) 2019년 10월 ~ 2019년 12월의 60개의 데이터를 이용하여 2020년 1월 1일을 맞춤.
       2019년 10월 ~ 2019년 12월의 59개의 데이터와 가상의 1월 1일 데이터를 이용해 1월 2일을 맞춤.
       2019년 10월 ~ 2019년 12월의 58개의 데이터와 가상의 1월 1일, 2일 데이터를 이용해 1월 3일을 맞춤.
       .......
       이렇게 60일까지 예측
 - 1년까지 가기에는 성능이 매우 떨어지나, 3개월(시장일 기준 60일) 정도는 흐름을 파악할 수 있음.
 - [Virtual Model](https://github.com/ajskdlf64/Project-Exchange-Rate/blob/master/Jupyter%20Notebook/19.%20Model%2017%20%20(USD%2C%20Regression%2C%20LightGBM%2C%20Sklearn%2C%2060_1_60%2C%20Virtual%2C%20Test%3D2019_2020).ipynb)



### 5. Many to Many Model

 - 과거 60개의 데이터를 이용해 1~60일을 각각 60개의 모델로 예측
 - 10일이 지난 시점부터 예측력이 현저하게 떨어짐.
 - [1 ~ 60 Model](https://github.com/ajskdlf64/Project-Exchange-Rate/blob/master/Jupyter%20Notebook/23.%20Final%20Regression%20Model%20(sklearn%20Linear%20Regression%2C%202019).ipynb)



### 6. 예정

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

   
