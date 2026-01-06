# Customer Churn Prediction (Telecom Dataset)

## Project Overview

Customer churn occurs when customers stop using a company’s product or service.  
In the telecom industry, even a small increase in churn can lead to significant revenue loss.

This project builds a **machine learning model to predict customer churn** using historical telecom customer data.  
The goal is to identify **customers at high risk of leaving** so businesses can take **proactive retention actions**.

---

## Business Objective

- Predict whether a customer is likely to churn
- Identify patterns and behaviors linked to churn
- Improve churn detection by optimizing classification thresholds
- Provide insights that support customer retention strategies

---

## 🗂️ Project Structure

customer-churn-prediction/  
│  
├── data/  
│   └── telco_TS.csv  
│  
├── notebooks/  
│   ├── 01_EDA.ipynb  
│   ├── 02_Feature_Engineering.ipynb  
│   └── 03_Modeling.ipynb  
│  
├── README.md  
├── requirements.txt  
├── .gitignore  
└── .gitattributes  


---

## Dataset

- **Source:** Telecom customer dataset
- **Target Variable:** `Churn`  
  - `1` → Customer churned  
  - `0` → Customer retained
- **Features Include:**
  - Demographics
  - Account information
  - Subscription details
  - Service usage patterns

---

## Project Workflow

### 1. Exploratory Data Analysis (EDA)
- Understand customer demographics and service usage
- Analyze churn distribution and imbalance
- Explore relationships between features and churn
- Identify data quality issues

📌 *Key insight:* Certain contract types, tenure length, and payment methods strongly influence churn.

---

### 2. Feature Engineering
- Encode categorical variables using One-Hot Encoding
- Separate features (`X`) and target (`y`)
- Prepare data for machine learning models
- Ensure compatibility with scikit-learn pipelines

📌 *Why this matters:*  
Machine learning models require numerical, well-structured inputs to perform optimally.

---

### 3. Modeling
- Train/Test split with stratification to preserve churn distribution
- Feature scaling for better convergence
- Logistic Regression used as a baseline model
- Model evaluation using:
  - Accuracy
  - Precision
  - Recall
  - F1-Score
  - ROC-AUC
- Probability threshold tuning to improve churn detection

---

## 📊 Model Performance

### 🔹 Default Threshold (0.5)
- **Accuracy:** ~74%
- **ROC-AUC:** ~0.80
- **Churn Recall:** ~61%

### 🔹 Tuned Threshold
- **Churn Recall improved to ~72%**
- Better identification of customers likely to churn
- Slight trade-off in precision (acceptable in churn scenarios)

📌 **Business Insight:**  
In churn prediction, **recall is more important than accuracy** — missing a churner is costlier than targeting a non-churner.

---

## Tools & Technologies

- Python
- Pandas & NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook

---

## ⚙️ Installation & Usage

Clone the repository:
```bash
git clone https://github.com/Blessing-analytics/customer-churn-prediction.git
cd customer-churn-prediction
```

Install dependencies:
```bash
pip install -r requirements.txt
```

Run notebooks in order:

01_EDA.ipynb  
02_Feature_Engineering.ipynb  
03_Modeling.ipynb  

---

## 📈 Key Insights

- Customers with shorter tenure are more likely to churn.
- Contract type and payment method significantly influence churn behavior.
- Threshold tuning improves the effectiveness of churn detection.
- Logistic Regression provides a strong and interpretable baseline model for binary classification.

---

## 👤 Author

**Atoyebi Simon Blessing (Blessing-analytics)**  
Data Analyst | Python | SQL  
📎 GitHub: https://github.com/Blessing-analytics  

⭐ If you find this project useful, feel free to star the repository.