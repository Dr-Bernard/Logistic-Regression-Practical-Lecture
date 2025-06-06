# Logistic-Regression-Practical-Lecture
This is a lecture practical I delivered to my students on Logistics Regression

# Logistic Regression for Room Rental Prediction

This project demonstrates the application of Logistic Regression to predict whether a room should be rented based on its rent and area.

## Overview

The goal of this project is to build a classification model using Logistic Regression. The model takes two features: rent and area, and predicts a binary outcome: whether to rent the room (1: yes, 0: no).

## Dataset

The dataset `X` consists of features (rent and area) and `y` represents the corresponding labels (0: no, 1: yes).

* `X`: A list of lists, where each inner list contains `[rent, area]`.
    Example: `[[2200, 15], [2750, 20], ...]`
* `y`: A list of integers representing the labels.
    Example: `[1, 1, 0, 0, ...]`

## Steps

The project follows these steps:

1.  **Import Dependencies**: Imports necessary libraries from `sklearn`, specifically `StandardScaler` for data preprocessing and `LogisticRegression` for model building.
2.  **Define the Dataset**: The input features (`X`) and target labels (`y`) are defined.
3.  **Preprocess Data**:
    * `StandardScaler` is used to standardize the feature data. This ensures that the variance of feature data in each dimension is 1 and the mean is 0, preventing features with larger values from dominating the prediction results.
    * The `fit_transform` method is applied to the training data `X` to perform this standardization.
4.  **Fit the Data**:
    * An instance of `LogisticRegression` is created.
    * The `fit` method is used to train the logistic regression model parameters on the standardized training data (`X_train`) and the labels (`y`).
5.  **Predict the Data**:
    * A new data point (e.g., `[2000, 8]`) is defined for prediction.
    * This new data point is also standardized using the *same* `StandardScaler` instance (`ss.transform`).
    * The `predict` method of the trained `LogisticRegression` model is used to get the predicted label (0 or 1).
    * The `predict_proba` method is used to output the predicted probabilities for each class.

## How to Run

To run this project, you will need a Python environment with `scikit-learn` installed.

1.  Save the provided code as a Jupyter Notebook file (e.g., `logistic_regression_room_rental.ipynb`).
2.  Open the Jupyter Notebook and run each cell sequentially.

## Dependencies

* `sklearn` (scikit-learn)
* `numpy` (usually installed as a dependency of scikit-learn)
