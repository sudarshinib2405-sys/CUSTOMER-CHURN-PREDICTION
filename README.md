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
## 🔮 Future Improvements
- Implement advanced models like XGBoost, LightGBM, and CatBoost for better performance  
- Perform feature selection using techniques like Recursive Feature Elimination (RFE)  
- Apply cross-validation strategies like Stratified K-Fold for more robust evaluation  
- Tune decision threshold based on business requirements (precision vs recall trade-off)  
- Add model explainability using SHAP or LIME  
- Build a real-time prediction API using Flask or FastAPI  
- Develop an interactive dashboard using Streamlit for user-friendly predictions  
- Deploy the model on cloud platforms (AWS / Azure / GCP)  
- Automate the ML pipeline using tools like MLflow or Airflow  
- Monitor model performance and retrain periodically with new data  

---

## 👩‍💻 Author
**Sudarshini**  
B.Tech Artificial Intelligence and Data Science  
Kumaraguru College of Technology  

📌 Interests: Machine Learning, Computer Vision, AI for Robotics  
📌 Tools: Python, Scikit-learn, Pandas, NumPy, OpenCV  
