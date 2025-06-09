# Predicting Car Prices 🚗💰

This project builds a predictive model to estimate car prices using linear regression. This was a project I created for my Data Exploration Course. 

## 📊 Research Question

**How do car characteristics like engine size, horsepower, MPG, curb weight, and fuel type affect the price of a car?**

This model aims to help dealerships estimate competitive car prices and identify which features contribute most to value.

## 📁 Dataset

- Source: [Kaggle - Car Price Prediction](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction)
- Size: 205 rows before cleaning
- Features used:
  - `enginesize`, `horsepower`, `highwaympg`, `curbweight`, `fueltype`
- Target variable: `price`

## 🧹 Data Cleaning

- No missing values in selected variables
- Log transformation applied to skewed variables
- `fueltype` encoded as a binary dummy variable
- Numerical features standardized using z-score scaling
- Outliers retained to preserve luxury car pricing data

## 🔍 Exploratory Analysis

- Pairplots and boxplots to assess distribution and outliers
- Correlation matrix showed strong relationships between features
- Log-transformed features helped meet linearity assumptions
- Interaction terms tested for fuel type × horsepower and engine size

## 🤖 Models Tested

1. **Linear Regression (All Features)**  
   R² (test) = 0.8307  
2. **Linear Regression + Interaction Terms**  
   R² (test) = 0.8311  
3. **Backward Feature Elimination**  
   ✅ **Best model** — R² (test) = 0.8314 (with `highwaympg` removed)


## 📌 Insights

- **Curb weight** was the most influential predictor
- **Horsepower** and **fuel type** also mattered significantly
- **Engine size** had minimal predictive power
- Multicollinearity was present between numerical features

## ⚠️ Limitations

- Only linear models tested
- No regularization techniques (e.g., LASSO, Ridge)
- Economic and brand-level variables were not included

## 🔭 Future Work

- Try LASSO or Elastic Net to improve feature selection
- Add car brand or model year
- Explore nonlinear models 

## 🧪 How to Run

> This project was developed in a Jupyter notebook in VS Code. You can run it locally with the steps below:

1. Clone the repository  
   ```bash
   git clone https://github.com/allisonprabakar12/predicting-car-prices.git
   cd predicting-car-prices```
  
2. Install Required Libraries
   ```bash
   pip install pandas numpy seaborn matplotlib scikit-learn statsmodels```
3. Launch notebook
   ```bash
   jupyter notebook```


