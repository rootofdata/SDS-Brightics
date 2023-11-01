
## 데이터
- Aerial Bombing Operations of World War Two 데이터셋을 기반
- 데이터는 **날씨 관측 위치**와 **날짜별 관측된 기후 정보**로 구성

### **1. 날씨 관측 위치**
|DATA SET 1|WBAN|NAME|STATE|LAT/Latitude|LON/Longitude|ELEV|
|:-----:|:-----:|:-----:|:----:|:----:|:----:|:----:|
|Weather station location|Weather Station Number|Weather Station Name|Location|Latitude as a string/number|Longitude as a string/number|Note that an elevation of 9999 means unknown|
|관측 장소|관측 장소 코드|관측 장소 이름 (Seoul 등)|주/나라 ID|위도|경도|고도|

### **2. 날짜별 관측된 기후 정보**
|DATA SET 2|STA|Date|Max Temp|MeanTemp|Min Temp|
|:-----:|:-----:|:-----:|:----:|:----:|:----:|
|Weather|Weather Station| Self-explantory|Max temperature|Mean temperature|Min temperature |
|날씨 데이터|관측 장소 코드|날짜|최대 기온|평균 기온|최소 기온|

## 기법 소개
- 이 프로젝트에서는 이동평균(MA) 및 지수가중이동평균(EWMA) 모델을 사용하여 시계열 데이터를 분석
-   MA (이동평균): 연속된 데이터를 계산하여 이후 값을 예측하는 방법
  - 중심 이동 평균 (centered window): 가운데 시점을 중심으로 양쪽 관측치의 평균 계산
  - 후행 이동 평균 (trailing window): 이전 관측치의 합을 기간으로 나눠 평균 계산
-   EWMA (지수가중이동평균): 변동성을 고려하여 최근 변동치에 더 큰 가중치를 부여하여 계산하는 방법

## 데이터 전처리
### **1. 초기 데이터 탐색**
- 데이터를 불러온 후, 결측치를 처리하고 시각화를 통해 데이터의 특성을 관찰. 서울과 관련된 데이터를 중점적으로 분석하기 위해 해당 지역의 데이터를 추출

### **2. 통계적 검정**  

#### **2.1. 단위근 검정 (Unit root)** 
- 정상성을 확인하기 위해 단위근 검정을 실시. p-value가 0.0으로 나와 주어진 시계열 데이터가 정상성을 만족한다는 결과를 확인.

#### **2.2. 자기상관 분석 (AutoCorrelation)**  
- 자기상관 함수 (ACF)는 시계열 데이터의 상관성 여부를 판단하는데 사용  
- 부분 자기상관 함수 (PACF)는 자기 회귀 차수 (AR)를 식별하는데 활용

#### **2.3. 결측값 제거**  
  
## **모델링**  
### **1. 이동평균 모델**
- 이동평균 모델을 생성하고, MAPE와 MSE를 사용하여 모델의 성능을 평가. 이를 통해 초기 모델의 예측 성능을 확인.
- Window size가 7로 설정된 경우, 계절성 고려 및 일별 데이터를 주간 단위로 분석하기 위해 선택
  
### **2. 지수가중이동평균 모델 (EWMA)**
- EWMA 모델을 생성하고, MAPE와 MSE를 사용하여 모델의 성능을 평가. MAPE와 MSE를 비교하여 모델 간 성능을 평가.
- 동일한 window size (7) 및 custom ratio (0.5)로 MA와 비교하여 성능 평가를 수행
  
### **3. ARIMA 모델**
- ARIMA 모델을 수동으로 구성하여 평가, AR=1, 차분=1, MA=1로 설정
- AIC 값이 높아 다양한 전처리와 파라미터 튜닝이 필요함을 확인
<p align="center">
 <img src="https://github.com/rootofdata/SDS-Brightics/assets/86711374/54382adb-f775-496b-bf16-00ffe575fb78",width="300" height="250/">
</p>  

- Auto ARIMA 모델을 사용하여 자동으로 최적의 파라미터를 결정하고 예측을 수행
- ARIMA 모델보다 더 높은 AIC 값을 보였으나, 실제 예측값과 실제 값이 비교적 유사한 것을 확인
<p align="center">
 <img src="https://github.com/rootofdata/SDS-Brightics/assets/86711374/c8d4cafe-f5d9-42b2-9106-f68e8091486c",width="300" height="250/">
</p>  

### **4. Holt-Winters 모델링**
- Holt-Winters 지수 평활법을 사용하여 시계열 데이터를 모델링하고 예측. 승법적 모델과 가법적 모델 중 선택하여 모델을 생성
- AIC 값이 매우 낮아 모델이 데이터에 잘 적합됨을 확인
- Holt-Winters 모델로 예측한 결과를 실제 값과 비교하여 시각화

<p align="center">
 <img src="https://github.com/rootofdata/SDS-Brightics/assets/86711374/63c67bf9-c2ac-4546-a0fe-3dec71588470",width="400" height="400/">
</p>  

## 분석 결과

|AVG|MA|EWMA|
|:-----:|:-----:|:-----:|
|RMSE|0.72|0.39|
|MAPE|2.98|0.61|

- 이동평균 모델과 지수가중이동평균 모델의 결과를 비교. 두 모델의 성능을 MAPE와 MSE를 통해 평가하였고, 각 모델의 장단점을 고려하여 최종 모델을 선정.
- 실측값과 MA, EWMA 예측값의 시각적 비교를 통해 EWMA가 MA보다 정확한 예측을 제공함을 확인할 수 있음

|AVG|ARIMA|Auto ARIMA|Holt-Winters|
|:-----:|:-----:|:-----:|:----:|
|RMSE|1.734|0.833|0.843|
|MAPE|7.389|3.759|3.890|

- ARIMA 모델: 데이터에 적합한 파라미터를 찾지 못해 성능이 낮음.
- Auto ARIMA 모델: ARIMA보다 나은 결과를 보이지만, Holt-Winters 모델보다는 성능이 떨어짐.
- Holt-Winters 모델: AIC 값이 낮고 실제 값과 유사한 예측을 제공함으로써 가장 적합한 모델로 선택됨.
- 각 모델의 장단점을 고려하여 Holt-Winters 모델이 이 데이터에 가장 적합한 모델임을 확인하였습니다.

## **결론**
- 분석을 통해 선정된 최종 모델을 기반으로 향후 기간의 기온을 예측할 수 있음. 이를 통해 2차 세계 대전 공중 폭격 작전의 영향을 받지 않는 안정적인 시간대를 식별.
- 분석 결과를 토대로 미래 기온을 예측하고 전략을 수립할 수 있을 것으로 기대됨.

