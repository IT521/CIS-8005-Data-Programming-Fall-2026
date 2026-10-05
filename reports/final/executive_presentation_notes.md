# Executive Presentation Notes

## Slide 1: Project Overview

This project analyzed customer churn across three industries:

- Telecommunications
- Retail Customer Churn
- Retail Sales

The project combined SQL analytics, MongoDB analytics, exploratory data analysis, predictive modeling, and business intelligence recommendations.

## Slide 2: Business Problem

Customer churn affects profitability and customer lifetime value.

Goal:
Identify churn drivers and develop predictive models to support customer retention.

## Slide 3: Dataset Overview

Datasets analyzed:

- Telco (7,043 customers)
- Retail Churn (5,630 customers)
- Retail Sales (1,000,000 customers)

## Slide 4: Data Cleaning

Major activities:

- Missing value treatment
- Duplicate removal
- Data type correction
- Feature engineering

## Slide 5: SQLite Analytics

Key finding:

Customers with higher monthly charges showed higher churn rates.

## Slide 6: MongoDB Analytics

MongoDB aggregation pipelines produced results consistent with SQLite.

## Slide 7: Exploratory Data Analysis

Top churn indicators:

- Monthly Charges
- Tenure
- CashbackAmount

## Slide 8: Predictive Modeling

Models evaluated:

- Logistic Regression
- Decision Tree
- Random Forest

Best Overall Model:

- Decision Tree
- F1 Score: 0.8133

## Slide 9: Feature Importance

Top Drivers:

Telco:
- Monthly Charges
- Total Charges
- CLTV

Retail Churn:
- Tenure
- CashbackAmount
- WarehouseToHome

## Slide 10: Recommendations

- Review pricing strategy
- Strengthen loyalty programs
- Improve retention campaigns
- Monitor high-risk customers

## Slide 11: Limitations

Retail Sales models achieved lower performance and require additional feature engineering.

## Slide 12: Future Work

- Evaluate XGBoost
- Explore K-Means clustering
- Investigate PCA
- Improve Retail Sales feature set

## Slide 13: Conclusion

Churn can be predicted effectively in Telco and Retail Customer Churn datasets.

Organizations can use predictive analytics to proactively target retention efforts.

