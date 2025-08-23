# House Price Prediction (Advanced Linear Regression and Deep learning)

## 📊 Surprise Housing Case Study

### Overview

Surprise Housing, a US-based real estate analytics firm, is expanding into the Australian market. To identify undervalued properties for profitable resale, the company has collected housing sales data from Australia. This project aims to build predictive models using regularized regression techniques to estimate actual house prices and guide investment decisions.

## 🎯 Business Objective
Predict the actual sale price of prospective properties using available features.

Identify key variables influencing house prices.

Determine optimal regularization parameters (λ) for Ridge and Lasso regression.

Provide actionable insights to inform Surprise Housing’s market entry strategy.

## 🧭 Project Workflow
### Data Capture

Source: CSV file containing 1,460 records and 81 features.

###  Data Understanding & EDA

Target variable: SalePrice

Visualize relationships and correlations using heatmaps.

Key correlated pairs:

        GarageYrBuilt_Age ↔ YearBuilt_Age

        GrLivArea ↔ TotRmsAbvGrd

        GarageArea ↔ GarageCars

### Data Cleaning

Handle missing values using SimpleImputer:

    Categorical: impute with 'NA'

    Numerical: impute with mean

###  Data Preparation

Normalize skewed target variable (SalePrice)

Generate dummy variables for categorical features

Final feature set: 273 columns

###  Model Building & Evaluation

Ridge Regression

    Optimal λ: 571.85

    R² (Train): 0.89

    R² (Test): 0.93

    Top predictors:

        LotFrontage

        BsmtFullBath

        2ndFlrSF

        1stFlrSF

        OverallQual_Fair

Lasso Regression

    Optimal λ: 0.001

    R² (Train): 0.90

    R² (Test): 0.93

    Top predictors:

        LotFrontage

        BsmtFullBath

        1stFlrSF

        OverallQual_Fair

        OverallQual_Very Poor

## Summary & Insights

Both Ridge and Lasso models demonstrate strong predictive performance.

Regularization effectively handles multicollinearity and feature selection.

Key features like frontage, basement baths, and floor area are consistent indicators of price.

## 🛠 Technologies Used
Python (pandas, scikit-learn, matplotlib, seaborn)

Regression Techniques: Ridge, Lasso

Data Imputation: SimpleImputer

Feature Engineering: One-hot encoding, log transformation