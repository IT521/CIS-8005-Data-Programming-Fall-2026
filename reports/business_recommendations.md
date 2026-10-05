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
