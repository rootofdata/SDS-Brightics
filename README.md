# SDS-Brightics

## [Smart Factory Semiconductor Process Optimization](https://github.com/rootofdata/SDS-Brightics/blob/main/Semiconductor%20optimization/README.md)
#### **Background and Objectives**. 
- The objective of this project was to enhance anomaly detection performance in a smart factory setting, specifically focusing on optimizing semiconductor manufacturing processes.
- The goal was to identify and predict defective products, thereby improving overall product quality.
  
#### **Project Overview**. 
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

## [Weather Conditions](https://github.com/rootofdata/SDS-Brightics/blob/main/Weather%20Conditions/README.md)

#### The goal is to investigate the impact of weather data on the postponement of D-DAY during World War II through data analysis and identify stable time periods.
### Main Objective
- The objective of this project was to analyze weather data sourced from the 'Aerial Bombing Operations of World War Two' dataset.
- The focus was on weather station locations and climate information recorded on specific dates.
- By employing various statistical techniques and time series models, the project aimed to gain insights into historical weather patterns and predict future temperatures.
- The analysis holds significance in identifying stable time periods unaffected by World War Two aerial bombing operations, enabling strategic planning based on weather conditions.

### Analysis Steps:
### Data Preprocessing:
- The initial step involved meticulous data preprocessing.
- The dataset was loaded and carefully cleaned, addressing missing values to ensure the reliability of subsequent analyses.
- Visualizations were employed to explore data characteristics, with a specific focus on data related to Seoul, providing a localized perspective.

### Statistical Testing:
- **Unit Root Test:** Unit root tests were conducted to confirm the stationarity of the data.
- **ACF:** Autocorrelation analysis was employed to understand the data's autocorrelation structure, providing valuable insights into its behavior over time.
### Analytical Techniques
- Primarily, time series data was analyzed using Moving Average (MA) and Exponentially Weighted Moving Average (EWMA) models, applied using Brightics Studio.

### Modeling Approaches:
#### Moving Average (MA) and Exponentially Weighted Moving Average (EWMA) Models:
- MA and EWMA models were implemented to analyze the time series data. EWMA, with its adaptive nature to recent variations, showcased superior accuracy. A comparative analysis of MA and EWMA models highlighted the latter’s effectiveness in capturing historical weather trends.

#### ARIMA and Holt-Winters Models:
- ARIMA models were manually configured, but the process revealed the need for parameter tuning to improve performance.
- Auto ARIMA, although an improvement, fell short compared to the Holt-Winters model.
- The Holt-Winters model, leveraging its ability to capture trends and seasonality, emerged as the most suitable choice.

### Analysis and Results:
- Comparative metrics such as Root Mean Square Error (RMSE) and Mean Absolute Percentage Error (MAPE) were employed to assess model performance.
- The Holt-Winters model demonstrated remarkable accuracy, outperforming other models. 
- Its ability to predict future temperatures accurately makes it invaluable for strategic planning, allowing stakeholders to identify stable time periods unaffected by historical events.

### Conclusion and Implications:
- In conclusion, the comprehensive analysis of weather data from World War Two aerial bombing operations provides valuable insights into historical weather patterns.
- The Holt-Winters model, identified as the most accurate, equips decision-makers with a powerful tool for predicting future temperatures.
- This knowledge is instrumental in strategic planning, enabling the identification of stable time periods for various activities.
- The implications are vast, ranging from agricultural planning to urban development, ensuring decisions are informed by historical weather trends, enhancing their efficacy and resilience.
- Based on the analysis results, future temperature predictions and strategic planning can be conducted, facilitating informed decision-making.


## [Financial Fraud Analysis](https://github.com/rootofdata/SDS-Brightics/blob/main/Financial%20Fraud%20Analysis/README.md)
### 금융범죄의 심각성 및 현황 파악

### 프로젝트 목적
**금융사기를 방지하고 이에 사전에 방지하는 등 EDA를 통해 유형을 파악하며 데이터 분석을 통한 '브라이틱스를 통한 금융사기분석'**
- 금융 계좌 개설 및 이용이 증가함에 따라 금융 사기에 대한 피해건수/피해액이 늘어나고 있다.
- 이에 따라 금융범죄의 심각성이 대두되고 피해를 막고자 금융 사기에 대응하고 있는 추세다.

### 분석 데이터

날짜 : 2022.01 ~ 2022.09
데이터 : '스마트 치안 빅데이터 플랫폼'에서 'THECHEAT'이 제공한 데이터
| 데이터 | 설명 | 컬럼명 |
|---|---|---|
| 금융사기 피해자의 연령대별 지역데이터 | 금융사기 피해자의 연령대와 지역을 집계한 데이터 | 고유번호 / 생년구간 / 광역시도명 / 법정시군구명 / 등록일시 |
| 금융사기 피해자의 성별 지역데이터 | 금융사기 피해자의 성별과 지역을 집계한 데이터 | 고유번호 / 성별 / 광역시도명 / 법정시군구명 / 등록일시 |
| 금융사기에 이용된 데이터_증권 /1금융권 | 금융사기에 이용된 일별 은행코드 (증권사코드), 은행명 (증권사명), 피해발생수를 집계한 데이터 | 고유번호 / 은행코드 (증권사코드) / 은행명 (증권사명) / 법정시군구명 / 등록일시 |
| 금융사기 피해자 통신사 데이터 | 금융사기 피해자의 통신사를 집계한 데이터 | 고유번호 / 등록일시 / 자원인터넷서비스제공자 |
 
### 전체 프로세스
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/7f5198be-32b1-451f-a314-d564bdb383ff)

#### 데이터 로드 및 결합

- 데이터 로드 및 Join과 관련된 프로세스
- Join 및 Distinct 함수 사용_ 연령/성별/통신사, 증권/1금융권

### Encoder 전체 프로세스
#### Label Encoder
- 여러 변수가 있더라도 일련의 숫자로 하여금 하나의 Column 내에서 처리
- 이름_index로 Column을 만들고,김브스를 0, 서브스를 1, 최브스를 2로 분류
#### Filter 
- 광역시도별 / 자원인터넷서비스, OneHotEncoder를 위한 Filter로count 기준 상위 개수를 고려하여Filter를 통해 column에 해당할 변수를 선택
#### OneHotEncoder
- 여러 변수를 그 변수에 대한 Column들을 일일이 생성하여 처리
- Column명을 이름_0, 이름_1, 이름_2 로 하여 이에 해당하면 1, 해당하지 않는다면 0으로 column을 채우는 방식

#### 데이터 시각화를 통한 EDA 분석
**1. 성별**
용의자 (가해자)의 성별 또한 남자가 80%에 달하는 수치로 금융사기와 관련된 성별은 남자가 훨씬 많다.
**2. 월별 금융사기 건수** 
- 가장 많았던 달 순으로는 8월 > 9월 > 7월 > 3월 순. 데이터의 불균형이 없다고 볼 정도로 균형있게 분포되어있음을 알 수 있다. 이로써 금융사기는 월과는 크게 상관이 없다는 것도 알 수 있다.
**3. 생년구간별 금융사기 건수**
- 생년구간(연령대)로 하였을 때, 금융사기와 관련된 피해자의 경우 ,00년대생 즉 10대 후반 혹은 20대 초반이 가장 많았고, 그 다음이 90년대생, 80년대생 순으로 많았습니다.
**4. 은행명 / 은행코드**
- 은행명 (은행코드)로 보았을 때, 카카오뱅크가 약 22%로 많은 부분을 차지하고 있다.
- 은행과 금융의 이용자수가 많음도 있을 수 있겠지만,실제 이용자 수를 알 수 있다면 취약한 금융권이 어느 곳인지도 알 수 있다.

### 모델링 프로세스
#### Classification Train
- '은행명'을 Y변수로 하여 Split 시,'은행명'을 group by하여 나눠줌.
#### Classification Predict
- prediction을 probability로 측정하여 다중 분류로 구성 Suffle Type을 index로 설정
#### Evaluate Classification
- Accuracy와 F1 등 평가지표를 은행명과 prediction으로 비교

### 결론_금융사기분석 & 기대효과
#### 사회
- 사회적으로 바라봤을 때 IT가 발전함에 따라 금융의 보안의 중요성이 대두된다.
- 이에 따라 사회적으로 피해를 줄이고, 안정화시키기 위해 금융범죄의 유형을 분석하고 사전에 미리 예방할 수 있도록  돕기 위함이다.

#### 기업
- 기업적으로 바라봤을 때 각 은행별로 보안과 금융사기에 대한 예방을 철저히 하기 위함이다.
- 비피해자의 데이터가 확보된다면 금융사기와 관련된 보험을 제시하거나 사전에 예방할 수 있는 상품을 개발하여 더욱 좋은 상품을 제공할 수 있다.

#### 개인
- 개인으로 바라봤을 때 자신과 비슷한 유형의 소비자가 어느 금융에서 많이 취약했는지를 알려줌으로써 개인적인 보안과 점검을 할 수 있도록 하기 위함이다.
- 금융범죄에 대해 수치적으로 알려줌으로써 정보를 제공한다.

## solar-wind

### Solar Power Forecasting:
#### Forecast Data (solar_forecast_weather):
- Forecast Period: 20-09-01 11:00 ~ 22-07-01 8:00 (1-hour intervals)
- Predicted solar power generation for hours after the forecast time

#### Solar Power Generation Data (solar_power_2204):
- Measurement Period: 20-09-10 0:00 ~ 22-04-30 23:50 (10-minute intervals)
- Actual solar power generation data

#### Weather Observation Data (weather_solar_actual):
- Measurement Point: 112 (Incheon)
- Measurement Period: 20-09-01 0:00 ~ 22-06-30 23:00 (1-hour intervals)
- Includes temperature, wind speed, wind direction, and humidity information

### Wind Power Forecasting:
#### Forecast Data (wind_forecast_weather):
- Forecast Period: 20-09-01 11:00 ~ 22-07-01 8:00 (1-hour intervals)
- Predicted wind power generation for hours after the forecast time

#### Wind Power Generation Data (wind_2204):
- Measurement Period: 20-09-10 0:00 ~ 22-04-30 23:50 (10-minute intervals)
- Actual wind power generation data

#### Weather Observation Data (weather_wind_actual):
- Measurement Point: 156 (Gwangju)
- Measurement Period: 20-09-01 0:00 ~ 22-06-30 23:00 (1-hour intervals)
- Includes temperature, wind speed, wind direction, and humidity information
![Untitled (53)](https://github.com/rootofdata/SDS-Brightics/assets/86711374/1c8f0038-f92f-434f-aeec-3e967555c434)
