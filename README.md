# Risk Alert Classifier: Predicting High-Risk Customers Using Machine Learning

## Project Overview

This project develops a machine learning-based Risk Alert Classifier to identify high-risk customers using demographic, financial, and behavioral data. The objective is to help financial institutions proactively detect risky customers, reduce default risk, and improve decision-making.

---

## Problem Statement

Financial institutions need a reliable system to identify customers who may become financially risky. Predicting these customers early helps minimize financial losses and supports better risk management.

The goal is to classify customers into:

- Low Risk (0)
- High Risk (1)

---

## Dataset Information

### Dataset Size

- Total Records: 4600
- Total Features: 19

### Features

- customer_id
- age
- gender
- region
- employment_type
- annual_income_inr
- credit_score
- credit_utilization_ratio
- missed_payments_12m
- avg_late_payment_days
- monthly_transaction_count
- monthly_spend_inr
- cash_advance_count_6m
- complaints_last_6m
- failed_login_attempts_3m
- account_tenure_months
- last_transaction_date
- debt_balance_inr
- risk_status

### Target Variable

- 0 = Low Risk
- 1 = High Risk

---

## Project Workflow

### Phase 1: Data Cleaning

#### Missing Value Treatment
- SimpleImputer
- Median strategy for numerical columns
- Most Frequent strategy for categorical columns

#### Outlier Treatment
- IQR-based detection
- Winsorization applied to cap extreme values

#### Feature Scaling
- StandardScaler

Output:
- Risk_Alert_Classifier_Cleaned.csv

---

### Phase 2: Exploratory Data Analysis (EDA)

Performed:
- Univariate Analysis
- Bivariate Analysis
- Multivariate Analysis
- Correlation Analysis
- Class Distribution Analysis
- Outlier Visualization

Key Findings:
- Dataset is imbalanced.
- High-risk customers generally have lower credit scores.
- High-risk customers tend to have more missed payments.
- Debt balance and credit utilization are strong risk indicators.

---

### Phase 3: Baseline Model

#### Logistic Regression

Metrics:
- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

Purpose:
- Establish baseline performance.

---

### Phase 4: Imbalanced Data Handling

Techniques Applied:

#### Random Under Sampling
Balances classes by reducing majority-class observations.

#### Random Over Sampling
Balances classes by duplicating minority-class observations.

#### SMOTE
Creates synthetic minority-class samples.

#### ADASYN
Generates adaptive synthetic samples for difficult cases.

---

### Phase 5: Tree-Based Models

#### Decision Tree
- Model Training
- Evaluation
- Tree Visualization
- Feature Importance

#### Random Forest
- Model Training
- Evaluation
- Feature Importance Analysis

---

### Phase 6: Hyperparameter Tuning

#### Decision Tree
- RandomizedSearchCV

#### Random Forest
- GridSearchCV

Optimized Parameters:
- max_depth
- criterion
- n_estimators
- min_samples_split
- min_samples_leaf

---

### Phase 7: ROC-AUC Analysis

Generated ROC Curves for:
- Logistic Regression
- Decision Tree
- Random Forest

Evaluation Metric:
- ROC-AUC Score

---

## Technologies Used

### Programming Language
- Python

### Libraries
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Imbalanced-Learn
- SciPy

### Development Environment
- Jupyter Notebook
- VS Code

---

## Project Structure

Risk_Alert_Classifier/

├── 01_Data_Cleaning_EDA.ipynb
├── 02_Logistic_Regression.ipynb
├── 03_Imbalance_Handling.ipynb
├── 04_DecisionTree_RandomForest.ipynb
├── 05_Hyperparameter_Tuning.ipynb
├── 06_ROC_AUC_Analysis.ipynb
├── 07_Final_Report.ipynb
├── Risk_Alert_Classifier_Dataset.csv
├── Risk_Alert_Classifier_Cleaned.csv
├── README.md
└── Project_Report.pdf

---

## Key Business Insights

- Low credit scores strongly indicate risk.
- Frequent missed payments are major warning signals.
- High debt balances increase customer risk.
- Credit utilization ratio significantly affects risk classification.
- Complaint history contributes to risk prediction.

---

## Evaluation Metrics

### Accuracy
Overall prediction correctness.

### Precision
How many predicted high-risk customers were actually high-risk.

### Recall
How many actual high-risk customers were correctly identified.

### F1 Score
Balance between Precision and Recall.

### ROC-AUC
Ability to distinguish between risk classes.

---

## Business Impact

### Type-I Error (False Positive)
Low-risk customer predicted as high-risk.

Impact:
- Unnecessary restrictions on good customers.

### Type-II Error (False Negative)
High-risk customer predicted as low-risk.

Impact:
- Financial losses and increased default risk.

Type-II Error is more critical in this project.

---

## Final Conclusion

The project successfully developed a machine learning-based Risk Alert Classifier using financial and behavioral customer data.

The dataset was cleaned using SimpleImputer, Winsorization, and StandardScaler. Multiple classification algorithms were implemented, including Logistic Regression, Decision Tree, and Random Forest. Class imbalance was addressed using Random Under Sampling, Random Over Sampling, SMOTE, and ADASYN.

Hyperparameter tuning and ROC-AUC analysis improved model performance and reliability. Among all evaluated models, the Tuned Random Forest model achieved the best overall performance and was selected as the final predictive model.

This solution can help financial institutions proactively identify risky customers, reduce defaults, and improve risk management strategies.

---

## Author

Santosh Kumar
Machine Learning Classification Project
Risk Alert Classifier
