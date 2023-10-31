# SDS-Brightics

## Smart Factory Semiconductor Process Optimization (Personal Project)
#### **Background and Objectives**
- The objective of this project was to enhance anomaly detection performance in a smart factory setting, specifically focusing on optimizing semiconductor manufacturing processes.
- The goal was to identify and predict defective products, thereby improving overall product quality.

#### **Project Overview**
- The project aimed to leverage the advantages of smart factories and the unique characteristics of semiconductor manufacturing processes.
- Various comprehensive processes were undertaken to construct an anomaly detection model, with the ultimate aim of predicting defective products and implementing differentiated quality management strategies.

#### **Data Collection and Preprocessing**
- Data consisted of eight features, including temperature and humidity, measured through sensors.
- Preprocessing involved handling missing values and considering correlations among features.

#### **Modeling and Performance Evaluation**
- After experimenting with multiple models, the Multilayer Perceptron (MLP) demonstrated superior performance. The MLP model was fine-tuned, leading to optimal results in testing as well.

#### **Results and Conclusion**
- Visualization analysis clearly highlighted distinctions between acceptable and defective products. The implemented classification algorithms successfully detected defects in advance. There is potential to reduce the defect rate by introducing automated processes and additional inspections.

#### **Future Research Directions**
- Future research should focus on refining the imputation methods for missing values, optimizing hyperparameters, and enhancing the model by considering inter-feature dependencies. Additionally, there is potential for constructing anomaly detection processes utilizing chemical reaction data.

#### **Conclusion**
- This project achieved successful detection and prediction of defects in a smart factory environment. It is anticipated that these findings will significantly contribute to future optimization efforts in the manufacturing process.

**remark** : https://www.brightics.ai/community/knowledge-sharing/detail/7098

## Medical_Cost_Prediction
#### **Title:** Predicting Personal Medical Expenses (Insurance) Project

#### **Overview:** In this analysis project, an individual-specific medical cost prediction model is constructed and evaluated by considering factors such as age, gender, obesity, number of childbirths, residence, and smoking status.  
#### Purpose:  
- Through predicting medical expenses based on social and physical individual information, individuals can forecast their medical costs, preventing overpayment and allowing them to pay corresponding insurance premiums directly. Additionally, insurance companies can understand trends in insurance cost changes and plan customized products accordingly.
1. **Data Collection:** Follow the data collection path below (Kaggle dataset).  
2. **Data Preprocessing:**  
- Check for missing values in all columns and handle them through removal or imputation.  
- Perform Label Encoding for columns with string data types.  
- Remove rows where negative values are present in any column.  
- Identify outliers based on criteria: age: 100 years, children: 10, and remove corresponding rows.  
- Apply One-Hot Encoding for necessary columns.  
  
#### **3. Modeling:**  

- Analyze the distribution of variables with Charges and select feature columns accordingly.  
- Split the preprocessed dataset into an 80:20 ratio.  
- Train/Test the data using models such as AdaBoost, Decision Tree, Linear Regression, Penalized Linear Regression, Random Forest, XGB Regression, etc.  
- If possible, find optimal parameters using GridSearchCV.  

#### **4. Model Evaluation and Selection:**  
- Select an evaluation metric (MAE, MSE, RMSE, MAPE) to calculate scores and choose the best-performing model.  

Data Source: Utilize the 'Medical Cost Personal Datasets' from Kaggle's Open DataSet.  

## Weather Conditions
1. 데이터 배경
1.1 데이터 소개
Aerial Bombing Operations of World War Two 데이터셋을 기반으로, 2차 세계 대전 기간 중의 날씨 데이터를 분석하여 D-DAY 연기의 영향을 알아보고자 합니다. 데이터는 미국 국립해양대기청에서 수집되었습니다.

1.2 데이터 설명
데이터는 날씨 관측 위치와 날짜별 관측된 기후 정보로 구성되어 있습니다. 주요 컬럼은 다음과 같습니다:

날씨 관측 위치 (Weather station location):
WBAN: 날씨 관측소 번호
NAME: 날씨 관측소 이름
STATE/COUNTRY ID: 위치 (주/나라 ID)
LAT/LON: 위도 및 경도
ELEV: 고도
기후 정보 (Weather):
STA: 날씨 관측소 코드
Date: 날짜
Max Temp: 최대 기온
MeanTemp: 평균 기온
Min Temp: 최소 기온
2. 기법 소개
이 프로젝트에서는 이동평균(MA) 및 지수가중이동평균(EWMA) 모델을 사용하여 시계열 데이터를 분석하고자 합니다.

MA (이동평균): 연속된 데이터를 계산하여 이후 값을 예측하는 방법입니다.
EWMA (지수가중이동평균): 변동성을 고려하여 최근 변동치에 더 큰 가중치를 부여하여 계산하는 방법입니다.
이 외에도 ARIMA, WMA 등 다양한 시계열 모델이 있으며, 이를 Brightics Studio에서 적용할 수 있습니다.

3. 분석 진행
3.1 초기 데이터 탐색
데이터를 불러온 후, 결측치를 처리하고 시각화를 통해 데이터의 특성을 살펴보았습니다. 서울과 관련된 데이터를 중점적으로 분석하기 위해 해당 지역의 데이터를 추출하였습니다.

3.2 단위근 검정
정상성을 확인하기 위해 단위근 검정을 실시하였습니다. 단위근 검정을 통해 주어진 시계열 데이터가 정상성을 만족한다는 결과를 확인하였습니다.

3.3 이동평균 모델
이동평균 모델을 생성하고, MAPE와 MSE를 사용하여 모델의 성능을 평가하였습니다. 이를 통해 초기 모델의 예측 성능을 확인하였습니다.

3.4 지수가중이동평균 모델 (EWMA)
EWMA 모델을 생성하고, MAPE와 MSE를 사용하여 모델의 성능을 평가하였습니다. MAPE와 MSE를 비교하여 모델 간 성능을 평가하였습니다.

4. 결과 및 평가
4.1 분석 결과
이동평균 모델과 지수가중이동평균 모델의 결과를 비교하였습니다. 두 모델의 성능을 MAPE와 MSE를 통해 평가하였고, 각 모델의 장단점을 고려하여 최종 모델을 선정하였습니다.

4.2 결론
분석을 통해 선정된 최종 모델을 기반으로 향후 기간의 기온을 예측할 수 있습니다. 이를 통해 2차 세계 대전 공중 폭격 작전의 영향을 받지 않는 안정적인 시간대를 식별할 수 있습니다.

1. MA (이동평균)
1.1 이해와 시각화
이동평균은 특정 기간(window) 동안의 관측치 평균을 계산하는 방법입니다. 두 가지 유형이 있습니다:

중심 이동 평균 (centered window): 가운데 시점을 중심으로 양쪽 관측치의 평균 계산
후행 이동 평균 (trailing window): 이전 관측치의 합을 기간으로 나눠 평균 계산
1.2 MA의 적용
Window size가 7로 설정된 경우, 계절성 고려 및 일별 데이터를 주간 단위로 분석하기 위해 선택되었습니다.

2. EWMA (지수 가중 이동 평균)
2.1 이해
EWMA는 이전 관측치에 가중치를 부여하여 예측값을 계산하는 방법입니다.

2.2 EWMA의 적용
동일한 window size (7) 및 custom ratio (0.5)로 MA와 비교하여 성능 평가를 수행하였습니다.

3. 결과 및 비교
3.1 평가 지표
MAPE (Mean Absolute Percentage Error): 예측값과 실제값 간의 백분율 오차의 평균
RMSE (Root Mean Square Error): 예측 오차의 제곱 평균의 제곱근
3.2 성능 비교
MAPE (MA): 약 2.98
MAPE (EWMA): 약 0.61
RMSE (MA): 약 0.72
RMSE (EWMA): 약 0.39
4. 시각화 및 결론
4.1 시각화 비교
실측값과 MA, EWMA 예측값의 시각적 비교를 통해 EWMA가 MA보다 정확한 예측을 제공함을 확인할 수 있습니다.

4.2 결론
EWMA가 MA보다 더 정확한 예측을 제공하며, 주어진 데이터에 적합한 모델임을 확인하였습니다. Parameter 조정에 따라 성능은 변할 수 있으나, 현재 설정에서 EWMA가 더 우수한 결과를 나타냈습니다.

분석을 통해 얻은 결과를 토대로, 향후 기간의 기온 예측 및 이에 따른 전략 수립이 가능하게 되었습니다.

1. 자기상관 (AutoCorrelation) 분석
1.1 자기상관 함수 (ACF)
자기상관 함수 (ACF)는 시계열 데이터의 상관성 여부를 판단하는데 사용됩니다. ACF를 통해 이동 평균(MA) 항의 차수를 식별할 수 있습니다.

1.2 부분 자기상관 함수 (PACF)
부분 자기상관 함수 (PACF)는 자기 회귀 차수 (AR)를 식별하는데 활용됩니다. 정상성 조건이 만족되지 않았을 때, 차분을 통해 정상성을 만족시키고 ACF와 PACF를 분석합니다.

정상성을 만족하는 경우의 ACF와 PACF

정상성을 만족하지 않는 경우의 ACF와 PACF

2. 데이터 전처리
2.1 차분 프로세스
Add Lead Lag: 대상 컬럼의 데이터를 한 칸씩 아래로 밀어 Lag=1을 생성합니다.
Add Function Column: 대상 컬럼과 밀린 컬럼의 차이를 계산하여 '차분 컬럼(difference_1)'으로 저장합니다.
Delete Missing Data: Lag에 따른 null값을 삭제합니다.
차분에 대한 단위근 검정 결과:
p-value가 0.0으로 나와 정상성을 만족함을 확인했습니다.

3. ARIMA 및 Auto ARIMA 모델링
3.1 ARIMA 모델
ARIMA 모델을 수동으로 구성하여 평가했습니다. AR=1, 차분=1, MA=1로 설정하였습니다.

ARIMA 모델 평가 결과:
AIC 값이 높아 다양한 전처리와 파라미터 튜닝이 필요함을 확인하였습니다.

3.2 Auto ARIMA 모델
Auto ARIMA 모델을 사용하여 자동으로 최적의 파라미터를 결정하고 예측을 수행했습니다.

Auto ARIMA 모델 평가 결과:
ARIMA 모델보다 더 높은 AIC 값을 보였으나, 실제 예측값과 실제 값이 비교적 유사한 것을 확인할 수 있었습니다.

4. Holt-Winters 모델링
4.1 Holt-Winters 모델
Holt-Winters 지수 평활법을 사용하여 시계열 데이터를 모델링하고 예측했습니다. 승법적 모델과 가법적 모델 중 선택하여 모델을 생성했습니다.

Holt-Winters 모델 평가 결과:
AIC 값이 매우 낮아 모델이 데이터에 잘 적합됨을 확인하였습니다.

4.2 Holt-Winters 모델 시각화
Holt-Winters 모델로 예측한 결과를 실제 값과 비교하여 시각화하였습니다.

5. 모델 평가 지표
5.1 RMSE (Root Mean Square Error) 및 MAPE (Mean Absolute Percentage Error)
ARIMA 모델: RMSE= [값], MAPE= [값]
Auto ARIMA 모델: RMSE= [값], MAPE= [값]
Holt-Winters 모델: RMSE= [값], MAPE= [값]
6. 결론
ARIMA 모델: 데이터에 적합한 파라미터를 찾지 못해 성능이 낮음.
Auto ARIMA 모델: ARIMA보다 나은 결과를 보이지만, Holt-Winters 모델보다는 성능이 떨어짐.
Holt-Winters 모델: AIC 값이 낮고 실제 값과 유사한 예측을 제공함으로써 가장 적합한 모델로 선택됨.
각 모델의 장단점을 고려하여 Holt-Winters 모델이 이 데이터에 가장 적합한 모델임을 확인하였습니다. 분석 결과를 토대로 미래 기온을 예측하고 전략을 수립할 수 있을 것으로 기대됩니다.
## solar-wind
