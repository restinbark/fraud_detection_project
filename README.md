# 🕵️‍♀️ Fraud Detection Project

This project focuses on building and interpreting machine learning models to detect fraudulent transactions using anonymized user data. The goal is to improve fraud detection accuracy and provide transparency through model interpretability tools like SHAP.

---

## 📁 Project Structure

```bash
fraud_detection_project/
│
├── data/                         # Raw data
├── notebooks/                   # Jupyter notebooks for each task
│   ├── 01_data_analysis_preprocessing.ipynb
│   ├── 02_model_building_training.ipynb
│   └── 03_shap.ipynb
│
├── outputs/
│   ├── data/                    # Cleaned & split data
│   └── figures/                 # Visualizations and plots
│
├── models/                      # Saved model files
├── README.md                    # Project summary
└── requirements.txt             # Python dependencies

📌 Task Overview
🧹 Task 1: Data Cleaning & Preprocessing
Handled missing values and duplicates

Merged IP address data with transaction data

Encoded categorical features

Addressed class imbalance using SMOTE

## 📈 Task 1 – Exploratory Data Analysis (EDA)

![Age Distribution](https://raw.githubusercontent.com/restinbark/fraud_detection_project/main/outputs/figures/age_distribution.png)
![Purchase vs Age](https://raw.githubusercontent.com/restinbark/fraud_detection_project/main/outputs/figures/purchase_vs_age.png)

---

## 🤖 Task 2 – Model Training & Evaluation

| Model            | Accuracy | Precision | Recall | F1-score | ROC AUC |
|------------------|----------|-----------|--------|----------|---------|
| Logistic Regression | 0.73     | 0.19      | 0.59   | 0.29     | 0.70    |
| Random Forest       | 0.95     | 0.82      | 0.53   | 0.65     | 0.77    |
| XGBoost             | 0.95     | 0.91      | 0.53   | 0.67     | 0.76    |

![ROC Curve](https://raw.githubusercontent.com/restinbark/fraud_detection_project/main/outputs/figures/roc_curve.png)

---

## 🧠 Task 3 – Model Interpretability with SHAP

### 📈 Univariate & Bivariate Analysis

![Age Distribution](outputs/figures/univariate_age.png)
![Purchase Value vs Age](outputs/figures/univariate_purchase_value.png)


🤖 Task 2: Model Building & Evaluation
Trained Logistic Regression, Random Forest, and XGBoost classifiers

Evaluated models on metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC

Random Forest and XGBoost showed superior performance
### 📊 Confusion Matrices

![XGBoost Confusion Matrix](outputs/figures/xgb_confusion_matrix.png)

### 🧮 ROC Curve Comparison

![ROC Curves](outputs/figures/roc_comparison.png)

📊 Task 3: Model Interpretability
Used SHAP to explain feature contributions in XGBoost

Generated beeswarm, bar, and waterfall plots for global and local interpretations

📈 Visual Results
🔹 Univariate & Bivariate Plots
![Age Distribution](https://raw.githubusercontent.com/restinbark/fraud_detection_project/master/outputs/figures/univariate_age.png)

![Class Distribution](https://raw.githubusercontent.com/restinbark/fraud_detection_project/master/outputs/figures/univariate_class_distribution.png)

![Purchase vs Age](https://raw.githubusercontent.com/restinbark/fraud_detection_project/master/outputs/figures/bivariate_purchase_value_by_class.png)



🔍 Model Evaluation Summary
| Model              | Accuracy | Precision | Recall | F1-score | ROC AUC |
| ------------------ | -------- | --------- | ------ | -------- | ------- |
| LogisticRegression | 73%      | 19%       | 59%    | 29%      | 0.70    |
| Random Forest      | 95%      | 82%       | 53%    | 65%      | 0.775   |
| XGBoost            | 95%      | 91%       | 53%    | 67%      | 0.765   |


✅ Recommended Model: XGBoost
Provides strong performance and better interpretability with SHAP

🔍 SHAP Interpretability Plots



✅ Conclusion
This project demonstrates an end-to-end ML pipeline for fraud detection:

Preprocessing, EDA, and SMOTE for class balance

Multiple model training and evaluation

Interpretation using SHAP to build trust in decisions

🚀 Future work: Streamlit dashboard and real-time fraud monitoring

📦 Requirements
bash
pip install -r requirements.

🙌 Author
Barkilign Mulatu | 
