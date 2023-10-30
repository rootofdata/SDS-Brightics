# SDS-Brightics


## Smart factory semiconductor process optimization

## Medical_Cost_Prediction
### **Project Title:** Predicting Personal Medical Expenses (Insurance) Project

### **Project Overview:** In this analysis project, an individual-specific medical cost prediction model is constructed and evaluated by considering factors such as age, gender, obesity, number of childbirths, residence, and smoking status.  
Project Purpose:  
- Through predicting medical expenses based on social and physical individual information, individuals can forecast their medical costs, preventing overpayment and allowing them to pay corresponding insurance premiums directly. Additionally, insurance companies can understand trends in insurance cost changes and plan customized products accordingly.
1. Data Collection: Follow the data collection path below (Kaggle dataset).  
2. Data Preprocessing:  
- Check for missing values in all columns and handle them through removal or imputation.  
- Perform Label Encoding for columns with string data types.  
- Remove rows where negative values are present in any column.  
- Identify outliers based on criteria: age: 100 years, children: 10, and remove corresponding rows.  
- Apply One-Hot Encoding for necessary columns.  
  
3. Modeling:  

- Analyze the distribution of variables with Charges and select feature columns accordingly.  
- Split the preprocessed dataset into an 80:20 ratio.  
- Train/Test the data using models such as AdaBoost, Decision Tree, Linear Regression, Penalized Linear Regression, Random Forest, XGB Regression, etc.  
- If possible, find optimal parameters using GridSearchCV.  

4. Model Evaluation and Selection:  
- Select an evaluation metric (MAE, MSE, RMSE, MAPE) to calculate scores and choose the best-performing model.  

Data Source: Utilize the 'Medical Cost Personal Datasets' from Kaggle's Open DataSet.  
Medical Cost Personal Datasets | Kaggle  

## Weather Conditions

## solar-wind
