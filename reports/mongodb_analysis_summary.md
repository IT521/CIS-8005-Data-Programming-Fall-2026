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

