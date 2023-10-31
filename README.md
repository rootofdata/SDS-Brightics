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

#### Main Objective
- The goal is to investigate the impact of weather data on the postponement of D-DAY during World War II through data analysis and identify stable time periods.
#### Data Introduction
- The analysis utilizes the Aerial Bombing Operations of World War Two dataset, consisting of key columns such as weather observation locations, climate information, dates, maximum temperature, mean temperature, and minimum temperature.
#### Analytical Techniques
- Primarily, time series data was analyzed using Moving Average (MA) and Exponentially Weighted Moving Average (EWMA) models, applied using Brightics Studio.

#### Analysis Steps:

- **Initial Data Exploration:** Data was loaded, missing values were handled, and visualization was employed to understand its characteristics.
- **Unit Root Test:** Unit root tests were conducted to confirm the stationarity of the data.
- **Moving Average and Exponentially Weighted Moving Average Model Creation:** Both models were generated and evaluated using metrics like MAPE and MSE. A comparison of the results led to the selection of the final model.
- **Results and Evaluation:** The outcomes of both models were compared, and the final model was chosen based on metrics. Future temperature predictions and identification of stable time periods were made using this model.
- **MA vs. EWMA Model Comparison:** MAPE and RMSE were utilized for model comparison. Visual comparison confirmed that EWMA provided more accurate predictions.
- **Autocorrelation (ACF) Analysis:** ACF was used to analyze the correlation in time series data and identify the order of the Moving Average (MA) component.
- **Data Preprocessing:** Differencing was applied to achieve stationarity. ARIMA and Auto ARIMA models were then used for predictions.
- **Holt-Winters Model:** Holt-Winters exponential smoothing was employed for modeling, and the model's performance was evaluated.
- **Model Evaluation Metrics:** RMSE and MAPE were calculated for ARIMA, Auto ARIMA, and Holt-Winters models.

#### Conclusion
- Based on the analysis results, future temperature predictions and strategic planning can be conducted, facilitating informed decision-making.

## solar-wind
- KETI 지속가능한 에너지 활용을 위한 인공지능 경진대회
