# Anticipated Questions

## Why did you select Logistic Regression, Decision Tree, and Random Forest?

The project objective was customer churn classification.

Logistic Regression was selected as an interpretable baseline classification model.

Decision Trees were selected because they can capture nonlinear customer behavior patterns and generate easily understandable decision rules.

Random Forest was selected because it improves predictive performance, reduces overfitting, and provides feature importance measures that were used to identify the key business drivers of churn.

Models such as Linear Regression, Ridge Regression, Lasso Regression, and Support Vector Regression were not appropriate because the target variable was categorical rather than continuous.

Methods such as SVM and KNN were less suitable due to the large size of the Retail Sales dataset, while K-Means and PCA were not selected because the project focused on churn prediction and business interpretability rather than clustering or dimensionality reduction.

---

## Why did Logistic Regression benefit from scaling?

Logistic Regression uses numerical optimization to estimate model coefficients.

The selected features were measured on very different scales, such as Tenure Months versus CLTV and Total Charges.

StandardScaler was used to standardize the variables and improve convergence, model stability, and coefficient estimation.

Decision Tree and Random Forest models did not require scaling because tree-based algorithms split data based on thresholds rather than feature magnitudes.

---

## Why was F1 Score used instead of Accuracy?

Customer churn prediction requires balancing Precision and Recall.

Accuracy alone can be misleading because a model may correctly classify many non-churners while failing to identify customers who are actually at risk of leaving.

F1 Score provides a balanced measure of model performance and is better suited for evaluating churn prediction models.

---

## Why was Decision Tree selected as the best model?

Decision Tree achieved the highest F1 Score on the evaluated datasets.

Although Random Forest sometimes achieved slightly higher accuracy, Decision Tree provided a better balance between Precision and Recall.

Since customer churn prediction focuses on identifying churners while minimizing false predictions, F1 Score was used as the primary model selection criterion.

---

## Why was Random Forest included if Decision Tree performed better?

Random Forest provided feature importance rankings that were used during Phase 8 Feature Importance Analysis.

These rankings identified the strongest drivers of customer churn and supported the development of business recommendations.

Random Forest therefore contributed valuable business insights even when it was not the highest-performing predictive model.

---

## Why were only numerical features initially selected for Telco Modeling?

The initial model focused on a small set of high-value numerical predictors identified through exploratory analysis:

- Tenure Months
- Monthly Charges
- Total Charges
- CLTV

This simplified the modeling process and provided a clear baseline for comparison.

Future work would include one-hot encoding categorical variables such as Contract, Internet Service, and Tech Support to determine whether model performance can be improved.

---

## Why weren't Contract and Tech Support included initially?

Those variables likely contain additional predictive information.

However, categorical features require additional preprocessing and encoding before they can be used in machine learning models.

The initial model focused on key numerical predictors identified during exploratory analysis.

A future enhancement would be to include one-hot encoded categorical variables and compare model performance.

---

## Why did Telco performance change after adding categorical variables?

Adding categorical variables such as Contract, Internet Service, and Tech Support changed the feature space available to the models.

Model performance can improve or decline depending on how informative the new variables are, how they interact with existing features, and whether they introduce additional complexity.

Feature selection is therefore an iterative process. New features should be evaluated using the same model evaluation metrics to determine whether they improve predictive performance.

---

## Should data leakage have been part of Phase 2: Data Profiling and Quality Assessment?

Yes.

Potential data leakage should ideally be identified during Phase 2 because it represents both a data quality risk and a modeling risk.

Examples from the Telco dataset include:

- Churn Label
- Churn Score
- Churn Reason

These variables either directly represent the target variable or contain information that would only be available after a customer has already churned.

A future revision of the methodology would explicitly include a Target Leakage Assessment section in Phase 2 so that leakage risks are documented before exploratory analysis and predictive modeling begin.

---

## Why was LabelEncoder used for the Retail Sales churn target?

The churned variable was stored as text values.

Machine learning classifiers require a numeric target variable.

LabelEncoder converted the binary categories into numeric values (0 and 1) that could be used directly by Logistic Regression, Decision Tree, and Random Forest.

Unlike one-hot encoding, which is typically used for predictor variables, LabelEncoder is appropriate for binary classification targets because it produces a single numeric outcome variable.

---

## Why wasn't One-Hot Encoding used for the churn target?

One-hot encoding is generally used for predictor variables rather than the target variable.

For binary classification, machine learning models typically expect a single target column containing values such as 0 and 1.

LabelEncoder provides this format directly and avoids creating unnecessary target columns.

---

## Why were Confusion Matrices and ROC Curves added?

Accuracy alone does not provide a complete picture of model performance.

Confusion Matrices show:

- True Positives
- True Negatives
- False Positives
- False Negatives

ROC Curves evaluate model performance across different classification thresholds.

AUC measures the model's ability to distinguish churners from non-churners.

Together with Accuracy, Precision, Recall, and F1 Score, these metrics provide a more comprehensive evaluation of model performance.

---

## How should the Confusion Matrix and ROC Curve be interpreted?

### Confusion Matrix

The Confusion Matrix shows the four possible prediction outcomes:

- True Positives (TP)
- True Negatives (TN)
- False Positives (FP)
- False Negatives (FN)

For churn prediction, False Negatives are particularly important because they represent customers who churned but were not identified by the model.

A strong churn model should maximize True Positives while minimizing False Negatives.

### ROC Curve

The ROC Curve evaluates model performance across multiple classification thresholds.

The ROC Curve plots:

- True Positive Rate (Recall)
- False Positive Rate

A curve closer to the upper-left corner indicates stronger model performance.

### AUC

AUC measures how effectively a model distinguishes churners from non-churners.

General interpretation:

- 0.50 = Random guessing
- 0.60–0.70 = Weak
- 0.70–0.80 = Acceptable
- 0.80–0.90 = Strong
- Above 0.90 = Excellent

F1 evaluates model performance at a single threshold, while ROC/AUC evaluates performance across all thresholds.

---

## Why wasn't SVM used?

The Retail Sales dataset contains approximately 1,000,000 records.

Support Vector Machines can become computationally expensive at that scale.

Decision Trees and Random Forests provided more practical solutions while maintaining strong predictive performance.

---

## Why wasn't PCA used?

One project objective was business interpretability.

Feature Importance Analysis required features with clear business meaning, such as Monthly Charges, Tenure, and CashbackAmount.

PCA would have transformed these variables into principal components, making the results less interpretable to business stakeholders.

---

## Why did the Retail Sales models perform poorly?

The strongest Retail Sales model achieved an F1 Score near 0.50.

This suggests that the selected feature set provides limited predictive information regarding customer churn.

Future work should investigate:

- Loyalty program participation
- Purchase frequency measures
- Promotion effectiveness
- Customer engagement variables
- Additional engineered features

These enhancements may improve predictive performance.

---

## What were the strongest churn drivers?

Telco:

- Monthly Charges
- Total Charges
- CLTV

Retail Customer Churn:

- Tenure
- CashbackAmount
- WarehouseToHome

Retail Sales:

- total_sales
- unit_price
- avg_purchase_value

These drivers were identified using Random Forest feature importance analysis.

---

## What is the key business takeaway from the project?

The analysis demonstrated that customer churn can be predicted with reasonable accuracy in the Telco and Retail Customer Churn datasets.

Pricing, customer value, tenure, and incentive programs were identified as the most influential factors affecting churn.

Organizations can use these insights to improve retention strategies, prioritize high-risk customers, and make more informed business decisions.
