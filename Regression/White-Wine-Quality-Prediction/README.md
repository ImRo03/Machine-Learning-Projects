# White Wine Quality Prediction — Decision Tree Regression

**Status:** Completed foundational practice; further regression topics will be continued separately.

## Objective

Use a Decision Tree Regressor to predict wine quality from physicochemical measurements, then compare tree depth settings using validation MAE.

## Dataset

- **File:** [whitewines.csv](whitewines.csv) — included in this folder.
- **Rows before duplicate removal:** 4,898.
- **Exact duplicate rows removed:** 937.
- **Rows after duplicate removal:** 3,961.
- **Target:** `quality`.
- **Input features:** 11 wine measurements.

## Workflow

1. Inspect the dataset, data types, missing values, summary statistics, and duplicate records.
2. Remove exact duplicate rows.
3. Separate input features (`X`) from the target (`y`).
4. Create a training/test split, then create a validation split from the training data.
5. Train an unrestricted Decision Tree and inspect training versus validation MAE.
6. Compare `max_depth=2` and `max_depth=3` on the same validation split.
7. Train the selected depth-3 model on the full training split and report final test MAE.

## Results from this split

| Model | Training MAE | Validation MAE |
|---|---:|---:|
| Unrestricted Decision Tree | 0.0000 | 0.6830 |
| Decision Tree, `max_depth=2` | 0.6141 | 0.6341 |
| Decision Tree, `max_depth=3` | 0.5868 | 0.6070 |

The depth-3 model had a lower validation MAE than depth 2 among the two configurations compared.

**Final test MAE for the depth-3 model:** 0.6261.

These scores describe this particular split and practice experiment; they do not guarantee the same result on other samples. In a production evaluation, keep the test set untouched while selecting hyperparameters.

## Run locally

1. Keep `Decision Tree Regression.ipynb` and `whitewines.csv` in this folder.
2. Open the notebook in Jupyter.
3. Run the cells from top to bottom.

Required libraries: `pandas` and `scikit-learn`.
