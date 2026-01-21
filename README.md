# Car Price Prediction Using Ridge Regression with Snowflake Integration

## Overview
This project focuses on predicting car prices using a machine learning regression approach.  
Data is fetched directly from a Snowflake data warehouse and processed using a complete preprocessing and modeling pipeline built with scikit-learn.

The goal of this project is to demonstrate:
- Database integration with Snowflake
- Feature preprocessing for numerical and categorical data
- Regression modeling using Ridge Regression
- Model evaluation using standard regression metrics

---

## Technologies Used
- Python
- Pandas, NumPy
- Snowflake Connector for Python
- Scikit-learn
- Ridge Regression
- OneHotEncoder & StandardScaler

---

## Dataset
- Source: Snowflake Data Warehouse
- Table contains car-related attributes such as specifications and categorical features
- Target variable: **PRICE**
- Identifier column (**CAR_ID**) is removed before training

---

## Project Workflow

1. Connect to Snowflake and load data
2. Drop unnecessary identifier columns
3. Split data into features (X) and target (y)
4. Identify numerical and categorical columns
5. Apply preprocessing:
   - Standard scaling for numerical features
   - One-hot encoding for categorical features
6. Build a machine learning pipeline
7. Train Ridge Regression model
8. Evaluate model performance

---

## Model Used
**Ridge Regression**

Ridge Regression is chosen to handle multicollinearity and prevent overfitting by applying L2 regularization.

---

## Evaluation Metrics
The model is evaluated using:
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

These metrics help measure prediction accuracy and model reliability.

---

## Results
The trained model successfully predicts car prices with reasonable accuracy based on the given features.  
Performance metrics are printed after evaluation on the test dataset.

---

## How to Run the Project

1. Install required dependencies:
   ```bash
   pip install pandas numpy scikit-learn snowflake-connector-python
