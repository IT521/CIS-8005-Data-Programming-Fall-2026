# Executive Dashboard Summary

## Churn Rates

| Dataset | Churn Rate |
|----------|----------:|
| Telco | 26.54% |
| Retail Churn | 16.84% |
| Retail Sales | 49.97% |

## Best Performing Models

| Dataset      | Best Model    |   F1 Score |
|:-------------|:--------------|-----------:|
| Retail Churn | Decision Tree |     0.8133 |
| Retail Sales | Decision Tree |     0.5003 |
| Telco        | Random Forest |     0.5145 |

## Top Churn Drivers

### Telco

- Monthly Charges
- Total Charges
- CLTV

### Retail Customer Churn

- Tenure
- CashbackAmount
- WarehouseToHome

### Retail Sales

- total_sales
- unit_price
- avg_purchase_value

## Best Overall Model

- Dataset: Retail Churn
- Model: Decision Tree
- F1 Score: 0.8133

## Executive Recommendations

- Review pricing and customer value strategies.
- Expand customer reward and cashback programs.
- Focus retention efforts on recently acquired customers.
- Deploy predictive churn monitoring.
- Prioritize high-risk customers for intervention.

## Key Project Finding

Decision Tree achieved the strongest balance of precision and recall across the analyzed churn datasets, while Random Forest models identified the primary business drivers of customer churn.
