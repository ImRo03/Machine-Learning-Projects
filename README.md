# Machine Learning Projects

Hands-on Machine Learning projects using Python, Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn. This repository documents practical experiments, model evaluation, and end-to-end ML workflows.

## Projects

### 1. Advertising Sales Prediction — Linear Regression
**Folder:** `Regression/Advertising-Sales-Prediction/`

A regression project using the Advertising dataset to predict product sales from advertising budgets.

**What this project covers**
- Inspecting and cleaning tabular data
- Exploring relationships between advertising spend and sales
- Training a Linear Regression model with one feature (TV)
- Comparing a simple model against a model using TV, radio, and newspaper
- Evaluating predictions with Mean Absolute Error (MAE)
- Comparing performance with a mean-prediction baseline

**Results from the current 80/20 train-test split**
| Model | Test MAE |
|---|---:|
| Mean-prediction baseline | 4.9625 |
| Linear Regression — TV only | 2.4444 |
| Linear Regression — TV, radio, newspaper | 1.4608 |

The three-feature model had a lower MAE on this test split. This is a result from one split, not proof that the same score will generalize to every sample.

**Notebook:** [Linear Regression Model on Advertising dataset](Regression/Advertising-Sales-Prediction/Linear%20Regression%20Model%20on%20Advertising%20dataset.ipynb)

**Dataset:** [Advertising.csv](Regression/Advertising-Sales-Prediction/Advertising.csv) — included in this repository.

**Dataset source:** [Introduction to Statistical Learning (ISLR)](https://www.statlearning.com/)

> The notebook looks for `Advertising.csv` in either its own project folder or the repository root.

### 2. Medical Insurance Charges — Linear Regression Practice
**Folder:** `Regression/Medical-Insurance-Cost-Prediction/`

**Status:** Foundational practice completed; the full regression study will continue later.

- Notebook: [insurance_linear_regression_practice.ipynb](Regression/Medical-Insurance-Cost-Prediction/insurance_linear_regression_practice.ipynb)
- Dataset: [insurance.csv](Regression/Medical-Insurance-Cost-Prediction/insurance.csv)
- Project notes and run instructions: [README](Regression/Medical-Insurance-Cost-Prediction/README.md)
- Current model uses only `age`, `bmi`, and `children`; categorical encoding and further regression evaluation are not yet covered.
- On one 80/20 split, the baseline MAE was 9,861.80 and Linear Regression MAE was 9,620.93. These are introductory results, not a finished or optimized model.

Dataset source: [Medical Insurance dataset](https://github.com/stedy/Machine-Learning-with-R-datasets/blob/master/insurance.csv).

### 3. Customer Churn Prediction — Classification
**Folder:** `Classification/Customer-Churn-Prediction/`

**Status:** In progress.

A classification project focused on identifying customers at higher risk of leaving, with the goal of helping a business prioritize retention outreach.

- Dataset: [Telco Customer Churn CSV](Classification/Customer-Churn-Prediction/data/Telco-Customer-Churn.csv)
- Project brief and workflow: [Customer Churn README](Classification/Customer-Churn-Prediction/README.md)
- Dataset has 7,043 customer records and the target column `Churn` (Yes/No).
- Models, evaluation results, and business recommendations will be added only after we implement and evaluate them.

Dataset source: [IBM Telco Customer Churn sample](https://github.com/IBM/telco-customer-churn-on-icp4d/blob/master/data/Telco-Customer-Churn.csv). It describes a fictional telecom company and is for educational/portfolio use, not a production customer dataset.

## Tools
- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook

## Repository structure

```text
Machine-Learning-Projects/
├── README.md
├── Regression/
│   ├── Advertising-Sales-Prediction/
│   │   ├── README.md
│   │   ├── Advertising.csv
│   │   └── Linear Regression Model on Advertising dataset.ipynb
│   └── Medical-Insurance-Cost-Prediction/
│       ├── README.md
│       ├── insurance.csv
│       └── insurance_linear_regression_practice.ipynb
└── Classification/
    └── Customer-Churn-Prediction/
        ├── README.md
        └── data/
            └── Telco-Customer-Churn.csv
```
