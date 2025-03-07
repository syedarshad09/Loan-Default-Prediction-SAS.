# Loan Default Prediction Analysis

## Business Question
The goal of this project is to analyze loan default data to identify key factors influencing loan defaults and build a predictive model for interest rates based on credit scores. The insights can help financial institutions make better lending decisions.

## Dataset
The dataset (`Loan_default.csv`) contains the following variables:
- `LoanID`: Unique identifier for each loan.
- `Age`: Age of the borrower.
- `Income`: Income of the borrower.
- `LoanAmount`: Amount of the loan.
- `MaritalStatus`: Marital status of the borrower.
- `LoanTerm`: Duration of the loan.
- `LoanPurpose`: Purpose of the loan.
- `InterestRate`: Interest rate on the loan.
- `HasMortgage`: Whether the borrower has a mortgage.
- `HasDependents`: Whether the borrower has dependents.
- `HasCoSigner`: Whether the loan has a co-signer.
- `EmploymentType`: Type of employment.
- `Education`: Education level of the borrower.
- `DTIRatio`: Debt-to-income ratio.
- `Default`: Whether the loan defaulted (1 = Yes, 0 = No).
- `CreditScore`: Credit score of the borrower.
- `MonthsEmployed`: Number of months employed.
- `NumCreditLines`: Number of credit lines.

## Methodology
1. **Data Preparation**:
   - Renamed variables for clarity.
   - Checked for missing values and duplicates.
   - Created a new variable `default_status` to categorize loan defaults.
2. **Descriptive Analysis**:
   - Used `PROC MEANS` and `PROC FREQ` to summarize the data.
3. **Modeling**:
   - Split the data into 70% training and 30% testing sets.
   - Performed correlation analysis between `credit_score` and `interest_rate`.
   - Built a simple linear regression model to predict `interest_rate` based on `credit_score`.

## Insights
- **Key Findings**:
  - The correlation between `credit_score` and `interest_rate` is weak, indicating other factors may influence interest rates.
  - Descriptive statistics revealed that most borrowers have a high credit score and a low debt-to-income ratio.
- **Recommendations**:
  - Financial institutions should consider additional variables (e.g., income, loan purpose) when setting interest rates.
  - Further analysis using advanced models (e.g., logistic regression) could improve default prediction.

