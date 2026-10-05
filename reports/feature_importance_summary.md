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
