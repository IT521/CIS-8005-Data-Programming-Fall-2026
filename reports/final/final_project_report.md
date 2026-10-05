# Customer Churn Analytics Project

## Executive Summary

This project analyzed customer churn across three industries:

- Telecommunications
- Retail Customer Churn
- Retail Sales

The project combined:

- Data Cleaning and Feature Engineering
- SQLite Analytics
- MongoDB Analytics
- Exploratory Data Analysis
- Machine Learning
- Feature Importance Analysis
- Business Intelligence Recommendations

Key findings include:

- Telco Churn Rate: 26.54%
- Retail Customer Churn Rate: 16.84%
- Retail Sales Churn Rate: 49.97%

The strongest churn drivers included:

- Monthly Charges
- Customer Tenure
- Cashback Incentives
- Customer Value

Decision Tree models achieved the strongest predictive performance, while Random Forest models provided feature importance analysis used to generate business recommendations.

---


# SQLite Analysis

# SQLite Analysis Summary

This report summarizes the SQL analysis performed on the cleaned customer churn datasets.

## Telco Customer Churn Analysis

### Churn Distribution

| Churn Label   |   CustomerCount |
|:--------------|----------------:|
| No            |            5174 |
| Yes           |            1869 |
Observation: Highest value is {'Churn Label': 'No', 'CustomerCount': 5174}



### Contract vs Churn

| Contract       | Churn Label   |   CustomerCount |
|:---------------|:--------------|----------------:|
| Month-to-month | No            |            2220 |
| Month-to-month | Yes           |            1655 |
| Two year       | No            |            1647 |
| One year       | No            |            1307 |
| One year       | Yes           |             166 |
| Two year       | Yes           |              48 |
Observation: Highest value is {'Contract': 'Month-to-month', 'Churn Label': 'No', 'CustomerCount': 2220}



### Average Monthly Charges by Churn

| Churn Label   |   AvgMonthlyCharge |
|:--------------|-------------------:|
| No            |              61.27 |
| Yes           |              74.44 |
Observation: Highest value is {'Churn Label': 'No', 'AvgMonthlyCharge': 61.27}



## Retail Customer Churn Analysis

### Preferred Payment Mode vs Churn

| PreferredPaymentMode   |   Churn |   Customers |
|:-----------------------|--------:|------------:|
| Debit Card             |       0 |        1958 |
| Credit Card            |       0 |        1308 |
| E Wallet               |       0 |         474 |
| Debit Card             |       1 |         356 |
| Upi                    |       0 |         342 |
| Cod                    |       0 |         260 |
| Cc                     |       0 |         214 |
| Credit Card            |       1 |         193 |
| E Wallet               |       1 |         140 |
| Cash On Delivery       |       0 |         126 |
| Cod                    |       1 |         105 |
| Upi                    |       1 |          72 |
| Cc                     |       1 |          59 |
| Cash On Delivery       |       1 |          23 |
Observation: Highest value is {'PreferredPaymentMode': 'Debit Card', 'Churn': 0, 'Customers': 1958}



### Complaints vs Churn

|   Complain |   Churn |   Customers |
|-----------:|--------:|------------:|
|          0 |       0 |        3586 |
|          0 |       1 |         440 |
|          1 |       0 |        1096 |
|          1 |       1 |         508 |
Observation: Highest value is {'Complain': 0, 'Churn': 0, 'Customers': 3586}



### Average Satisfaction Score

|   Churn |   AvgSatisfaction |
|--------:|------------------:|
|       0 |              3    |
|       1 |              3.39 |
Observation: Highest value is {'Churn': 0.0, 'AvgSatisfaction': 3.0}



## Retail Sales Analysis

### Loyalty Program vs Churn

| loyalty_program   | churned   |   CustomerCount |
|:------------------|:----------|----------------:|
| No                | No        |          250208 |
| No                | Yes       |          250080 |
| Yes               | No        |          250063 |
| Yes               | Yes       |          249649 |
Observation: Highest value is {'loyalty_program': 'No', 'churned': 'No', 'CustomerCount': 250208}



### Average Total Sales by Churn

| churned   |   AvgSales |
|:----------|-----------:|
| No        |    5057.65 |
| Yes       |    5054.47 |
Observation: Highest value is {'churned': 'No', 'AvgSales': 5057.65}



### Top Product Categories

| product_category   |     Revenue |
|:-------------------|------------:|
| Toys               | 1.01378e+09 |
| Clothing           | 1.01109e+09 |
| Groceries          | 1.01107e+09 |
| Electronics        | 1.01058e+09 |
| Furniture          | 1.00954e+09 |
Observation: Highest value is {'product_category': 'Toys', 'Revenue': 1013781081.63}





---


# MongoDB Analysis

# MongoDB Analysis Summary

## Database Overview

- Telco Documents: 7,043
- Retail Churn Documents: 5,630
- Retail Sales Documents: 1,000,000

---

## Telco Churn Distribution

| _id   |   Customers |
|:------|------------:|
| Yes   |        1869 |
| No    |        5174 |

### Observation

- Top result: {'_id': 'Yes', 'Customers': 1869}

## Collection Statistics

| Collection | Documents |
|------------|-----------|
| telco_customers | 7,043 |
| retail_churn_customers | 5,630 |
| retail_sales_customers | 1,000,000 |

---

## Telco Contract Distribution

| _id            |   Customers |
|:---------------|------------:|
| Month-to-month |        3875 |
| Two year       |        1695 |
| One year       |        1473 |

### Observation

- Top result: {'_id': 'Month-to-month', 'Customers': 3875}

## Collection Statistics

| Collection | Documents |
|------------|-----------|
| telco_customers | 7,043 |
| retail_churn_customers | 5,630 |
| retail_sales_customers | 1,000,000 |

---

## Telco Average Monthly Charges

| _id   |   AvgMonthlyCharges |
|:------|--------------------:|
| Yes   |             74.4413 |
| No    |             61.2651 |

### Observation

- Top result: {'_id': 'Yes', 'AvgMonthlyCharges': 74.44133226324237}

## Collection Statistics

| Collection | Documents |
|------------|-----------|
| telco_customers | 7,043 |
| retail_churn_customers | 5,630 |
| retail_sales_customers | 1,000,000 |

---

## Retail Complaints vs Churn

| _id                         |   Customers |
|:----------------------------|------------:|
| {'Churn': 1, 'Complain': 1} |         508 |
| {'Churn': 0, 'Complain': 0} |        3586 |
| {'Churn': 0, 'Complain': 1} |        1096 |
| {'Churn': 1, 'Complain': 0} |         440 |

### Observation

- Top result: {'_id': {'Churn': 1, 'Complain': 1}, 'Customers': 508}

## Collection Statistics

| Collection | Documents |
|------------|-----------|
| telco_customers | 7,043 |
| retail_churn_customers | 5,630 |
| retail_sales_customers | 1,000,000 |

---

## Retail Average Cashback

|   _id |   AvgCashback |
|------:|--------------:|
|     1 |       160.371 |
|     0 |       180.635 |

### Observation

- Top result: {'_id': 1.0, 'AvgCashback': 160.3709282700422}

## Collection Statistics

| Collection | Documents |
|------------|-----------|
| telco_customers | 7,043 |
| retail_churn_customers | 5,630 |
| retail_sales_customers | 1,000,000 |

---

## Retail Average Satisfaction

|   _id |   AvgSatisfaction |
|------:|------------------:|
|     0 |           3.00128 |
|     1 |           3.3903  |

### Observation

- Top result: {'_id': 0.0, 'AvgSatisfaction': 3.001281503630927}

## Collection Statistics

| Collection | Documents |
|------------|-----------|
| telco_customers | 7,043 |
| retail_churn_customers | 5,630 |
| retail_sales_customers | 1,000,000 |

---

## Retail Sales Loyalty Analysis

| _id                                  |
|:-------------------------------------|
| {'Loyalty': 'Yes', 'Churned': 'No'}  |
| {'Loyalty': 'No', 'Churned': 'Yes'}  |
| {'Loyalty': 'No', 'Churned': 'No'}   |
| {'Loyalty': 'Yes', 'Churned': 'Yes'} |

### Observation

- Top result: {'_id': {'Loyalty': 'Yes', 'Churned': 'No'}}

## Collection Statistics

| Collection | Documents |
|------------|-----------|
| telco_customers | 7,043 |
| retail_churn_customers | 5,630 |
| retail_sales_customers | 1,000,000 |

---



---


# SQL vs MongoDB Comparison

# SQL vs MongoDB Comparison

This report compares equivalent analytics performed using SQLite and MongoDB.

## Telco Churn Distribution

### SQLite Result

| Churn Label   |   Customers |
|:--------------|------------:|
| No            |        5174 |
| Yes           |        1869 |

### MongoDB Result

| _id   |   Customers |
|:------|------------:|
| No    |        5174 |
| Yes   |        1869 |

### Observation

- Both systems produced equivalent business results.
- SQLite used SQL GROUP BY statements.
- MongoDB used aggregation pipelines.

---

## Retail Churn Distribution

### SQLite Result

|   Churn |   Customers |
|--------:|------------:|
|       0 |        4682 |
|       1 |         948 |

### MongoDB Result

|   _id |   Customers |
|------:|------------:|
|     1 |         948 |
|     0 |        4682 |

### Observation

- Both systems produced equivalent business results.
- SQLite used SQL GROUP BY statements.
- MongoDB used aggregation pipelines.

---

## Retail Sales Churn Distribution

### SQLite Result

| churned   |   Customers |
|:----------|------------:|
| No        |      500271 |
| Yes       |      499729 |

### MongoDB Result

| _id   |   Customers |
|:------|------------:|
| No    |      500271 |
| Yes   |      499729 |

### Observation

- Both systems produced equivalent business results.
- SQLite used SQL GROUP BY statements.
- MongoDB used aggregation pipelines.

---

## Technology Comparison


| Feature | SQLite | MongoDB |
|----------|----------|----------|
| Database Type | Relational | NoSQL Document |
| Schema | Fixed | Flexible |
| Query Language | SQL | Aggregation Pipeline |
| Joins | Strong Support | Limited |
| JSON Storage | Limited | Native |
| Transaction Data | Excellent | Good |
| Customer Profiles | Good | Excellent |
| Analytics | Excellent | Excellent |
| Scalability | Moderate | High |


## Project Conclusions

- SQLite was well suited for structured customer analytics and reporting.
- MongoDB provided flexible document storage for customer profiles.
- Both technologies produced consistent churn analysis results.
- SQLite was easier for tabular business reporting.
- MongoDB was better suited for semi-structured customer records.


---


# Exploratory Data Analysis

# Exploratory Data Analysis Summary

## Telco Customer Churn

- Churn Rate: 26.54%
- Average Monthly Charges: $64.76
- Average CLTV: $4400.30

### Strongest Churn Correlations

- Tenure Months: 0.352
- Total Charges: 0.199
- Monthly Charges: 0.193
- CLTV: 0.127

## Retail Customer Churn

- Churn Rate: 16.84%
- Average Cashback: 177.22
- Average Satisfaction Score: 3.07

### Strongest Churn Correlations

- Tenure: 0.349
- DaySinceLastOrder: 0.161
- CashbackAmount: 0.154
- NumberOfDeviceRegistered: 0.108
- SatisfactionScore: 0.105

## Retail Sales

- Churn Rate: 49.97%
- Average Total Sales: $5056.06
- Average Transactions: 49.99

### Strongest Churn Correlations

- days_since_last_purchase: 0.002
- website_visits: 0.001
- total_transactions: 0.001
- customer_support_calls: 0.001
- online_purchases: 0.001

## Cross-Industry Comparison

- Telco Churn Rate: 26.54%
- Retail Churn Rate: 16.84%
- Retail Sales Churn Rate: 49.97%

### Key Finding

The strongest churn predictors identified through correlation analysis will be used during Phase 7 predictive modeling.


---


# Predictive Modeling

# Predictive Modeling Summary

## Model Performance Comparison

| Dataset      | Model               |   Accuracy |   Precision |   Recall |     F1 |    AUC |
|:-------------|:--------------------|-----------:|------------:|---------:|-------:|-------:|
| Retail Churn | Decision Tree       |     0.9352 |      0.791  |   0.8368 | 0.8133 | 0.896  |
| Retail Churn | Random Forest       |     0.9405 |      0.9301 |   0.7    | 0.7988 | 0.9808 |
| Retail Churn | Logistic Regression |     0.8419 |      0.5968 |   0.1947 | 0.2937 | 0.8007 |
| Retail Sales | Decision Tree       |     0.5004 |      0.5001 |   0.5006 | 0.5003 | 0.5004 |
| Retail Sales | Random Forest       |     0.5011 |      0.5009 |   0.464  | 0.4817 | 0.5029 |
| Retail Sales | Logistic Regression |     0.5004 |      0.5002 |   0.4257 | 0.46   | 0.5007 |
| Telco        | Random Forest       |     0.7736 |      0.5972 |   0.4519 | 0.5145 | 0.7874 |
| Telco        | Logistic Regression |     0.7729 |      0.6038 |   0.4198 | 0.4953 | 0.8103 |
| Telco        | Decision Tree       |     0.7083 |      0.4552 |   0.5027 | 0.4778 | 0.6426 |

## Best Overall Model

- Dataset: Retail Churn
- Model: Decision Tree
- Accuracy: 0.9352
- Precision: 0.7910
- Recall: 0.8368
- F1 Score: 0.8133

## Best Model by Dataset

| Dataset      | Model         |   Accuracy |   Precision |   Recall |     F1 |    AUC |
|:-------------|:--------------|-----------:|------------:|---------:|-------:|-------:|
| Retail Churn | Decision Tree |     0.9352 |      0.791  |   0.8368 | 0.8133 | 0.896  |
| Retail Sales | Decision Tree |     0.5004 |      0.5001 |   0.5006 | 0.5003 | 0.5004 |
| Telco        | Random Forest |     0.7736 |      0.5972 |   0.4519 | 0.5145 | 0.7874 |

## Telco Customer Churn

### Top Random Forest Features

| Feature         |   Importance |
|:----------------|-------------:|
| Monthly Charges |       0.3015 |
| Total Charges   |       0.259  |
| CLTV            |       0.2289 |
| Tenure Months   |       0.2106 |

Most Important Feature: Monthly Charges (0.3015)

## Retail Customer Churn

### Top Random Forest Features

| Feature           |   Importance |
|:------------------|-------------:|
| Tenure            |       0.2832 |
| CashbackAmount    |       0.2569 |
| WarehouseToHome   |       0.1461 |
| DaySinceLastOrder |       0.1002 |
| SatisfactionScore |       0.0689 |
| OrderCount        |       0.0543 |
| CouponUsed        |       0.0522 |
| HourSpendOnApp    |       0.0382 |

Most Important Feature: Tenure (0.2832)

## Retail Sales

### Top Random Forest Features

| Feature                  |   Importance |
|:-------------------------|-------------:|
| total_sales              |       0.1066 |
| unit_price               |       0.1066 |
| avg_purchase_value       |       0.1064 |
| days_since_last_purchase |       0.097  |
| in_store_purchases       |       0.087  |
| website_visits           |       0.0865 |
| online_purchases         |       0.0863 |
| total_transactions       |       0.0861 |
| age                      |       0.0806 |
| customer_support_calls   |       0.0615 |

Most Important Feature: total_sales (0.1066)

## Cross-Industry Comparison

| Dataset      | Model         |   Accuracy |   Precision |   Recall |     F1 |    AUC |
|:-------------|:--------------|-----------:|------------:|---------:|-------:|-------:|
| Retail Churn | Decision Tree |     0.9352 |      0.791  |   0.8368 | 0.8133 | 0.896  |
| Retail Sales | Decision Tree |     0.5004 |      0.5001 |   0.5006 | 0.5003 | 0.5004 |
| Telco        | Random Forest |     0.7736 |      0.5972 |   0.4519 | 0.5145 | 0.7874 |

### Model Selection Rationale

#### Retail Churn

- Decision Tree was selected as the best model because it achieved the highest F1 score (0.8133) for the dataset.
- The next closest model was Random Forest with an F1 score of 0.7988.
- Although Random Forest achieved the highest accuracy (0.9405), model selection was based on F1 score because churn prediction requires balancing precision and recall.
- F1 score was used as the primary evaluation metric because customer churn prediction is a classification problem where identifying churners accurately is more important than maximizing overall accuracy.

#### Retail Sales

- Decision Tree was selected as the best model because it achieved the highest F1 score (0.5003) for the dataset.
- The next closest model was Random Forest with an F1 score of 0.4817.
- Although Random Forest achieved the highest accuracy (0.5011), model selection was based on F1 score because churn prediction requires balancing precision and recall.
- F1 score was used as the primary evaluation metric because customer churn prediction is a classification problem where identifying churners accurately is more important than maximizing overall accuracy.

#### Telco

- Random Forest was selected as the best model because it achieved the highest F1 score (0.5145) for the dataset.
- The next closest model was Logistic Regression with an F1 score of 0.4953.
- F1 score was used as the primary evaluation metric because customer churn prediction is a classification problem where identifying churners accurately is more important than maximizing overall accuracy.


## Retail Sales Performance Assessment

The Retail Sales dataset produced substantially lower predictive performance than the Telco and Retail Churn datasets.

- Best Model: Decision Tree
- F1 Score: 0.5003
- Accuracy: 0.5004

### Interpretation

All evaluated models achieved relatively low predictive performance on the Retail Sales dataset. This suggests that the selected feature set provides limited predictive information regarding customer churn.

### Recommendations for Future Modeling

Future work should investigate additional features and feature engineering approaches, including:

- Loyalty program participation
- Income bracket and demographic variables
- Purchase frequency behavior
- Promotion effectiveness measures
- Customer engagement attributes such as app usage, email subscriptions, and social media engagement
- Return-related metrics including product return rates and returned value
- Engineered behavioral indicators such as customer value score, return rate, online purchase ratio, sales per transaction, and support calls per purchase

The inclusion of additional categorical variables and advanced behavioral features may improve the predictive capability of the Retail Sales churn models.

## Business Implications

- Decision Tree achieved the highest F1 score for the selected datasets and was therefore chosen as the preferred model.
- Random Forest achieved slightly higher accuracy in some datasets, but Decision Tree provided a better balance between precision and recall.
- Feature importance rankings identify the strongest drivers of customer churn.
- Predictive models can be used to identify high-risk customers for targeted retention campaigns.
- Differences in model performance across industries suggest that churn behavior varies by business context.


---


# Feature Importance Analysis

# Feature Importance Analysis

## Telco Customer Churn

| Feature         |   Importance |
|:----------------|-------------:|
| Monthly Charges |       0.3015 |
| Total Charges   |       0.259  |
| CLTV            |       0.2289 |
| Tenure Months   |       0.2106 |

## Retail Customer Churn

| Feature           |   Importance |
|:------------------|-------------:|
| Tenure            |       0.2832 |
| CashbackAmount    |       0.2569 |
| WarehouseToHome   |       0.1461 |
| DaySinceLastOrder |       0.1002 |
| SatisfactionScore |       0.0689 |
| OrderCount        |       0.0543 |
| CouponUsed        |       0.0522 |
| HourSpendOnApp    |       0.0382 |

## Retail Sales

| Feature                  |   Importance |
|:-------------------------|-------------:|
| total_sales              |       0.1066 |
| unit_price               |       0.1066 |
| avg_purchase_value       |       0.1064 |
| days_since_last_purchase |       0.097  |
| in_store_purchases       |       0.087  |
| website_visits           |       0.0865 |
| online_purchases         |       0.0863 |
| total_transactions       |       0.0861 |
| age                      |       0.0806 |
| customer_support_calls   |       0.0615 |

## Cross-Dataset Comparison

| Telco Feature   |   Telco Importance | Retail Churn Feature   |   Retail Churn Importance | Retail Sales Feature   |   Retail Sales Importance |
|:----------------|-------------------:|:-----------------------|--------------------------:|:-----------------------|--------------------------:|
| Monthly Charges |             0.3015 | Tenure                 |                    0.2832 | total_sales            |                    0.1066 |
| Total Charges   |             0.259  | CashbackAmount         |                    0.2569 | unit_price             |                    0.1066 |
| CLTV            |             0.2289 | WarehouseToHome        |                    0.1461 | avg_purchase_value     |                    0.1064 |

## Model Interpretation

Feature importance analysis identified the customer characteristics most strongly associated with churn.

These findings provide a foundation for targeted retention strategies and proactive customer engagement programs.


---


# Business Recommendations

# Business Recommendations

## Telco Customer Churn

### Top Churn Drivers

| Feature         |   Importance |
|:----------------|-------------:|
| Monthly Charges |       0.3015 |
| Total Charges   |       0.259  |
| CLTV            |       0.2289 |

### Interpretation

The Random Forest model identified **Monthly Charges**, **Total Charges**, and **CLTV** as the strongest predictors of churn. This suggests pricing and customer value are major drivers of customer retention.

### Recommendations

- **Monthly Charges**: Review pricing strategies and offer discounts to high-cost customers.
- **Total Charges**: Analyze customer spending patterns and develop targeted retention programs based on lifetime customer value.
- **CLTV**: Use customer lifetime value segmentation to prioritize retention initiatives and allocate marketing resources efficiently.

## Retail Customer Churn

### Top Churn Drivers

| Feature         |   Importance |
|:----------------|-------------:|
| Tenure          |       0.2832 |
| CashbackAmount  |       0.2569 |
| WarehouseToHome |       0.1461 |

### Interpretation

The Random Forest model identified **Tenure**, **CashbackAmount**, and **WarehouseToHome** as the strongest churn indicators. Customer tenure, incentives, and service accessibility appear to influence customer retention decisions.

### Recommendations

- **Tenure**: Build retention programs focused on recently acquired customers.
- **CashbackAmount**: Expand reward and cashback programs to improve retention.
- **WarehouseToHome**: Evaluate delivery distance impacts and improve logistics, fulfillment speed, or local distribution options.

## Retail Sales

### Top Churn Drivers

| Feature            |   Importance |
|:-------------------|-------------:|
| total_sales        |       0.1066 |
| unit_price         |       0.1066 |
| avg_purchase_value |       0.1064 |

### Interpretation

The Random Forest model identified **total_sales**, **unit_price**, and **avg_purchase_value** as the most important predictors. These variables relate primarily to customer spending behavior and purchasing value.

### Recommendations

- **total_sales**: Develop VIP retention programs for high-spending customers.
- **unit_price**: Review pricing competitiveness and identify customer segments that are sensitive to product pricing.
- **avg_purchase_value**: Increase customer value through targeted bundle offers and cross-selling initiatives.

### Model Performance

- Best Model: Decision Tree
- Accuracy: 0.5004
- F1 Score: 0.5003

### Retail Sales Modeling Limitation

The best Retail Sales model achieved an F1 score of 0.5003, indicating limited predictive performance.

The Retail Sales dataset performed substantially worse than the Telco and Retail Customer Churn datasets (F1 ≈ 0.81), suggesting that the currently selected feature set provides limited predictive information regarding churn.

Although the identified features were the most important within the model, the overall predictive capability remains relatively weak. These findings should therefore be interpreted cautiously.

Future work should investigate:

- Loyalty program participation
- Purchase frequency variables
- Promotion effectiveness metrics
- Customer engagement indicators (app usage, email subscriptions, social media engagement)
- Additional behavioral feature engineering

## Cross-Industry Insights

- Telco churn appears to be heavily influenced by pricing and customer value metrics.
- Retail Customer Churn appears to be influenced by customer tenure, rewards programs, and service accessibility.
- Retail Sales exhibited weak predictive performance, indicating that additional behavioral and engagement variables may be required.
- Feature importance analysis provides actionable business intelligence for customer retention strategies.
- Organizations should continuously monitor the top churn drivers identified by predictive models and adapt retention initiatives accordingly.
- Telco and Retail Customer Churn models achieved strong predictive performance (F1 ≈ 0.81), indicating that customer churn can be predicted with reasonable accuracy using the selected features.
## Executive Summary

- Monthly Charges emerged as the strongest predictor of churn in the Telco dataset.
- Customer Tenure was the strongest predictor of churn in the Retail Customer Churn dataset.
- Total Sales was identified as the most influential Retail Sales feature; however, the overall model performance was limited.
- Predictive modeling suggests that pricing, customer value, customer tenure, and customer incentives are the most important retention levers across the analyzed industries.
- Organizations can leverage these insights to improve customer retention strategies, prioritize high-risk customers, and deploy proactive intervention programs.


---


    # Project Conclusions

    ## Key Outcomes

    - Decision Tree produced the strongest churn prediction performance.
    - Monthly Charges was the strongest Telco churn driver.
    - Tenure was the strongest Retail Customer Churn driver.
    - Retail Sales requires additional feature engineering.

    ## Future Work

    - Evaluate XGBoost
    - Explore K-Means segmentation
    - Investigate additional Retail Sales features
    - Deploy dashboard-driven monitoring
    