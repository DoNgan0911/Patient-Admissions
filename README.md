# Health Admission Outcome Analysis and Prediction

This project focuses on analyzing and predicting hospital admission outcomes based on patient data. The workflow includes data preprocessing, exploratory data analysis, feature engineering, handling class imbalance, and applying various classification models.

## 📂 Dataset
The dataset used in this project contains hospital admission records with various patient information such as:
- Age, Gender, Region (Urban/Rural)
- Type of Admission (Emergency/OPD)
- Lifestyle Factors: Smoking, Alcohol
- Medical Conditions: Diabetes (DM), Hypertension (HTN), Chronic Kidney Disease (CKD), etc.
- BNP levels, Anaemia, Acute Coronary Syndrome (ACS), Heart Failure, etc.
- Outcome (Target Variable): `DISCHARGE`, `EXPIRY`, or `DAMA`

> **Note:** The dataset has been cleaned by:
- Removing irrelevant columns.
- Handling missing values in the `BNP` feature.
- Encoding categorical variables.

## 🔍 Exploratory Data Analysis (EDA)
Key steps:
- Distribution analysis (boxplots, histograms).
- Outlier detection using IQR method.
- Correlation matrix (heatmap).
- Chi-squared tests between categorical variables and outcome.
- Violin plots and bar plots for visual comparison.

## ⚙️ Data Preprocessing
- One-Hot/Label Encoding for categorical variables.
- Feature scaling (if necessary).
- Class imbalance handled using:
  - **Tomek Links** (Undersampling)
  - **SMOTENC** (Oversampling for categorical + numerical data)

## 🧠 Models Used
We tested several models to predict the outcome:
1. **Decision Tree Classifier**
2. **Random Forest Classifier**
3. **Support Vector Machine (SVM)**
4. **XGBoost Classifier**

### Performance Metric:
- Precision, Recall, F1-Score, and Accuracy.

## 📈 Model Comparison Summary
| Model         | Accuracy |
|---------------|----------|
| Decision Tree | 74%      |
| Random Forest | 81%      |
| SVM           | 54%      |
| XGBoost       | 78%      |

**Random Forest** achieved the best performance.
