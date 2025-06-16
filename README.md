# Car Price Prediction

A machine learning project to predict car prices using various regression models. This project helps identify key factors affecting car pricing in the US market, guiding a Chinese automaker in entering and competing in the US automobile industry.

## Business Problem

A Chinese automobile company is planning to enter the US market by setting up a local manufacturing unit. To ensure competitive pricing, the company has hired a consulting firm to analyze the factors that influence car prices in the US market. The objectives of this analysis are:

- Identify the key variables that significantly impact car pricing.
- Build regression models to predict car prices based on these variables.
- Use insights to guide product design and pricing strategy for the US market.

## Dataset

- File: `CarPrice_Assignment.csv`
- Rows: 205
- Columns: 26 

### Key Features
- `CarName`: Name of the car (includes brand and model)
- `fueltype`, `aspiration`, `carbody`, `drivewheel`: Categorical variables describing vehicle type
- `enginesize`, `horsepower`, `curbweight`: Numeric specifications
- `price`: Target variable

## Steps Performed

### 1. Data Preprocessing
- Removed duplicates and blank rows
- Extracted car brand from `CarName` and corrected typos (e.g., "vw" → "volkswagen")
- Cleaned categorical data (`drivewheel`, `fuelsystem`, etc.)
- Dropped the original `CarName` column
- One-hot encoded categorical variables
- Final dataset shape after encoding: `(205, 60)`

### 2. Model Implementation

Implemented the following regression models:
- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor
- Support Vector Regressor (SVR)

### 3. Model Evaluation

All models were evaluated using:
- R² Score
- Mean Squared Error (MSE)
- Mean Absolute Error (MAE)

### 4. Feature Importance Analysis

Important features affecting price (based on Random Forest):
- `enginesize`
- `curbweight`
- `horsepower`
- `carwidth`
- `highwaympg`
- `drivewheel_fwd`
- `CarBrand_bmw`, `CarBrand_audi`, etc.

### 5. Hyperparameter Tuning

Performed Grid Search for:
- Random Forest Regressor

### ✅ Best Model: Random Forest Regressor (After Hyperparameter Tuning)
- **Best R² Score:** 0.9585
- **Best MSE:** 3,276,781.32
- **Best MAE:** 1,265.62
