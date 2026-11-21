# Salary vs Years of Experience — Simple Linear Regression

Predicting salary from years of experience with simple linear regression in Python (scikit-learn).

## Overview
This project fits a straight-line model, `salary = intercept + slope × years_of_experience`, and checks how much of the variation in salary is explained by experience alone.

## Dataset
- File: `data/salaries.csv` (100 rows, no missing values)
- Source: _add source / note if synthetic_

| Column | Description |
|---|---|
| `years_of_experience` | Years of work experience (independent variable) |
| `salary` | Salary (dependent variable) |

## Approach
1. Load the data and inspect shape, data types and missing values
2. Define X (`years_of_experience`) and y (`salary`)
3. Split 80/20 into train and test sets (`random_state=42`): 80 training rows, 20 test rows
4. Train a `LinearRegression` model
5. Predict on the test set and compare actual vs predicted salary
6. Evaluate with MSE, RMSE and R²
7. Plot the actual test points against the fitted regression line

## Results

| Metric | Value |
|---|---|
| Intercept | ≈ 2,246 |
| Coefficient (per year of experience) | ≈ 189.68 |
| MSE | 22,766.87 |
| RMSE | 150.89 |
| R² | 0.937 |

Each additional year of experience is associated with roughly 190 more in salary, and experience alone explains about 94% of the variance in the test set.

## Limitations
- Only one predictor; factors such as role, location or education are not modelled
- Evaluated on a single 20-row test split; no cross-validation
- Linearity is assumed, not tested

## Getting Started
```bash
git clone https://github.com/<your-username>/salary-vs-experience-linear-regression.git
cd salary-vs-experience-linear-regression
pip install pandas numpy matplotlib scikit-learn jupyter
jupyter notebook
```

## Repository Structure
```
├── data/
│   └── salaries.csv
├── salary_vs_experience_simple_linear_regression.ipynb
└── README.md
```

## Tech Stack
Python · pandas · NumPy · scikit-learn · Matplotlib · Jupyter

## Author
Kshitij Nareda
