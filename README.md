# Loan Default Risk – Exploratory Data Analysis (EDA)
## Project Overview

This project focuses on performing Exploratory Data Analysis (EDA) on a consumer lending dataset to identify key drivers of loan default (Charge Off).
The analysis is designed from a pre-approval risk perspective, with the objective of understanding borrower characteristics and loan attributes that contribute to higher default risk.

The study combines data cleaning, feature engineering, univariate, bivariate, and multivariate analysis to derive actionable insights for credit risk assessment.

## Business Objective

-Identify pre-loan approval factors that influence loan default

-Understand borrower behaviour patterns linked to credit risk

-Support data-driven lending decisions and risk mitigation strategies

## Dataset Description

Source: Lending loan dataset (CSV format)

Dataset Link:  https://docs.google.com/spreadsheets/d/1CEr_xj8NYEhyw43hjOhPuzh0b7lF009e7OgWNL6P6MU/edit?usp=drive_link

Target Variable: loan_status

Fully Paid

Charged Off

Current (removed from analysis)

Only Fully Paid and Charged Off loans are considered to ensure clear outcome-based analysis.

## Tools & Technologies

Python

Libraries:

Pandas, NumPy – data manipulation

Matplotlib, Seaborn – data visualization

## Techniques:

Exploratory Data Analysis

Feature Engineering

Statistical Summarisation

Data Visualization

## Key Steps in Analysis
### 1. Data Understanding & Initial Exploration

Identified numerical and categorical variables

Analysed target variable distribution

Removed irrelevant loan status (Current) to focus on final outcomes

### 2. Data Cleaning & Feature Reduction

Removed:

Features with >30% missing values

Categorical and numerical features with single unique values

Post-loan approval features that cause data leakage

Retained only pre-approval, decision-impacting features

### 3. Feature Engineering

Converted percentage-based features (int_rate, revol_util) to numeric

Derived:

issue_year

issue_month

Bucketed continuous variables for deeper behavioural analysis:

Loan Amount

Interest Rate

Annual Income

Installment Amount

### 4. Missing Value Treatment

Applied mode imputation for low-cardinality categorical features

Used median imputation for skewed numerical variables

Ensured zero missing values before analysis

### 5. Univariate Analysis

Analysed distributions of:

Loan amount

Interest rate

Annual income

Loan tenure

Borrowing trends by year and month

High-risk loan purposes

### 6. Bivariate Analysis

Focused specifically on Charged Off loans to identify risk drivers:

Employment length vs default

Loan amount vs home ownership

Interest rate vs loan purpose

Loan grade vs default amount

Verification status vs loan behaviour

### 7. Multivariate Analysis

Correlation heatmap to identify strong feature relationships

Pair plots to understand interaction effects

Swarm plots to observe borrower segmentation patterns

## Key Insights & Findings
Major Drivers of Loan Default

High interest rates combined with longer employment tenure (10+ years)

Loan amounts greater than ₹12,000 for:

Debt consolidation

Credit cards

Small business loans

Higher default rates for:

Grades E, F, G

Loans with interest rates >13%

Longer tenure loans (60 months) show:

Higher interest rates

Increased charge-off probability

Installments above ₹800 with high interest significantly increase risk

## Business Recommendations

Strengthen risk checks for:

High-interest, long-tenure loans

Lower credit grades (E–G)

Re-evaluate pricing strategies for high-risk loan purposes

Enhance verification requirements for mid-range loan amounts

Use bucket-based monitoring for early risk detection

## Conclusion

This EDA provides a structured, data-driven understanding of loan default behaviour, highlighting key borrower and loan attributes that influence credit risk.
