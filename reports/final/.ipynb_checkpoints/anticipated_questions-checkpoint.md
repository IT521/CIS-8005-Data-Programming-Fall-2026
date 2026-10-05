# Anticipated Questions

## Why were Logistic Regression, Decision Tree, and Random Forest selected?

These models are appropriate for binary classification and customer churn prediction.

Decision Trees and Random Forests also support nonlinear relationships and feature importance analysis.

---

## Why was F1 used instead of Accuracy?

Churn prediction requires balancing Precision and Recall.

F1 Score provides a more meaningful evaluation metric than Accuracy alone.

---

## Why was Decision Tree selected?

Decision Tree achieved the highest F1 Score on all datasets.

---

## Why wasn't SVM used?

The Retail Sales dataset contains approximately 1,000,000 records.

SVM becomes computationally expensive at this scale.

---

## Why wasn't PCA used?

A major project objective was interpretability.

Feature importance analysis requires interpretable business variables.

---

## Why did Retail Sales perform poorly?

Retail Sales achieved an F1 Score near 0.50.

Additional behavioral and engagement features are likely required.

---

## What was the strongest churn driver?

Telco:
Monthly Charges

Retail Churn:
Tenure

Retail Sales:
total_sales
