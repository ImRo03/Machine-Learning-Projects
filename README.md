# Machine Learning Projects

Hands-on Machine Learning projects using Python, Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn. This repository documents practical experiments, model evaluation, and end-to-end ML workflows.

## Projects

### 1. Advertising Sales Prediction — Linear Regression
**Folder:** `Regression/`

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

**Notebook:** [Linear Regression Model on Advertising dataset](Regression/Linear%20Regression%20Model%20on%20Advertising%20dataset.ipynb)

**Dataset source:** [Introduction to Statistical Learning (ISLR) — Advertising data](https://www.statlearning.com/)

> Note: The notebook expects `Advertising.csv` to be available in its working directory. Download it from the source above before running the notebook.

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
└── Regression/
    └── Linear Regression Model on Advertising dataset.ipynb
```

More projects will be added as I learn and implement additional Machine Learning algorithms.
