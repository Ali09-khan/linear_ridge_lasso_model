# Polynomial Regression with Ridge and Lasso Regularization

## Overview
This project implements polynomial regression using Ridge and Lasso regularization techniques. It allows users to explore polynomial features of varying degrees, apply regularization to prevent overfitting, and evaluate model performance. The notebook is designed to be reusable with any dataset containing numerical features and a target variable.

## How It Works

### Data Splitting
- The dataset is split into training and test sets using `train_test_split`.

### Feature Transformation
- Polynomial transformations are applied to the input features using `PolynomialFeatures` to generate higher-order terms.
- Standardization of features is performed using `StandardScaler` to ensure that all features are on the same scale.

### Model Selection
- Two regularization techniques are explored:
  - **Ridge Regression (L2 Regularization):** Penalizes the sum of squared coefficients.
  - **Lasso Regression (L1 Regularization):** Penalizes the sum of absolute values of coefficients, encouraging sparsity.
- A range of `alpha` values (regularization strength) is tested using `GridSearchCV` for hyperparameter tuning.

### Metrics Evaluation
- The models are evaluated using multiple metrics such as:
  - **MAE** (Mean Absolute Error)
  - **MSE** (Mean Squared Error)
  - **RMSE** (Root Mean Squared Error)
  - **MAPE** (Mean Absolute Percentage Error)
  - **\(R^2\)** (Coefficient of Determination)
