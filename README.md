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
금융범죄의 심각성 및 현황 파악

프로젝트 목적
금융사기를 방지하고 이에 사전에 방지하는 등 EDA를 통해 유형을 파악하며 데이터 분석을 통한 '브라이틱스를 통한 금융사기분석'

금융 계좌 개설 및 이용이 증가함에 따라 금융 사기에 대한 피해건수/피해액이 늘어나고 있다.
이에 따라 금융범죄의 심각성이 대두되고 피해를 막고자 금융 사기에 대응하고 있는 추세다.

part3. 분석 데이터
| 데이터 | 설명 | 컬럼명 |
|---|---|---|
| 금융사기 피해자의 연령대별 지역데이터 | '스마트 치안 빅데이터 플랫폼'에서 'THECHEAT'이 제공한 데이터로 금융사기 피해자의 연령대와 지역을 집계한 데이터 | 고유번호 / 생년구간 / 광역시도명 / 법정시군구명 / 등록일시 |
| 금융사기 피해자의 성별 지역데이터 | '스마트 치안 빅데이터 플랫폼'에서 'THECHEAT'이 제공한 데이터로 금융사기 피해자의 성별과 지역을 집계한 데이터 | 고유번호 / 성별 / 광역시도명 / 법정시군구명 / 등록일시 |
| 금융사기에 이용된 데이터_증권 /1금융권 | '스마트 치안 빅데이터 플랫폼'에서 'THECHEAT'이 제공한 데이터로금융사기에 이용된 일별 은행코드 (증권사코드), 은행명 (증권사명), 피해발생수를 집계한 데이터 | 고유번호 / 은행코드 (증권사코드) / 은행명 (증권사명) / 법정시군구명 / 등록일시 |
| 금융사기 피해자 통신사 데이터 | '스마트 치안 빅데이터 플랫폼'에서 'THECHEAT'이 제공한 데이터로 금융사기 피해자의 통신사를 집계한 데이터 | 고유번호 / 등록일시 / 자원인터넷서비스제공자 |
|2022.01 ~ 2022.09 | 2022.01 ~ 2022.09 | 2022.01 ~ 2022.09 | 2022.01 ~ 2022.09 |

 

part4. 전체 프로세스

4-1. 데이터 로드 및 결합

데이터 로드 및 Join과 관련된 프로세스
 Join 및 Distinct 함수 사용_ 연령/성별/통신사
Join 및 Distinct 함수 사용_ 증권/1금융권
데이터 로드 및 Join과 관련된 프로세스


04-2. Encoder 및 전처리

Encoder 전체 프로세스
Label Encoder
Filter_ 광역시도명 / 자원인터넷서비스
OneHot Encoder
전처리 후 데이터프레임

04-3. 데이터 시각화를 통한 EDA 분석

성별
시간
연령대
자원인터넷서비스제공자
은행
지역_광역시도별
지역_서울특별시
지역_서울특별시_중구



04-4. 모델링 프로세스

분류 모델링 구성

05. 결론_금융사기분석 & 기대효과
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
