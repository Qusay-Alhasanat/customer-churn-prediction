# Data Dictionary – Customer Churn Analysis Project

## Project Purpose
This data dictionary documents the key variables used in the customer churn analysis project.
The goal is to identify which customers are likely to churn and understand the main factors influencing churn behavior.

---

## 🎯 Target Variable

| Column Name | Data Type | Description | Usage Decision | Reason |
|------------|----------|-------------|----------------|--------|
| Churn Label | Categorical | Indicates whether the customer has churned (Yes / No) | Target | This is the main outcome the model aims to predict |

---

## 👤 Customer Demographics

| Column Name | Data Type | Description | Usage Decision | Reason |
|------------|----------|-------------|----------------|--------|
| Gender | Categorical | Gender of the customer | Included | May influence service preferences and churn behavior |
| Age | Numerical | Age of the customer | Included | Age often correlates with usage patterns and loyalty |
| Under 30 | Categorical | Indicates whether the customer is under 30 years old | Included | Helps capture churn trends among younger customers |
| Senior Citizen | Categorical | Indicates whether the customer is a senior citizen | Included | Senior customers may have different churn drivers |
| Married | Categorical | Indicates whether the customer is married | Included | Family status can affect service stability |
| Dependents | Categorical | Indicates whether the customer has dependents | Included | Customers with dependents tend to have lower churn |
| Number of Dependents | Numerical | Number of dependents | Included | Provides more granular insight than a binary indicator |

---

## 📄 Subscription & Relationship Information

| Column Name | Data Type | Description | Usage Decision | Reason |
|------------|----------|-------------|----------------|--------|
| Tenure in Months | Numerical | Number of months the customer has stayed with the company | Included | One of the strongest indicators of churn risk |
| Contract | Categorical | Type of contract (Monthly, One Year, Two Year) | Included | Short-term contracts are usually associated with higher churn |
| Offer | Categorical | Promotional offers applied to the customer | Included | Promotions may impact customer retention |
| Referred a Friend | Categorical | Indicates whether the customer referred a friend | Included | Referral behavior suggests higher engagement |
| Number of Referrals | Numerical | Number of customers referred | Included | Measures customer loyalty and advocacy |

---

## 💸 Charges & Usage Metrics

| Column Name | Data Type | Description | Usage Decision | Reason |
|------------|----------|-------------|----------------|--------|
| Monthly Charge | Numerical | Monthly billing amount | Included | High monthly costs can increase churn probability |
| Total Charges | Numerical | Total amount charged to the customer | Included | Reflects long-term customer value |
| Avg Monthly GB Download | Numerical | Average monthly internet usage in GB | Included | Usage patterns often correlate with satisfaction |
| Total Revenue | Numerical | Total revenue generated from the customer | Included | Indicates customer importance to the business |

---

## 🚫 Excluded Variables

| Column Name | Reason for Exclusion |
|------------|---------------------|
| Customer ID | Unique identifier with no analytical value |
| Country | Geographical identifier not relevant to churn behavior |
| State | Location-based information excluded to avoid noise |
| City | High-cardinality categorical variable with limited insight |
| Zip Code | Identifier with no behavioral meaning |
| Latitude | Geospatial data not required for this analysis |
| Longitude | Geospatial data not required for this analysis |
| Churn Score | Calculated after churn occurred (data leakage risk) |
| Churn Category | Available only after the churn event |
| Churn Reason | Post-churn information not available at prediction time |
| Customer Status | Directly reflects the final churn outcome |
| CLTV | Pre-calculated metric that could bias the model |

---

## Notes
- Only variables available **before** churn occurs are included in the predictive modeling phase.
- Excluded variables are still useful for **post-analysis interpretation** but are not used as model features.
- This structured selection helps prevent data leakage and ensures realistic model performance.
