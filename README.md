# 🏥 Healthcare Readmission Prediction System

An end-to-end healthcare analytics and machine learning project predicting 30-day hospital readmission risk for diabetic patients — from raw clinical data to risk stratification and executive reporting.

---

## 📌 Project Overview

| Detail | Info |
|--------|------|
| **Domain** | Healthcare Analytics · Predictive Modeling |
| **Dataset** | UCI Diabetes 130-US Hospitals (1999–2008) |
| **Records** | 101,766 patient admissions · 50 features |
| **Target** | 30-day hospital readmission (binary classification) |
| **Tools** | Python · Pandas · Scikit-learn · Matplotlib · Seaborn |

---

## 🎯 Business Problem

Hospital readmissions within 30 days are a major cost driver in healthcare — both financially and in patient outcomes. This project builds a predictive system to:

- Identify **which patients are at high risk** of readmission before discharge
- Surface **key clinical drivers** of readmission
- Enable **targeted interventions** to reduce preventable readmissions
- Quantify the **financial impact** of early identification

---

## 📁 Project Structure

```
healthcare-readmission-prediction/
│
├── data/
│   ├── diabetic_data.csv               # Raw dataset (download from UCI)
│   └── diabetic_data_cleaned.csv       # Preprocessed dataset
│
├── notebooks/
│   └── healthcare_readmission_analysis.ipynb   # Full pipeline notebook
│
├── visualizations/
│   ├── 01_target_distribution.png
│   ├── 02_numeric_distributions.png
│   ├── 03_categorical_distributions.png
│   ├── 04_numeric_vs_readmission.png
│   ├── 05_categorical_vs_readmission.png
│   ├── 06_correlation_matrix.png
│   ├── 07_model_comparison.png
│   ├── 08_confusion_matrices.png
│   ├── 09_feature_importance.png
│   ├── 10_probability_distribution.png
│   ├── 11_risk_stratification.png
│   └── 12_FINAL_DASHBOARD.png
│
├── EXECUTIVE_SUMMARY.txt
├── requirements.txt
└── README.md
```

---

## 🔄 Project Workflow

### Phase 1 — Data Acquisition & Setup
- Loaded the UCI Diabetes 130-US Hospitals dataset (101,766 records, ~50 features)
- Dataset covers 10 years of patient admissions across 130 US hospitals
- Features include patient demographics, diagnoses, procedures, medications, and admission details

### Phase 2 — Data Cleaning & Preprocessing
- Handled missing values across multiple clinical columns
- Encoded categorical variables (diagnosis codes, medication flags)
- Engineered features from admission type, discharge disposition, and medication changes
- Standardized numerical features using StandardScaler for model compatibility

### Phase 3 — Exploratory Data Analysis
- Univariate and bivariate analysis across all 50 features
- Identified key patterns linking readmission to medication changes, number of diagnoses, and time in hospital
- Correlation matrix analysis to detect multicollinearity
- Visualized class distribution and feature relationships

### Phase 4 — Predictive Modeling
Trained and evaluated two classifiers:

| Model | Notes |
|-------|-------|
| Logistic Regression | Baseline linear model |
| **Random Forest** | **Best performing model** |

- Random Forest outperformed Logistic Regression across all key metrics
- Feature importance analysis revealed top clinical predictors of readmission

### Phase 5 — Risk Stratification & Business Impact
- Segmented patients into High / Medium / Low risk tiers based on predicted probabilities
- **11.16% of patients** identified as high readmission risk
- Random Forest correctly identified **865 true high-risk patients**
- Estimated net benefit of early intervention: **$4,644,500** in prevented readmission costs

---

## 📊 Key Results

| Metric | Value |
|--------|-------|
| Dataset Size | **101,766 patient records** |
| Features Used | **50 clinical features** |
| Best Model | **Random Forest** |
| High-Risk Patients Identified | **865 true positives** |
| Readmission Rate in Dataset | **11.16%** |
| Estimated Net Benefit | **$4,644,500** |
| Visualizations Produced | **12** |

---

## 📈 Visualizations

The pipeline produces 12 publication-ready visualizations:

- Target class distribution
- Numerical and categorical feature distributions
- Feature vs. readmission bivariate plots
- Correlation heatmap
- Model performance comparison
- Confusion matrices (Logistic Regression vs. Random Forest)
- Feature importance chart
- Risk probability distribution
- Patient risk stratification plot
- Final executive dashboard

---

## 💡 Clinical Insights

1. **Medication changes** at discharge are strongly associated with readmission risk — patients with adjusted medications show higher probability of return
2. **Number of diagnoses** and **time in hospital** are among the strongest predictors of 30-day readmission
3. **High-risk patients** (11.16%) represent a disproportionate share of readmission burden — targeted discharge planning for this group offers the highest ROI
4. Early identification of 865 true high-risk patients enables proactive care coordination before discharge

---

## 🛠️ Tech Stack

- **Python 3.9+** — Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
- **Machine Learning** — Logistic Regression, Random Forest, StandardScaler, LabelEncoder
- **Evaluation** — ROC-AUC, Precision, Recall, F1-Score, Confusion Matrix
- **Environment** — Google Colab / Jupyter Notebook
- **Version Control** — Git & GitHub

---

## 📂 Dataset

**Source:** UCI Machine Learning Repository
**Link:** [Diabetes 130-US Hospitals Dataset](https://archive.ics.uci.edu/ml/datasets/diabetes+130-us+hospitals+for+years+1999-2008)

> Note: Download the dataset separately from UCI and place `diabetic_data.csv` in the `data/` folder before running the notebook.

---

## 👩‍💻 Author

**Indu Singh**
[LinkedIn](https://www.linkedin.com/in/indu-singh-458929365) · [GitHub](https://github.com/iamindusinghds)
