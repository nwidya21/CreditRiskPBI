# Credit Risk Prediction Project

## Project Overview
This project aims to develop a machine learning model to predict **credit risk** for a multifinance company. The goal is to improve the accuracy of assessing and managing credit risk, enabling better business decisions and reducing potential losses. The dataset includes data on approved and rejected loans, with detailed borrower and loan attributes.

---

## Problem Statement
The client wants to optimize their decision-making process in granting loans by accurately predicting credit risk. This involves classifying loans based on their likelihood of default using historical data, including borrower income, credit history, and loan details.

---

## Dataset
The dataset contains **466,285 entries** with **75 columns** in the raw data, which include:
- Borrower demographics (e.g., employment length, annual income)
- Loan details (e.g., loan amount, interest rate, term)
- Credit history (e.g., number of delinquencies, revolving credit utilization)

### Target Variable
- `loan_status`: Indicates the current status of the loan, with the following categories:
  - 'Fully Paid', 'Charged Off', 'Current', 'Default', 'In Grace Period', 'Late (16-30 days)', 'Late (31-120 days)', 'Does not meet the credit policy. Status: Fully Paid', 'Does not meet the credit policy. Status: Charged Off'

### Selected Features
The following features were chosen for modeling as they capture critical financial, credit, and loan-specific factors:
- **`annual_inc`**: Borrower’s annual income.
- **`emp_length_encoded`**: Encoded employment length indicating financial stability.
- **`loan_amnt`**: Loan amount requested.
- **`term_encoded`**: Encoded loan repayment term (e.g., 36 or 60 months).
- **`grade_encoded`**: Encoded loan grade representing borrower creditworthiness.
- **`total_rec_prncp`**: Total principal received to date.
- **`total_rec_int`**: Total interest received to date.
- **`last_pymnt_amnt`**: Amount paid in the last installment.
- **`delinq_2yrs`**: Number of delinquencies in the past 2 years.
- **`revol_util`**: Revolving credit utilization rate.
- **`loan_to_income`**: Loan-to-income ratio, representing debt burden relative to income.
- **`dti_recalculated`**: Recalculated debt-to-income ratio, assessing whether the borrower can manage additional debt.

### Feature Engineering
- **Loan-to-Income Ratio**: Calculated as `loan_amnt / annual_inc` to measure debt burden relative to income.
- **Recalculated DTI**: Updated debt-to-income ratio for improved assessment.

---

## Methodology
1. **Data Understanding**:
   - Exploratory Data Analysis (EDA) was performed to identify trends and correlations.
2. **Data Preparation**:
   - Null values were handled, and unnecessary columns were removed.
   - Features were selected and engineered to enhance model performance.
3. **Modeling**:
   - Four machine learning algorithms were evaluated: Random Forest, Gradient Boosting, Decision Tree, and Logistic Regression.
   - **Random Forest** was chosen as the best-performing model.
4. **Evaluation**:
   - Models were evaluated using **ROC AUC** as the primary metric.

---

## Results
- The **Random Forest** model achieved an impressive **ROC AUC score of 97%** on the test set, demonstrating excellent performance in distinguishing between different credit risk levels.
- This result indicates that the model can reliably predict credit risk, supporting the client's decision-making process.

---

## Conclusion
This project successfully developed a machine learning model to predict credit risk with high accuracy. By leveraging advanced features and robust evaluation metrics, the model provides valuable insights into loan approval and risk management strategies.

---


