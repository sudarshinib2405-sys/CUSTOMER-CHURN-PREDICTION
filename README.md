# 🏦 Bank Customer Churn Prediction

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![ML](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 📌 Overview
This project builds a complete **Machine Learning pipeline** to predict whether a bank customer will churn.  

It covers:
- Data preprocessing  
- Exploratory Data Analysis (EDA)  
- Feature engineering  
- Model training & tuning  
- Evaluation and optimization  

---

## 📂 Dataset
- Source: Kaggle  
- Dataset: Bank Customer Churn Prediction  
- File: `Churn_Modelling.csv`

### Features
- Demographics: Age, Gender, Geography  
- Financial: Balance, Credit Score, Salary  
- Account Info: Tenure, Products, Activity  
- Target: `Exited` (0 = Stayed, 1 = Churned)

---

## ⚙️ Tech Stack
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- Imbalanced-learn (SMOTE)  
- Joblib  

---

## 🔄 ML Pipeline

### 🧹 Data Preprocessing
- Dropped irrelevant columns  
- Handled missing values  
- One-hot encoding  
- Feature scaling  

### 📊 EDA
- Target distribution (imbalanced dataset)  
- Correlation heatmap  
- Feature relationships  

### 📈 Statistical Testing
- Chi-Square Test (categorical)  
- T-Test (numerical)  

### 🚀 Feature Engineering
- BalanceSalaryRatio  
- AgeTenureRatio  
- ProductsPerTenure  
- Balance_to_Credit  
- Active_Balance  
- EngagementScore  
- AgeGroup  
- TenureGroup  
- Salary_per_Product  

### ⚖️ Handling Imbalance
- SMOTE (Synthetic Oversampling)

### 🤖 Model
- Random Forest Classifier  
- Pipeline: Preprocessing → SMOTE → Model  

### 🔧 Hyperparameter Tuning
- RandomizedSearchCV  
- 5-fold Cross Validation  
- Optimized for F1-score  

---

## 📊 Model Performance

| Metric    | Score |
|----------|------|
| Accuracy | 0.8265 |
| Precision | 0.559 |
| Recall | 0.695 |
| F1 Score | 0.619 |
| ROC-AUC | 0.858 |

---

## 🎯 Key Insights
- Dataset is imbalanced (~80% non-churn, ~20% churn)  
- Age, Balance, and Geography strongly influence churn  
- Feature engineering significantly improved performance  
- SMOTE improved recall for churn prediction  

---

## 🔍 Model Comparison

| Model                | Accuracy | Precision | Recall | F1-score |
|---------------------|---------|----------|--------|---------|
| Logistic Regression | 0.714   | 0.39     | 0.73   | 0.51    |
| Random Forest       | 0.866   | 0.80     | 0.45   | 0.57    |

---

## 💾 Model Usage

```python
import joblib
model = joblib.load("bank_churn_model.pkl")
