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



