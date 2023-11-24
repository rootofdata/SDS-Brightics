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

**Remark** : https://www.brightics.ai/community/knowledge-sharing/detail/7098

## Medical_Cost_Prediction

#### **Title:** Predicting Personal Medical Expenses (Insurance) Project
![download (1)](https://github.com/rootofdata/SDS-Brightics/assets/86711374/952b6d2c-bb9d-429e-ad52-78f2a82996b6)
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
![download](https://github.com/rootofdata/SDS-Brightics/assets/86711374/f3462f52-c2f4-4df8-b7a3-ac90ba41e095)
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
### Assessing the Severity and Current Status of Financial Crimes

### The purpose of the project
**To prevent and proactively address financial fraud through Exploratory Data Analysis (EDA). The analysis aims to identify patterns through EDA and analyze financial fraud using 'Brightics.'**
- With the increase in the opening and usage of financial accounts, the number of financial fraud cases and the associated losses have been rising.
- Consequently, there is a growing concern about the severity of financial crimes. Efforts are being made to respond to financial fraud and mitigate its impact.

### Data

Date: January 2022 to September 2022
Source: Data provided by 'THECHEAT' from the 'Smart Security Big Data Platform.'
#### Financial Fraud Victims' Age and Location Data
- Unique ID / Birth Year Range / Metropolitan Area Name / Legal City or County Name / Registration Date
#### Financial Fraud Victims' Gender and Location Data
- Unique ID / Gender / Metropolitan Area Name / Legal City or County Name / Registration Date
#### Data Used in Financial Fraud - Securities / 1st Financial Sector
- Unique ID / Bank Code (Securities Company Code) / Bank Name (Securities Company Name) / Legal City or County Name / Registration Date
#### Financial Fraud Victims' Telecom Provider Data
- Unique ID / Registration Date / Internet Service Provider
 
### Overall Process
![image](https://github.com/rootofdata/SDS-Brightics/assets/86711374/7f5198be-32b1-451f-a314-d564bdb383ff)

#### Data Loading and Combination
- Load and join related processes.
- Join and Distinct Functions Usage
  - Age/Gender/Telecom, Securities/1st Financial Sector
### Encoder Process

#### Label Encoder
- Convert multiple variables into numeric values within a single column.
- For example, create an index named 'Name_index' and categorize 'Kim Bros' as 0, 'Seo Bros' as 1, and 'Choi Bros' as 2.
#### Filter 
- Filter based on the count of top variables for Metropolitan Area / Internet Service Provider, considering it for OneHotEncoder.
#### OneHotEncoder
- Generate columns for multiple variables and fill the columns with 1 if applicable, and 0 otherwise (e.g., Name_0, Name_1, Name_2).
  
#### Data Visualization for EDA Analysis
- Analyze gender distribution among suspects, monthly financial fraud cases, age group-wise fraud cases, and prominent banks/financial institutions.  
#### **1. Gender:**  
- In the case of suspects (perpetrators), males account for approximately 80% of the total, indicating that males are significantly more involved in financial fraud-related activities.
#### **2. Monthly Financial Fraud Cases:** 
- In descending order, the months with the highest number of financial fraud cases are August, followed by September, July, and March.
- The data shows a balanced distribution across months, indicating there is no significant imbalance.
- Consequently, it can be inferred that financial fraud occurrences are not strongly correlated with specific months.
#### **3. Financial Fraud Cases by Birth Year Range**
- When categorized by birth year range (age groups), individuals born in the 2000s, specifically late teens to early twenties, experienced the highest number of financial fraud incidents.
- Following this group, those born in the 1990s and 1980s had the next highest occurrences, in that order.
#### **4. Bank Name / Bank Code**
- When examined by bank name (bank code), KakaoBank dominates, accounting for approximately 22% of the cases.
- While the high prevalence of KakaoBank might be influenced by the large number of users, knowing the actual user counts could reveal which financial institutions are more susceptible to fraud.

### Modeling Process
#### Classification Train
- Use 'Bank Name' as the Y variable, split the data, and group 'Bank Name' by applying group by.
#### Classification Predict
- Measure predictions as probabilities for multi-class classification. Set Shuffle Type as index.
#### Evaluate Classification
- Compare metrics such as accuracy and F1 score between 'Bank Name' and predictions.

### Conclusion - Financial Fraud Analysis & Expected Benefits
#### Societal Impact
- With the advancement of IT, the importance of financial security in society has increased.
- This analysis aims to analyze types of financial crimes and prevent them in advance, contributing to reducing social harm and enhancing stability.
#### Corporate Perspective
- Each bank aims to strengthen security and prevent financial fraud.
- By securing data from non-victims, banks can offer better products, such as insurance related to financial fraud or preventive measures.
#### Individuals
- Individuals can enhance their personal security by understanding which financial institutions are more vulnerable.
- Providing numerical information about financial crimes enables the dissemination of knowledge, allowing individuals to take necessary precautions.

## [Solar Power / Wind Power Forecasting](https://github.com/rootofdata/SDS-Brightics/tree/main/solar-wind)

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
