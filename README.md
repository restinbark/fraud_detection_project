# 🕵️‍♂️ Fraud Detection Project

This project applies machine learning to detect fraudulent transactions using anonymized user data and transactional behavior. The pipeline includes data cleaning, exploratory data analysis (EDA), model training, performance evaluation, and model interpretability using SHAP.

---

## 📁 Project Structure

fraud_detection_project/
├── data/
├── notebooks/
├── outputs/
│ └── figures/
│ └── models/
├── src/
├── requirements.txt
└── README.md


---

## 📌 Objectives

- Preprocess and analyze transactional data
- Build and evaluate fraud detection models
- Interpret model behavior using SHAP
- Recommend the best-performing model

---

## 🧪 Datasets

- `Fraud_Data.csv`
- `IpAddress_to_Country.csv`
- `creditcard.csv` (for extended modeling)

---

## 📊 Task 1 – Exploratory Data Analysis (EDA)

### 🔹 Univariate & Bivariate Plots

![Age Distribution](https://raw.githubusercontent.com/restinbark/fraud_detection_project/main/outputs/figures/age_distribution.png)  
![Purchase Value vs Age](https://raw.githubusercontent.com/restinbark/fraud_detection_project/main/outputs/figures/purchase_vs_age.png)

### 🔹 Insights

- Majority of users fall between ages 25–40
- Fraud distribution varies across device/browser/source
- Class imbalance confirmed: many more legitimate transactions than fraudulent ones

---

## ⚙️ Task 2 – Model Training & Evaluation

### 🧹 Preprocessing

- Missing value check: None
- Label encoding for categorical variables
- SMOTE applied to address class imbalance

### 🔍 Models Trained

- Logistic Regression
- Random Forest
- XGBoost

### 📈 Performance Comparison

| Model               | Accuracy | Precision | Recall | F1-score | ROC AUC |
|---------------------|----------|-----------|--------|----------|---------|
| Logistic Regression | 0.73     | 0.19      | 0.59   | 0.29     | 0.70    |
| Random Forest       | 0.95     | 0.82      | 0.53   | 0.65     | 0.77    |
| XGBoost             | 0.95     | 0.91      | 0.53   | 0.67     | 0.76    |

> ✅ **XGBoost** performed best in terms of precision and F1-score — critical for fraud detection where false negatives are costly.

---

## 🧠 Task 3 – Model Interpretability (SHAP)

### 🔹 SHAP Plots

![SHAP Beeswarm](https://raw.githubusercontent.com/restinbark/fraud_detection_project/main/outputs/figures/shap_beeswarm_plot.png)  
![SHAP Global Bar Plot](https://raw.githubusercontent.com/restinbark/fraud_detection_project/main/outputs/figures/shap_global_bar_plot.png)  
![SHAP Waterfall](https://raw.githubusercontent.com/restinbark/fraud_detection_project/main/outputs/figures/shap_waterfall_plot.png)

### 🔹 SHAP Insights

- Age, browser type, and IP address range significantly influence fraud predictions.
- SHAP confirms that engineered features such as device ID frequency also play a strong role.

---

## ✅ Final Recommendation

We recommend deploying the **XGBoost model** for fraud detection due to its:

- High **precision** (91%) — reducing false positives
- Balanced **recall** and **F1-score**
- Interpretability with SHAP for transparent decision-making

---

## 📦 Requirements

```bash
pip install -r requirements.txt

👨‍💻 Author
Barkilign Mulatu 