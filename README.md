# SDS-Brightics

## [Smart Factory Semiconductor Process Optimization](https://github.com/rootofdata/SDS-Brightics/blob/main/Semiconductor%20optimization/README.md)
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

## [Weather Conditions](https://github.com/rootofdata/SDS-Brightics/blob/main/Weather%20Conditions/README.md)

#### The goal is to investigate the impact of weather data on the postponement of D-DAY during World War II through data analysis and identify stable time periods.
#### Main Objective
- The objective of this project was to analyze weather data sourced from the 'Aerial Bombing Operations of World War Two' dataset.
- The focus was on weather station locations and climate information recorded on specific dates.
- By employing various statistical techniques and time series models, the project aimed to gain insights into historical weather patterns and predict future temperatures.
- The analysis holds significance in identifying stable time periods unaffected by World War Two aerial bombing operations, enabling strategic planning based on weather conditions.

### Analysis Steps:
#### Data Preprocessing:
- The initial step involved meticulous data preprocessing.
- The dataset was loaded and carefully cleaned, addressing missing values to ensure the reliability of subsequent analyses.
- Visualizations were employed to explore data characteristics, with a specific focus on data related to Seoul, providing a localized perspective.

#### Statistical Testing:
- **Unit Root Test:** Unit root tests were conducted to confirm the stationarity of the data.
- **ACF:** Autocorrelation analysis was employed to understand the data's autocorrelation structure, providing valuable insights into its behavior over time.
#### Analytical Techniques
- Primarily, time series data was analyzed using Moving Average (MA) and Exponentially Weighted Moving Average (EWMA) models, applied using Brightics Studio.

#### Modeling Approaches:
Moving Average (MA) and Exponentially Weighted Moving Average (EWMA) Models:
- MA and EWMA models were implemented to analyze the time series data. EWMA, with its adaptive nature to recent variations, showcased superior accuracy. A comparative analysis of MA and EWMA models highlighted the latter’s effectiveness in capturing historical weather trends.

#### ARIMA and Holt-Winters Models:
- ARIMA models were manually configured, but the process revealed the need for parameter tuning to improve performance.
- Auto ARIMA, although an improvement, fell short compared to the Holt-Winters model.
- The Holt-Winters model, leveraging its ability to capture trends and seasonality, emerged as the most suitable choice.

#### Analysis and Results:
- Comparative metrics such as Root Mean Square Error (RMSE) and Mean Absolute Percentage Error (MAPE) were employed to assess model performance.
- The Holt-Winters model demonstrated remarkable accuracy, outperforming other models. 
- Its ability to predict future temperatures accurately makes it invaluable for strategic planning, allowing stakeholders to identify stable time periods unaffected by historical events.

#### Conclusion and Implications:
- In conclusion, the comprehensive analysis of weather data from World War Two aerial bombing operations provides valuable insights into historical weather patterns.
- The Holt-Winters model, identified as the most accurate, equips decision-makers with a powerful tool for predicting future temperatures.
- This knowledge is instrumental in strategic planning, enabling the identification of stable time periods for various activities.
- The implications are vast, ranging from agricultural planning to urban development, ensuring decisions are informed by historical weather trends, enhancing their efficacy and resilience.
- Based on the analysis results, future temperature predictions and strategic planning can be conducted, facilitating informed decision-making.


## Financial Fraud Analysis [https://github.com/rootofdata/SDS-Brightics/blob/main/Financial%20Fraud%20Analysis/README.md]

## solar-wind
- KETI 지속가능한 에너지 활용을 위한 인공지능 경진대회
