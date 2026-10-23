# White Wine Quality Prediction — Decision Tree & Random Forest Regression

**Status:** Foundational regression practice completed; further ML topics will continue separately.

## Objective

Predict numerical wine-quality ratings from physicochemical measurements and practise model training, validation, MAE evaluation, and model comparison.

## Dataset

- **File:** [whitewines.csv](whitewines.csv) — included in this folder.
- **Rows before duplicate removal:** 4,898.
- **Exact duplicate rows removed:** 937.
- **Rows after duplicate removal:** 3,961.
- **Target:** `quality`.
- **Input features:** 11 wine measurements.

## Notebooks

### 1. Decision Tree Regression

[Open Decision Tree Regression.ipynb](Decision%20Tree%20Regression.ipynb)

- Compared `max_depth=2` and `max_depth=3` using validation MAE.
- Depth 3 had the lower validation MAE among those two candidates.

### 2. Random Forest Regression

[Open Random_Forest.ipynb](Random_Forest.ipynb)

- Trained a Random Forest with `n_estimators=100`.
- Compared training and validation MAE, then evaluated a model trained on the full training split on the test split.

## Results from these practice splits

| Model | Training MAE | Validation MAE | Test MAE |
|---|---:|---:|---:|
| Decision Tree, `max_depth=3` | 0.5868 | 0.6070 | 0.6261 |
| Random Forest, 100 trees | 0.2016 | 0.5482 | 0.5689 |

The Random Forest had lower validation and test MAE than the depth-3 Decision Tree in this exercise. Its much lower training MAE than validation MAE also indicates a generalization gap.

These are educational results from particular splits, not guarantees of future performance. In a strict benchmark, keep the test set untouched until the full model-selection process is complete.

## Workflow covered

1. Inspect and clean tabular data.
2. Separate features (`X`) and target (`y`).
3. Create training, validation, and test sets.
4. Train regression models using `.fit()`.
5. Generate predictions using `.predict()`.
6. Calculate MAE and compare models on validation data.
7. Evaluate a selected configuration on test data.

## Run locally

1. Keep both notebooks and `whitewines.csv` in this folder.
2. Open a notebook in Jupyter.
3. Run its cells from top to bottom.

Required libraries: `pandas` and `scikit-learn`.
