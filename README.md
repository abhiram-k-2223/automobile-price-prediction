# Automobile Price Prediction

This project aims to predict the price of automobiles based on various features such as symboling, normalized-losses, num-of-doors, wheel-base, curb-weight, num-of-cylinders, engine-size, bore, stroke, compression-ratio, horsepower, peak-rpm, city-mpg, highway-mpg, drive-wheels, aspiration, fuel-type, body-style, engine-type, and fuel-system.

## Data Preprocessing

The code starts by importing the necessary libraries and reading the automobile dataset from a CSV file. It then performs the following data preprocessing steps:

1. Drops irrelevant columns such as 'make', 'length', 'width', 'height', and 'engine-location'.
2. Handles missing values in specific columns by imputing them with appropriate values.
3. Converts data types of certain columns to their appropriate types (e.g., 'horsepower' to int, 'peak-rpm' and 'stroke' to float).
4. Converts the 'num-of-cylinders' column from word representation to numerical representation using the `word2number` library.
5. Removes duplicate rows from the dataset.

## Feature Engineering

The code then performs feature engineering by splitting the features into different categories:

- Scaling features: Features that need to be scaled using Standard Scaler.
- Ordinal categorical feature: Features with an inherent ordering (e.g., 'drive-wheels').
- Missing features: Features with missing values that need to be imputed.
- Nominal categorical features: Features without any inherent ordering (e.g., 'aspiration', 'fuel-type', 'body-style', 'engine-type', 'fuel-system').

## Model Building

The code sets up a pipeline using `scikit-learn` to preprocess the data and build a linear regression model for predicting the price. The pipeline consists of the following steps:

1. Imputation of missing values using KNN Imputer.
2. Scaling of numerical features using Standard Scaler.
3. One-Hot Encoding of nominal categorical features.
4. Ordinal Encoding of ordinal categorical features.
5. Linear Regression model for prediction.

The dataset is split into training and testing sets using `train_test_split` from `scikit-learn`. The model is then trained on the training set, and predictions are made on the test set. Finally, the coefficient of determination (R-squared) is calculated to evaluate the model's performance.

## Usage

To run the code, you need to have the following dependencies installed:

- pandas
- scikit-learn
- word2number

You can install them using pip:
 ```bash
    pip install pandas scikit-learn word2number
```
Once you have the dependencies installed, you can run the code by executing the Python script or Jupyter Notebook containing the code.

## Contributing

Contributions to this project are welcome. If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.
