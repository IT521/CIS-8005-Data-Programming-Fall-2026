# Data Profiling Summary

## Project Overview

This report summarizes the initial data profiling and quality assessment for the datasets used in the Customer Churn Analytics project.

## Telco Customer Churn

### Dataset Overview

- Rows: 7,043
- Columns: 33
- Numeric Columns: 10
- Categorical Columns: 23
- Missing Values: 5,185
- Duplicate Rows: 0

### Missing Values

- Churn Reason: 5174 missing values
- Total Charges: 11 missing values

### Data Quality Issues

- 5,185 missing values detected.

### Data Type Summary

- str: 23 columns
- int64: 6 columns
- float64: 4 columns

### Date Profiling

- No date columns identified.

### Potential Key Columns

- CustomerID

### Target Variable Analysis

- No: 5,174 (73.46%)
- Yes: 1,869 (26.54%)

### Profiling Observations

- Contains missing values that will require treatment during data cleaning.
- Contains categorical fields that may require encoding for machine learning.
- Contains numeric attributes that should be evaluated for outliers.

### Feature Engineering Candidates

- Tenure Months
- Monthly Charges
- Total Charges
- CLTV
## Retail Customer Churn

### Dataset Overview

- Rows: 5,630
- Columns: 20
- Numeric Columns: 15
- Categorical Columns: 5
- Missing Values: 1,856
- Duplicate Rows: 0

### Missing Values

- DaySinceLastOrder: 307 missing values
- OrderAmountHikeFromlastYear: 265 missing values
- Tenure: 264 missing values
- OrderCount: 258 missing values
- CouponUsed: 256 missing values
- HourSpendOnApp: 255 missing values
- WarehouseToHome: 251 missing values

### Data Quality Issues

- 1,856 missing values detected.

### Data Type Summary

- float64: 8 columns
- int64: 7 columns
- str: 5 columns

### Date Profiling

- No date columns identified.

### Potential Key Columns

- CustomerID

### Target Variable Analysis

- 0: 4,682 (83.16%)
- 1: 948 (16.84%)

### Profiling Observations

- Contains missing values that will require treatment during data cleaning.
- Contains categorical fields that may require encoding for machine learning.
- Contains numeric attributes that should be evaluated for outliers.

### Feature Engineering Candidates

- OrderCount
- CouponUsed
- CashbackAmount
- Tenure
- HourSpendOnApp
## Retail Sales and Customer Behavior

### Dataset Overview

- Rows: 1,000,000
- Columns: 78
- Numeric Columns: 40
- Categorical Columns: 38
- Missing Values: 0
- Duplicate Rows: 0

### Missing Values

- No missing values detected.

### Data Quality Issues

- No major data quality issues detected.

### Data Type Summary

- str: 38 columns
- int64: 24 columns
- float64: 16 columns

### Date Profiling

- transaction_date: 0 invalid dates
- last_purchase_date: 0 invalid dates
- product_manufacture_date: 0 invalid dates
- product_expiry_date: 0 invalid dates
- promotion_start_date: 0 invalid dates
- promotion_end_date: 0 invalid dates

### Potential Key Columns

- customer_id

### Target Variable Analysis

- No: 500,271 (50.03%)
- Yes: 499,729 (49.97%)

### Profiling Observations

- Contains categorical fields that may require encoding for machine learning.
- Contains numeric attributes that should be evaluated for outliers.

### Feature Engineering Candidates

- total_sales
- total_transactions
- online_purchases
- in_store_purchases
- customer_support_calls
- days_since_last_purchase

---

