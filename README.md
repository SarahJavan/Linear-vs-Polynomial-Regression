
# Linear Regression vs. Polynomial Regression

## Overview

This project explores the impact of polynomial feature engineering on Linear Regression performance using a small, manually defined dataset with two input features.

The notebook implements and compares **Linear Regression (Degree 1)** and **Polynomial Regression (Degree 2)** using test data and three evaluation metrics: Mean Squared Error (MSE), Mean Absolute Error (MAE), and R² Score.

## Models and Methodology

### 1. Linear Regression — Degree 1

The baseline model uses two original features to predict the target variable. It is trained on the training dataset and evaluated on three test samples.

### 2. Polynomial Regression — Degree 2

Using Scikit-learn's `PolynomialFeatures`, the two input features are transformed into five features:

- \(x_1\)
- \(x_2\)
- \(x_1^2\)
- \(x_1x_2\)
- \(x_2^2\)

The transformed data is then used to train a new Linear Regression model. This allows the model to capture quadratic relationships and interactions between the input features.

## Evaluation Metrics

- **MSE:** Measures the average squared prediction error. Lower is better.
- **MAE:** Measures the average absolute prediction error. Lower is better.
- **R² Score:** Measures how well the model explains variation in the target. A score closer to 1 generally indicates a better fit.

The notebook also calculates RMSE, the square root of MSE.

## Results

| Metric | Degree 1 | Degree 2 |
|---|---:|---:|
| MSE | 46.5446 | 1.6896 |
| RMSE | 6.8224 | 1.2999 |
| MAE | 6.3365 | 1.0804 |
| R² Score | 0.9726 | 0.9990 |

## Conclusion

On this test dataset, **Degree 2 outperforms Degree 1 across all four reported metrics**. Its R² Score is closer to 1, while its MSE, RMSE, and MAE are lower.

This experiment demonstrates how polynomial feature engineering can improve regression performance by capturing nonlinear relationships that a standard linear model may not represent.

The results are specific to this small test dataset and do not guarantee that a higher polynomial degree will always perform better.

## Technologies

- Python
- NumPy
- Matplotlib
- Scikit-learn
- Linear Regression
- Polynomial Feature Engineering
- Regression Evaluation Metrics
### ّMore info on Metrics refer to my post on Linkedin https://lnkd.in/p/ddQjvgHx
