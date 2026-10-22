# Advertising Sales Prediction — Linear Regression

**Status:** Foundational project completed. Further regression topics will be studied separately.

## Goal

Explore how advertising budgets relate to product sales, train Linear Regression models, and compare test-set prediction errors against a simple baseline.

## Dataset

- **File:** [Advertising.csv](Advertising.csv)
- **Source:** [Introduction to Statistical Learning (ISLR)](https://www.statlearning.com/)
- **Rows:** 200 observations
- **Target:** `sales`
- **Features:** `TV`, `radio`, and `newspaper` advertising budgets

The original CSV contains an extra index-like column, which is removed during the notebook's data-cleaning steps.

## Notebook

Open [Linear Regression Model on Advertising dataset.ipynb](Linear%20Regression%20Model%20on%20Advertising%20dataset.ipynb).

The notebook covers:
- Dataset inspection and basic cleaning
- Exploratory scatter plots and correlation
- Simple Linear Regression with TV advertising only
- Multiple Linear Regression using all three advertising features
- Train-test splitting
- Baseline comparison
- Predictions, MAE, and actual-vs-predicted inspection

## Results recorded

Results from the project's 80/20 train-test split:

| Model | Test MAE |
|---|---:|
| Mean baseline | 4.9625 |
| Linear Regression — TV only | 2.4444 |
| Linear Regression — TV, radio, newspaper | 1.4608 |

The three-feature model had lower MAE on this split. This is a result from one test split and does not guarantee the same performance on unseen samples.

## Run locally

Keep `Advertising.csv` in the same folder as the notebook. Open the notebook from this project folder, or launch it from the repository root; the first cell checks both locations.

Required libraries: `pandas`, `matplotlib`, `seaborn`, and `scikit-learn`.

## Scope

This project was used to practise the basic supervised regression workflow. More advanced topics—such as categorical encoding, reusable preprocessing pipelines, cross-validation, regularization, and additional regression algorithms—will be covered later in the ML study roadmap.
