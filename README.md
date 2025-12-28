# Customer Churn Prediction – Telecom Dataset

## Project Overview
Customer churn is a critical challenge for subscription-based businesses.
This project analyzes customer behavior and builds a machine learning model
to predict whether a customer is likely to churn.

The project follows a complete data science workflow:
data cleaning, exploratory data analysis, feature engineering, modeling,
and business-driven conclusions.

---

## Project Structure
- `data/`: Raw and processed datasets  
- `notebooks/`: Step-by-step data science workflow  
- `reports/`: Documentation and data dictionary  
- `visuals/`: Saved figures from exploratory analysis  

---

## Objectives
- Understand key factors influencing customer churn
- Identify behavioral and contractual patterns
- Build a predictive model to detect high-risk customers
- Support data-driven customer retention strategies

---

## Methodology

### 1. Data Cleaning
- Inspected dataset structure and data types
- Standardized column names
- Handled missing values based on business context
- Saved a clean and reproducible dataset

### 2. Exploratory Data Analysis (EDA)
- Analyzed overall churn distribution
- Studied customer tenure, pricing, contracts, services, and referrals
- Identified key churn drivers through business-focused insights

### 3. Feature Engineering
- Selected features based on EDA findings
- Encoded categorical variables
- Scaled numerical features
- Prepared model-ready datasets

### 4. Modeling
- Trained Logistic Regression models
- Evaluated both baseline and class-balanced models
- Assessed performance using:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Confusion Matrix

The balanced model was selected to better capture churned customers,
which is critical from a business perspective.

---

## Key Insights
- Customers with short tenure are more likely to churn
- Contract type has a strong influence on retention
- Promotional offers and referrals significantly reduce churn risk
- Class imbalance strongly impacts model evaluation

---

## Tools & Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Future Improvements
- Experiment with advanced models (Random Forest, XGBoost)
- Perform hyperparameter tuning
- Build an interactive dashboard for business users
- Deploy the model as a prediction service
