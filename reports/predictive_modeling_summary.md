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
