# Medical Insurance Charges — Practice

I'm using this folder to practise regression and the data preparation that happens before model training. Some cells in the preprocessing notebook use small made-up examples just to understand each step.

## Dataset

- **File:** [insurance.csv](insurance.csv)
- **Source:** [Medical Insurance dataset on GitHub](https://github.com/stedy/Machine-Learning-with-R-datasets/blob/master/insurance.csv)
- **Original shape:** 1,338 rows × 7 columns.
- **Target:** `charges`.
- **Features:** `age`, `sex`, `bmi`, `children`, `smoker`, and `region`.

## Notebooks

### 1. Linear Regression Practice

[Open insurance_linear_regression_practice.ipynb](insurance_linear_regression_practice.ipynb)

This notebook covers loading and inspecting the dataset, basic EDA, checking duplicates and missing values, making a train/test split, building a mean baseline, and training a first Linear Regression model with numerical features.

The initial test MAE was 9,620.93, compared with 9,861.80 for the mean baseline on the same split. These are results from this practice exercise, not a guarantee of future performance.

### 2. Data Preprocessing and Data Pipeline

[Open Data Preprocessing and Data Pipeline.ipynb](Data%20Preprocessing%20and%20Data%20Pipeline.ipynb)

In this notebook I practised:

- Using a `Pipeline` to connect preprocessing and a model.
- Using `fit()` to train and `predict()` to make predictions.
- Using `ColumnTransformer` to apply different steps to selected columns and pass numerical columns through unchanged.
- Understanding data leakage and fitting preprocessing on training data only.
- Filling missing numerical values with `SimpleImputer`, using the median or most frequent value.
- Filling missing categorical values before using `OneHotEncoder`.
- Handling unseen categories with `handle_unknown="ignore"`.
- Combining numerical and categorical preprocessing Pipelines before Linear Regression.
- Checking predictions against actual values and calculating MAE.
- Feature scaling with `StandardScaler` and `MinMaxScaler`.
- Detecting potential outliers with boxplots, the IQR method, and Z-scores.
- Capping values with `.clip()`, trying log transformation with `np.log1p()`, and comparing skewness.

A main thing I learned is not to delete an unusual value just because it looks like an outlier. First check whether it is a real value or a data error.

## Running the notebooks

Keep `insurance.csv` in this folder, open a notebook in Jupyter Notebook or JupyterLab, and run the cells from top to bottom.

Libraries used across these notebooks include Pandas, NumPy, Matplotlib, Seaborn, SciPy, and scikit-learn.
