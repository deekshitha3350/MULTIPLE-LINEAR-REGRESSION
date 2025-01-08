# MULTIPLE-LINEAR-REGRESSION
# Multiple Linear Regression Analysis for Toyota Corolla Dataset

This repository contains a Python script to perform multiple linear regression analysis on the Toyota Corolla dataset. The analysis involves predicting the price of Toyota Corolla cars based on various attributes such as age, mileage, fuel type, and more. The script includes data preprocessing, exploratory data analysis (EDA), model training, and evaluation of multiple regression models.

## Dataset Description

The dataset consists of the following variables:

- **Age**: Age of the car in years
- **KM**: Accumulated kilometers on the odometer
- **FuelType**: Fuel type (Petrol, Diesel, CNG)
- **HP**: Horsepower
- **Automatic**: Whether the car is automatic (Yes=1, No=0)
- **CC**: Cylinder volume in cubic centimeters
- **Doors**: Number of doors
- **Weight**: Weight in kilograms
- **Quarterly_Tax**: Quarterly tax in Euros
- **Price**: Offer price in Euros (target variable)

## Steps Performed

### 1. Data Loading and Exploration

- Load the dataset using `pandas`.
- Display the first few rows of the dataset.
- Check for missing values and data types.
- Display summary statistics.

### 2. Exploratory Data Analysis (EDA)

- Generate a correlation heatmap to visualize relationships between numerical features.
- Visualize the distribution of important variables.

### 3. Data Preprocessing

- Handle missing values by replacing them with median values.
- Convert categorical variables (e.g., `FuelType`) to dummy variables using one-hot encoding.
- Standardize numerical features using `StandardScaler`.

### 4. Train-Test Split

- Split the dataset into training (80%) and testing (20%) sets.
- Ensure proper encoding of categorical variables using `LabelEncoder` where necessary.

### 5. Model Building and Evaluation

#### Model 1: Linear Regression

- Train a basic linear regression model using all features.
- Evaluate the model using:
  - Mean Squared Error (MSE)
  - R-squared Score

#### Model 2: Linear Regression with Selected Features

- Train a linear regression model using selected features (`Age`, `KM`, `HP`, `Weight`).
- Handle warnings for missing features in the training set.
- Evaluate the model performance using MSE and R-squared Score.

#### Model 3: Polynomial Regression

- Apply polynomial feature transformation (degree=2) to the dataset.
- Train a linear regression model using the transformed features.
- Evaluate the model performance using MSE and R-squared Score.

#### Model 4: Lasso Regression

- Train a Lasso regression model with an alpha value of 0.1 to apply L1 regularization.
- Evaluate the model performance using MSE and R-squared Score.

## Results

- **Linear Regression (Model 1)**: Baseline model using all features.
- **Selected Features Regression (Model 2)**: Improved model using a subset of features.
- **Polynomial Regression (Model 3)**: Enhanced performance with polynomial terms.
- **Lasso Regression (Model 4)**: Regularized model to prevent overfitting.

## Prerequisites

- Python 3.x
- Libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `scikit-learn`

## How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/toyota-corolla-regression.git
   ```
2. Navigate to the project directory:
   ```bash
   cd toyota-corolla-regression
   ```
3. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the script:
   ```bash
   python analysis.py
   ```

## Conclusion

This analysis demonstrates the steps to build and evaluate multiple linear regression models for predicting car prices. Regularization techniques like Lasso regression further enhance the model's robustness by mitigating overfitting.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
