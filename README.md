# IKEA Price Analysis

Python project analyzing IKEA furniture prices: data cleaning, hypothesis testing and price prediction models.

## Data

- IKEA product data

## Data cleaning

- Removed duplicate products
- Cleaned and normalized designer names
- Filled missing dimensions (depth, height, width) with median values
- Converted old prices from text to numbers

## Key findings

- Width has the strongest link to price among product dimensions
- Products with color options are more expensive (median 695 vs 476 SR).
- Median price differs significantly between categories

## Price prediction

Compared three models using a scikit-learn Pipeline
(imputation, scaling, one-hot encoding):

| Model | R² |
|---|---|
| Linear Regression | 0.60 |
| Random Forest | 0.79 |
| Gradient Boosting | 0.78 |

- Best model: Random Forest 
  **R² = 0.80** 
- The model is stable (5-fold cross-validation)
- Width is the most important feature (61% of total importance)

## Tools

Python, pandas, NumPy, Matplotlib, Seaborn, SciPy, scikit-learn, Jupyter
