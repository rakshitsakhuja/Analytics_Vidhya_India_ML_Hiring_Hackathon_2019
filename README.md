# Analytics_Vidhya_India_ML_Hiring_Hackathon_2019
Regression Problem for finding Loan Delinquency

# Approach and Steps for this Competition
1. Read train and test files
2. Checked for unique datapoints in loan_id, source, financial_institution, interest_rate, number_of_borrowers, loan_purpose, loan_term features
3. Created feature for difference in origination_date_dt,first_payment_date_dt as duration to measure the time after which lender started  paying back money and removed theese 2 columns for further analysis in both train and test
4. Created Dummy variables for the given features by concatenating data for both train and test ( because there are som values which were not present in either one thats why created dummy variables by combining train-test)
5. Applied F regression  and SelectKbest for selecting best 19 best features to be used in model
6. Implemented Train-test Split and Used SMOTE algorithm for creating synthetic data to handle the problem of imabalnced dataset
7. Leveraged Random Forest Regressor on this data for model creation and validation and checked for best f1 score 
8. Leveraged XGBoost as well but results were not good regarding regarding best f1 score so chose final output from Random Forest Regressor only

### Requirement ( Libraries Used) :

pandas==0.23.4
numpy==1.16.0
ipython==6.1.0
scikit-learn==0.21.3
imblearn==0.0
xgboost==0.80

### Accuracy Measure : F1 - Score
LeaderBoard:

Public : 0.3269

Private : 0.5675

Contest Link : https://datahack.analyticsvidhya.com/contest/india-ml-hiring-hackathon-2019/
