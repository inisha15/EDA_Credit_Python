# Credit_EDA_Project

📊 Credit Risk Analysis – Exploratory Data Analysis (EDA)

🔹 Problem Statement 
Financial institutions need to identify whether a customer is likely to face payment difficulties (loan default).
The objective of this project is to analyze customer data and uncover patterns, trends, and risk factors that influence credit default behavior.

🔹 Objective 
Understand the distribution of target variable (default vs non-default)
Identify key drivers of payment difficulty
Perform data cleaning, transformation, and visualization
Generate actionable business insights for credit risk assessment

🔹 Dataset Description 
This project uses two datasets:

📁 Application Data
Contains:
Customer demographics (Gender, Family status, Housing type)
Financial details (Income, Credit, Annuity)
Social & regional attributes

📁 Previous Application Data
Contains:
Past loan applications
Loan status (Approved/Rejected)
Rejection reasons

🔹 Data Preprocessing 
🧹 Missing Value Treatment
Columns with >50% missing values removed
Important features retained:
EXT_SOURCE_2, EXT_SOURCE_3
AMT_CREDIT, AMT_ANNUITY, etc.
❌ Data Cleaning
Removed invalid category: CODE_GENDER = XNA
Checked duplicates & inconsistencies

🔹 Feature Engineering ⚙️ 
Created meaningful categories to simplify analysis:

Income Class
<50K, 50K–100K, 100K–150K, etc.
Credit Amount Class
<5 Lakhs, 5–10 Lakhs, etc.
Annuity Class
Bucketed into ranges
Goods Price Class

👉 This helped in better interpretation of trends.

🔹 Outlier Treatment 📉 
Used IQR (Interquartile Range) Method:
AMT_INCOME_TOTAL
AMT_ANNUITY

✔ Reduced extreme values
✔ Improved skewness (from ~391 → ~0.78)

🔹 Exploratory Data Analysis (EDA) 
🔸 Target Variable Analysis
Default rate ≈ 8.07%
Dataset is highly imbalanced
🔸 Categorical Analysis (Bivariate)

Used crosstab + percentage analysis

👤 Gender vs Default
Male default rate > Female
👶 Children vs Default
More children → higher default risk
🚗 Car Ownership
Car owners → slightly lower risk
🏠 Realty Ownership
Minor variation in default rate
💼 Income Type
Working class → higher defaults
Pensioners → lower risk
🎓 Education
Lower education → higher default probability
👪 Family Status
Singles & separated → relatively higher risk
🏡 Housing Type
Rented / living with parents → higher risk
🔸 Numerical Analysis
💰 Income
Highly skewed distribution
Lower income → higher default
💳 Credit Amount
Higher credit → increased risk
📆 Annuity
Higher annuity → higher default probability
🏷 Goods Price
Similar trend as credit amount

🔹 Visualizations 📊 
Pie Chart → Target distribution
Bar Plots → Category vs Default %
Histograms → Distribution
Boxplots → Outlier detection

🔹 Key Insights 📌
⚠ Default rate is low but significant (~8%)
👨 Males are riskier than females
👶 Dependents increase financial burden → higher risk
💸 Low income group is most vulnerable
💳 High loan & EMI → strong default indicators
🎓 Education & occupation impact repayment ability
🏠 Living conditions also influence credit behavior

🔹 Business Recommendations 💡
📊 Focus more on low-income applicants
⚖ Apply stricter checks for high credit + high annuity
👨‍👩‍👧 Consider family size in risk evaluation
🎯 Use these features in credit scoring models

🔹 Future Scope 🚀
Feature scaling & encoding
Machine Learning models:
Logistic Regression
Random Forest
XGBoost
Model evaluation:
ROC-AUC
Precision-Recall
Handle class imbalance (SMOTE, etc.)

🔹 Project Structure
📁 Credit-EDA
│── application_data.csv
│── previous_application.csv
│── EDA_Credit.ipynb
│── README.md
│── images/

🔹 How to Run ▶️
pip install pandas numpy matplotlib seaborn scipy
jupyter notebook

🔹 Author 👩‍💻

Nisha

"This project performs Exploratory Data Analysis (EDA) on a Credit dataset using Python. It includes data cleaning, handling missing values, outlier detection, and visualization using libraries like Pandas, Matplotlib, and Seaborn. The goal is to understand patterns, relationships, and key factors affecting credit behavior."
