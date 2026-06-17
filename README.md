Customer Churn Prediction

Project Overview

This project implements a machine learning solution to predict customer churn for a telecommunications company. The model analyzes customer data from Q2 2022 to identify patterns and predict whether customers will stay, leave (churn), or join the company.

Dataset: 7,043 customers from a Telecommunications company in California

Objective: Build a predictive model to identify customers at risk of churning

Best Model Performance: XGBoost Classifier with 80.86% accuracy


Dataset Description

Customer Churn Table

Contains comprehensive information for all customers including:


Demographics: Age, Gender, Marital Status, Number of Dependents
Location Data: City, State (California), Zip Code
Service Information: Internet Type, Payment Method, Contract Type, Services Subscribed
Financial Data: Monthly Charges, Total Charges, Long Distance Charges, Extra Data Charges
Behavioral Data: Tenure (in months), Offers Applied, Referrals
Target Variable: Customer Status (Joined, Stayed, or Churned)


Features Included


Total of 21 features after preprocessing
Mix of categorical and numerical variables
Services tracked: Streaming TV, Movies, Music, Online Security, Device Protection, Premium Tech Support, Online Backup, Paperless Billing, Unlimited Data, Phone Service, Multiple Lines



Methodology

1. Data Preprocessing


Removed irrelevant columns: Customer ID, Total Refunds, Zip Code, Latitude, Longitude, Churn Category, Churn Reason
Handled missing values through interpolation and dropping null entries
Final dataset shape: 7,043 rows × 16 features


2. Exploratory Data Analysis (EDA)


Analyzed distribution of customer demographics (Age, Dependents, Referrals)
Visualized customer behavior patterns across different segments
Created correlation heatmaps to identify relationships between variables
Performed outlier analysis using box plots
Examined payment methods, contract types, and service offerings


3. Feature Engineering


Label Encoding:

Gender: Female (0), Male (1)
Binary features (Yes/No): Mapped to 0/1
Includes: Paperless Billing, Unlimited Data, Streaming Services, Security Features, etc.



One-Hot Encoding: Applied to categorical features

Payment Method, Contract Type, Internet Type, Offers, City



Feature Scaling: MinMax Normalization applied to numerical features

Scaled features: Age, Tenure, Charges (Monthly, Total, Long Distance, Extra Data), Revenue





4. Model Development

Models Evaluated:


Random Forest Classifier
Logistic Regression
Gaussian Naive Bayes
Decision Tree Classifier
XGBoost Classifier  (Best Performer)
Support Vector Classifier



5. Model Evaluation


Train-Test Split: 80% training, 20% testing
Performance Metrics:

Accuracy Score
Confusion Matrix
Classification Report (Precision, Recall, F1-Score)


Results

Final Model Performance

Selected Model: XGBoost Classifier

Test Accuracy: 80.86%

