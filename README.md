# Telecom Churn Prediction

This project aims to predict customer churn in a telecom company using machine learning.

## Dataset

The dataset used is `WA_Fn-UseC_-Telco-Customer-Churn.csv`. It contains information about customers and their service usage, including demographics, services subscribed, monthly charges, and churn status.

## Data Preprocessing

The following preprocessing steps were performed:

* **Handling missing values:** Rows with missing values were dropped.
* **Data type conversion:** The `TotalCharges` column was converted to numeric.
* **Encoding categorical features:**
    * Label encoding for binary features (e.g., `gender`, `Partner`).
    * One-hot encoding for multi-category features (e.g., `InternetService`, `Contract`).
* **Feature engineering:**
    * Created `tenure_mode` features based on median tenure.
    * Scaled numerical features (e.g., `tenure`, `TotalCharges`).
    * Applied log transformation to `TotalCharges`.

## Model Training

* **Logistic Regression:**
    * Trained with L1 and L2 regularization.
    * Hyperparameter tuning using `GridSearchCV`.
    * Evaluated using accuracy, precision, recall, F1-score, and confusion matrix.
    * Cross-validation performed to analyze performance across different folds.

## Results

* The Logistic Regression model with L1 regularization achieved a high recall (0.8207) but lower precision (0.4646) on the test set.
* The model is well-regularized and does not overfit.
* There is room to improve precision and balance the trade-off between false positives and true positives.

