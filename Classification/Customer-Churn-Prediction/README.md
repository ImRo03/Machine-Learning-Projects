# Customer Churn Prediction

**Status:** In progress  
**Problem type:** Binary classification  
**Domain:** Telecommunications

## Business problem

A telecommunications company wants to identify customers who are more likely to leave. The goal is to use customer/account attributes to estimate churn risk and help the business prioritize retention outreach.

The model is a decision-support tool, not proof that a customer will leave or that a retention offer will prevent churn.

## Dataset

- **File:** `data/Telco-Customer-Churn.csv`
- **Rows:** 7,043 customer records
- **Columns:** 21, including the target
- **Target:** `Churn` — Yes/No
- **Source:** [IBM Telco Customer Churn sample](https://github.com/IBM/telco-customer-churn-on-icp4d/blob/master/data/Telco-Customer-Churn.csv)
- **Dataset documentation:** [IBM Cognos Analytics sample description](https://www.ibm.com/docs/en/cognos-analytics/12.1.x?topic=samples-telco-customer-churn)

This is a sample dataset for a fictional telecommunications company, not real production customer data.

## Project workflow

We will build this step by step, validating decisions from the data rather than assuming them:

1. Define the business question and success criteria.
2. Inspect the dataset and identify data-quality issues.
3. Explore churn patterns with EDA.
4. Split data appropriately and prevent leakage.
5. Build a simple baseline classifier.
6. Build a preprocessing-and-model pipeline.
7. Train and compare suitable classifiers, starting with Logistic Regression.
8. Evaluate using a confusion matrix, precision, recall, F1-score, and ROC-AUC as appropriate.
9. Translate model findings into practical retention-prioritization recommendations.
10. Document limitations and make the project reproducible.

## Evaluation principles

Accuracy alone may hide poor detection of customers who churn. We will compare relevant metrics and explain the business trade-offs between missing likely churners and contacting customers who would stay.

All performance claims and recommendations will be added only after the experiments are run and checked.

## Tools

Python, Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn.

## Running the project

The notebook and reproducible instructions will be added as the project develops. The raw CSV is stored in `data/`; keep it unchanged and perform cleaning in code.
