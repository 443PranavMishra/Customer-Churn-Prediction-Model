# 📊 Customer Churn Prediction using Advanced Ensemble Machine Learning

<p align="center">
<img src="https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge&logo=python">
<img src="https://img.shields.io/badge/Scikit--Learn-ML-orange?style=for-the-badge">
<img src="https://img.shields.io/badge/XGBoost-Ensemble-green?style=for-the-badge">
<img src="https://img.shields.io/badge/LightGBM-Boosting-success?style=for-the-badge">
<img src="https://img.shields.io/badge/CatBoost-Gradient-yellow?style=for-the-badge">
<img src="https://img.shields.io/badge/License-MIT-red?style=for-the-badge">
</p>

---

Dataset Link : https://www.kaggle.com/datasets/pranavmishra443/dataset

# 🚀 Project Overview

Customer churn is one of the biggest challenges in the banking industry. Losing existing customers directly impacts revenue and increases customer acquisition costs.

This project develops a **high-performance Customer Churn Prediction System** using an advanced **Stacking Ensemble Learning** approach that combines multiple state-of-the-art machine learning models.

The solution was developed for the **ChurnZero'26 Analytics Competition organized by IIT Kharagpur**.

The objective is to predict:

- Customer Churn (0 / 1)
- Probability of Churn

allowing businesses to proactively identify high-risk customers and launch retention campaigns before customers leave.

---

# 🎯 Problem Statement

Given customer information including:

- Customer Profile
- Banking Relationship
- Transaction History
- Digital Banking Engagement
- Product Usage
- Complaints History
- Marketing Response

Predict whether the customer will churn in the upcoming period.

---

# 📂 Dataset Information

Training Samples : **8,101**

Test Samples : **2,026**

Total Features : **97**

Feature Categories:

- Customer Profile
- Relationship & Tenure
- Transaction Behaviour
- Product Holdings
- Credit Card & Loan Behaviour
- Digital Banking Engagement
- Complaint History
- Marketing & Retention

Target Variable

```
churn
0 → Retained Customer
1 → Churn Customer
```

---

# ⚙️ Complete Machine Learning Pipeline

## 1️⃣ Data Loading

- Pandas
- NumPy

---

## 2️⃣ Data Cleaning

- Missing Value Analysis
- Duplicate Check
- Data Type Verification

---

## 3️⃣ Feature Engineering

Separated:

- Numerical Features
- Categorical Features

Prepared features for preprocessing using Scikit-Learn pipelines.

---

## 4️⃣ Missing Value Imputation

Used

- Median Imputation

Advantages

- Robust to outliers
- Maintains feature distribution
- Improves model stability

---

## 5️⃣ Outlier Treatment

Applied

- IQR (Interquartile Range)

Technique

```
Lower Bound = Q1 − 1.5 × IQR

Upper Bound = Q3 + 1.5 × IQR
```

Values outside the range were clipped.

---

## 6️⃣ Exploratory Data Analysis

Performed

- Class Distribution
- Feature Correlation
- Customer Behaviour Analysis
- Outlier Visualization
- Churn Driver Identification

---

## 7️⃣ Train Test Split

```
80%
Training

20%
Validation
```

Random State = 42

---

## 8️⃣ Data Preprocessing

### Numerical Features

- StandardScaler

### Categorical Features

- OneHotEncoder

Implemented using

```
ColumnTransformer
```

to avoid data leakage.

---

# 🤖 Machine Learning Models

The project uses a **Stacking Ensemble Model** consisting of four powerful gradient boosting algorithms.

## Base Models

✅ Random Forest

✅ XGBoost

✅ LightGBM

✅ CatBoost

Meta Learner

Stacking Classifier

This architecture combines the strengths of all individual models and significantly improves prediction performance.

---

# 🧠 Stacking Architecture

```
          Random Forest
                 │
          XGBoost
                 │
          LightGBM
                 │
          CatBoost
                 │
         Meta Learner
                 │
      Final Churn Prediction
```

---

# 📈 Model Performance

| Metric | Score |
|---------|--------|
| Accuracy | **99.88%** |
| Precision | **99.86%** |
| Recall | **99.46%** |
| F1 Score | **99.56%** |
| ROC-AUC | **99.75%** |
| PR-AUC | **99.19%** |

---

# 📊 Individual Model Comparison

| Model | PR-AUC |
|---------|---------|
| Random Forest | 97.80% |
| XGBoost | 98.50% |
| LightGBM | 98.70% |
| CatBoost | 98.82% |
| **Stacking Ensemble** | **99.19%** |

---

# 💰 Business Cost Analysis

Competition Cost Function

False Negative

```
₹40,000
```

False Positive

```
₹500
```

Final Confusion Matrix

```
TN = 1391

FP = 1

FN = 1

TP = 228
```

Estimated Business Loss

```
₹40,500
```

The model minimizes revenue loss by accurately identifying customers at high risk of churn.

---

# 🔍 Top Churn Drivers

The most influential features include:

- Customer Satisfaction Score
- Total Digital Logins
- Balance Decline Percentage
- Mobile Banking Usage
- Complaint Resolution Time
- Email Open Rate
- Transaction Frequency
- Cash Withdrawal Count
- Monthly Transaction Count
- Minimum Due Paid Flag

---

# 💡 Business Recommendations

### 🎯 Proactive Retention Campaigns

Target customers with churn probability above 80%.

---

### 📱 Improve Digital Engagement

Increase:

- Mobile Banking Usage
- Login Frequency
- Digital Transactions

---

### 😊 Improve Customer Satisfaction

Reduce

- Complaint Resolution Time

Improve

- Customer Support

---

### 📈 Personalized Marketing

Use churn probability scores to optimize retention spending.

---

### ⚡ Real-Time Monitoring

Deploy the model into production for continuous churn monitoring.

---

# 🛠️ Tech Stack

## Programming

- Python

## Data Analysis

- Pandas
- NumPy

## Visualization

- Matplotlib
- Seaborn

## Machine Learning

- Scikit-Learn
- XGBoost
- LightGBM
- CatBoost

## Model Pipeline

- Pipeline
- ColumnTransformer
- StandardScaler
- OneHotEncoder
- StackingClassifier

---

# 📁 Repository Structure

```
Customer-Churn-Prediction/

│

├── ChurnZero_dataset_v1.csv

├── ChurnZero_test_v1.csv

├── Customer_Churn_Prediction.ipynb

├── Predictions.csv

├── Presentation.pdf

├── README.md

└── requirements.txt
```

---

# ▶️ Installation

Clone the repository

```bash
git clone https://github.com/yourusername/customer-churn-prediction.git
```

Install dependencies

```bash
pip install -r requirements.txt
```

Run

```bash
jupyter notebook
```

Open

```
Customer_Churn_Prediction.ipynb
```

---

# 📦 Required Libraries

```
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
lightgbm
catboost
joblib
```

---

# 🎓 Competition

Developed for

**ChurnZero'26 Analytics Competition**

Indian Institute of Technology (IIT), Kharagpur

---

# 📬 Details

**Pranav Mishra**

📧 443pranavmishra@gmail.com

---

# ⭐ If you found this project useful

Please consider giving this repository a ⭐.

It motivates further research and development.
