# Loan Approval Prediction

## Overview
This project predicts whether a loan application will be approved or rejected using machine learning.  
It uses demographic, financial, and loan-specific information to help financial institutions automate and improve decision-making in the loan approval process.

The project addresses common challenges such as missing values, class imbalance, and outliers, and achieves high predictive accuracy using a Random Forest Classifier.

---

## Dataset
The dataset contains 614 loan applications with the following features:

| Feature              | Description |
|----------------------|-------------|
| Gender               | Male / Female |
| Married              | Applicant’s marital status |
| Dependents           | Number of dependents |
| Education            | Graduate / Not Graduate |
| Self_Employed        | Yes / No |
| ApplicantIncome      | Applicant’s income |
| CoapplicantIncome    | Co-applicant’s income |
| LoanAmount           | Loan amount in thousands |
| Loan_Amount_Term     | Loan term in days |
| Credit_History       | Credit history meets guidelines (1 = Yes, 0 = No) |
| Property_Area        | Urban / Semi-Urban / Rural |
| Loan_Status          | Target variable (Y = Approved, N = Rejected) |

Dataset file: `Loan_Approval_Dataset.xlsx`

---

## Data Preprocessing
- Missing values handled via mean/median imputation for numerical features and mode imputation for categorical features.
- Outlier detection performed using boxplots and managed with transformations to reduce skewness.
- Feature engineering:
  - Created a new feature `Total_Income` by summing ApplicantIncome and CoapplicantIncome.
  - Applied log transformation to reduce skewness in income and loan amount features.
- Categorical variables encoded using Label Encoding.
- Class imbalance addressed through Random Oversampling.

---

## Models Used
1. Logistic Regression – baseline model for interpretability.
2. Decision Tree Classifier – captures non-linear relationships.
3. Random Forest Classifier – ensemble model that reduces overfitting and improves accuracy.
4. K-Nearest Neighbors (KNN) – distance-based classification method.

---

## Model Performance

| Model               | Accuracy (Imbalanced) | Accuracy (Balanced) |
|--------------------|----------------------|---------------------|
| Logistic Regression | 77.27%               | 69.67%              |
| Decision Tree       | 70.13%               | 79.62%              |
| Random Forest       | 79.22%               | 88.63%              |
| KNN                 | 71.43%               | 71.43%              |

---
