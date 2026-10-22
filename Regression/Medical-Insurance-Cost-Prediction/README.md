# Medical Insurance Charges — Linear Regression Practice

**Status:** In progress — foundational practice completed; the full regression study will continue later.

## Objective

Explore a medical insurance dataset and build an initial Linear Regression model to predict insurance charges using three numerical features: age, BMI, and number of children.

## Dataset

- **Local file:** [insurance.csv](insurance.csv) — included in this folder.
- **Source:** [Medical Insurance dataset on GitHub](https://github.com/stedy/Machine-Learning-with-R-datasets/blob/master/insurance.csv)
- **Shape before duplicate removal:** 1,338 rows × 7 columns.
- **Target:** `charges`.
- **Features currently used:** `age`, `bmi`, `children`.
- **Other available features:** `sex`, `smoker`, and `region`. These categorical features are not yet included in the model because encoding and preprocessing will be covered later.

## Work completed so far

1. Loaded and inspected the dataset with Pandas.
2. Checked descriptive statistics, missing values, and duplicate rows.
3. Found and removed one duplicate record.
4. Explored average charges by smoking status.
5. Visualized age vs. charges and BMI vs. charges, including a comparison by smoking status.
6. Split data into training and test sets using an 80/20 split with `random_state=42`.
7. Built a mean-prediction baseline.
8. Trained an initial Linear Regression model using `age`, `bmi`, and `children`.
9. Compared actual vs. predicted charges and inspected examples with large prediction errors.

## Initial results

| Model | Test MAE |
|---|---:|
| Mean baseline | 9,861.80 |
| Linear Regression | 9,620.93 |

The initial Linear Regression model improves MAE by approximately 2.44% compared with the mean baseline on this test split. The improvement is modest, and the model underpredicts some customers with high charges.

The EDA shows higher average charges among smokers in this dataset. This is an observed association; the analysis alone does not establish causation.

## Run the notebook

1. Download or clone this repository.
2. Open [`insurance_linear_regression_practice.ipynb`](insurance_linear_regression_practice.ipynb) in Jupyter Notebook or JupyterLab.
3. Ensure `insurance.csv` stays in the same folder as the notebook.
4. Run the notebook cells from top to bottom.

Required Python libraries: `pandas`, `matplotlib`, `seaborn`, and `scikit-learn`.

The notebook is stored without saved cell outputs; run the cells to regenerate tables and plots.

## Remaining learning topics

This is not the final version of the regression study. Planned follow-up topics include R², encoding categorical features, preprocessing pipelines, feature/model comparisons, and further regression algorithms after they are learned.

This repository documents a learning exercise; model results should not be treated as professional medical or insurance advice.
