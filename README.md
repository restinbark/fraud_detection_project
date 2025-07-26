# 🛡️ Fraud Detection Project

A supervised machine learning project designed to detect fraudulent activity using multiple datasets including transactional data, IP geolocation, and anonymized credit card usage records. This project follows a structured pipeline from data cleaning to model interpretability using SHAP.

---

## 📁 Project Structure

fraud_detection_project/
│
├── data/ # Raw datasets
├── outputs/
│ └── figures/ # Saved plots (EDA, models, SHAP)
│ └── data/ # Preprocessed CSVs (used in training)
├── notebooks/
│ ├── task_1_eda.ipynb # EDA + preprocessing
│ ├── task_2_modeling.ipynb # Model training and evaluation
│ ├── task_3_shap.ipynb # Interpretability
├── models/ # Trained model files
├── requirements.txt
└── README.md # Project documentation

yaml


---

## ✅ Objectives

- Analyze transactional behavior to detect fraud
- Train and evaluate models (Logistic Regression, Random Forest, XGBoost)
- Use SHAP to interpret model decisions
- Recommend the best model for deployment

---

## 🔍 Task 1: Data Profiling, Cleaning & EDA

### 🧹 Data Cleaning
- Merged transactional data with IP address geolocation.
- Handled missing values and converted data types.
- Engineered time-based features (e.g., `signup_hour`, `time_diff`).

### 📊 Univariate & Bivariate Plots

| Plot Title                    | Preview |
|------------------------------|---------|
| Age Distribution             | ![Age Distribution](outputs/figures/age_distribution.png) |
| Purchase Value vs Age        | ![Purchase Value vs Age](outputs/figures/purchase_vs_age.png) |
| Time Difference Distribution | ![Time Difference](outputs/figures/time_diff_distribution.png) |

---

## 🤖 Task 2: Model Training & Evaluation

### 🧠 Models Trained
- Logistic Regression
- Random Forest
- XGBoost

### 📈 Model Evaluation Metrics

| Model              | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|-------------------|----------|-----------|--------|----------|---------|
| LogisticRegression| 0.73     | 0.19      | 0.59   | 0.29     | 0.70    |
| Random Forest      | 0.95     | 0.82      | 0.53   | 0.65     | 0.77    |
| XGBoost            | 0.95     | 0.91      | 0.53   | 0.67     | 0.76    |

### 🧾 Model Visualizations

#### Logistic Regression
- ![Logistic Confusion Matrix](outputs/figures/logistic_confusion_matrix.png)
- ![Logistic ROC](outputs/figures/logistic_roc_curve.png)

#### Random Forest
- ![RF Confusion Matrix](outputs/figures/rf_confusion_matrix.png)
- ![RF ROC](outputs/figures/rf_roc_curve.png)

#### XGBoost
- ![XGBoost Confusion Matrix](outputs/figures/xgb_confusion_matrix.png)
- ![XGBoost ROC](outputs/figures/xgb_roc_curve.png)

---

## 🌐 Task 3: Model Interpretability with SHAP

- Applied SHAP to interpret XGBoost predictions.
- Identified most influential features driving fraud classification.

### 📊 SHAP Visualizations

| Plot Type        | Description               | Preview |
|------------------|---------------------------|---------|
| Global Summary   | Top features globally     | ![SHAP Bar](outputs/figures/shap_global_bar_plot.png) |
| Beeswarm         | Feature value influence   | ![Beeswarm](outputs/figures/shap_beeswarm_plot.png) |
| Waterfall        | Single prediction explainer| ![Waterfall](outputs/figures/shap_waterfall_plot.png) |

---

## 📌 Final Recommendation

📦 **Recommended Model: XGBoost**

- Best precision among all
- Balanced tradeoff between recall and accuracy
- Highly interpretable via SHAP

---

## 📚 Requirements

Install all required libraries:

```bash
pip install -r requirements.txt

👨‍💻 Author
Barkilign Mulatu | @restinbark
