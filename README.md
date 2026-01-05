## Customer Churn Prediction

### Project Overview

Customer churn is a major challenge for telecom companies.
This project focuses on predicting customer churn using historical customer data, enabling businesses to take proactive retention actions.

### Objective

Build a classification model that:

- a customer will churn
- Prioritizes recall for churners, not just accuracy
- Demonstrates real-world, business-oriented decision-making

### Project Structure
customer-churn-prediction/
│
├── EDA.ipynb
├── Feature_Engineering.ipynb
├── Modeling.ipynb
├── telco_TS.csv
└── README.md

#### Exploratory Data Analysis

- Examined churn distribution and key customer attributes

- Identified numerical and categorical features

- Observed class imbalance common in churn datasets
(See EDA.ipynb for details)

#### Feature Engineering

- Encoded categorical variables

- Prepared numerical features

- Ensured data was suitable for machine learning models

(See Feature_Engineering.ipynb)

#### Modeling Approach

- Model: Logistic Regression
- Train-Test Split: 80/20 with stratification
- Feature Scaling: StandardScaler
- Evaluation Metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC

#### Model Performance

- Accuracy: 74%
- ROC-AUC: 0.79
- Churn Recall (default threshold): 61%
- Churn Recall (threshold = 0.4): 72%

Threshold tuning was applied to improve churn detection, making the model more aligned with real-world retention strategies.

### Key Insights

- Logistic Regression provides a strong baseline for churn prediction
- Scaling features improves convergence and stability
- Threshold tuning significantly improves business usefulness
- Prioritizing recall is more valuable than maximizing accuracy in churn problems

## Project Takeaways

- Churn prediction requires prioritizing recall over accuracy.
- Proper feature preparation and scaling significantly improve model stability.
- Threshold tuning provides meaningful business trade-offs.
- Logistic Regression offers a strong, interpretable baseline for churn analysis.