📊 Customer Churn Prediction
This project applies machine learning to predict customer churn in a subscription-based service. By analyzing various features about customer behavior and contract details, 
the goal is to accurately determine which customers are at risk of leaving.

🗂️ Project Structure

customer churn prediction/
│
├── customer_churn_prediction.ipynb   # Jupyter notebook with full analysis & modeling
├── customer churn.csv                # Dataset used for training & evaluation
├── logistic_regression_pipeline.pkl  # Saved pipeline for best-performing model
└── README.md                         # Project documentation (this file)

📄 Dataset Overview
The dataset contains customer information, service usage, and account status. The target column is Churn (Yes/No), indicating whether a customer left the service.

🔍 Features
Feature	Description
gender	Customer gender (Male/Female)
SeniorCitizen	Whether the customer is a senior citizen (0/1)
Partner	Whether the customer has a partner (Yes/No)
Dependents	Whether the customer has dependents (Yes/No)
tenure	Number of months the customer has stayed
PhoneService	Whether the customer has phone service (Yes/No)
MultipleLines	Whether the customer has multiple lines (Yes/No/No phone)
InternetService	Internet provider type (DSL/Fiber optic/No)
OnlineSecurity	Whether online security is enabled
OnlineBackup	Whether online backup is enabled
DeviceProtection	Whether device protection is enabled
TechSupport	Whether tech support is available
StreamingTV	Streaming TV service (Yes/No/No internet)
StreamingMovies	Streaming movies service (Yes/No/No internet)
Contract	Contract type (Month-to-month/One year/Two year)
PaperlessBilling	Whether billing is paperless
PaymentMethod	Payment method (Credit card/Bank transfer/etc.)
MonthlyCharges	The amount charged per month
TotalCharges	Total amount charged during the customer’s tenure

🎯 Target
Column	Description
Churn	Whether the customer churned (Yes/No)

This column is transformed into binary (Yes → 1, No → 0).

🧪 Models Used
The following models were trained using a preprocessing pipeline and evaluated via cross-validation:

Logistic Regression (with class balancing)

Decision Tree

Random Forest

XGBoost

Each pipeline includes:

StandardScaler for numerical features

OneHotEncoder for categorical features

class_weight='balanced' or scale_pos_weight for handling class imbalance

📈 Model Evaluation
Evaluation Metric: ROC AUC Score

Validation: 5-Fold Cross-Validation

Best model saved as .pkl using joblib

📌 The best-performing model from this analysis was:
Logistic Regression

💾 Output
A bar chart comparing ROC AUC scores of all models

Best model saved as:

logistic_regression_pipeline.pkl

📦 Requirements
Install required packages:


pip install pandas numpy scikit-learn seaborn matplotlib xgboost joblib
▶️ How to Use
Place all files in the same folder:


customer churn prediction/
Open and run the Jupyter Notebook:


customer_churn_prediction.ipynb
The notebook:

Loads the dataset

Performs EDA and preprocessing

Trains and compares models

Saves the best model pipeline

📫 Contact
Created by Mohana Priya Murugesan
📧 Email: priyamurugesan3299@gmail.com
