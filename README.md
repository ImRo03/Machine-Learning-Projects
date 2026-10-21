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

**Dataset:** [Advertising.csv](Regression/Advertising.csv) — included in this repository.

**Dataset source:** [Introduction to Statistical Learning (ISLR)](https://www.statlearning.com/)

> Run the notebook with `Regression/` as the working directory so `pd.read_csv("Advertising.csv")` finds the dataset.

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
