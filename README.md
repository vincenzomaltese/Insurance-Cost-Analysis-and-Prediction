# Project: Medical Insurance Cost Analysis and Prediction

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.2.2-orange)
![Pandas](https://img.shields.io/badge/Pandas-1.5.3-red)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7.1-green)

## Overview

This project analyzes and predicts insurance costs using Python and machine learning techniques. It aims to identify key factors influencing insurance charges and develop predictive models.

## Project Objectives

The main objectives are:

*   **Data Handling**: Load and clean the insurance cost dataset, addressing missing data and ensuring data integrity.
*   **Exploratory Data Analysis (EDA)**: Explore the dataset to understand feature relationships and identify attributes affecting insurance charges.
*   **Predictive Modeling**: Build and evaluate linear regression models for predicting insurance costs.
*   **Model Refinement**: Improve model performance using Ridge Regression and polynomial features.

## Dataset

The project uses the `medical_insurance_dataset.csv` dataset, included in this repository. This dataset contains patient information and insurance charges, with the following features:

| Parameter         | Description                                | Content type         |
| ----------------- | ------------------------------------------ | -------------------- |
| `age`             | Age of the insured person in years         | Integer              |
| `gender`          | Gender of the insured person (1 for Male, 2 for Female) | Integer (1 or 2)     |
| `bmi`             | Body mass index of the insured person        | Float                |
| `no_of_children`  | Number of children covered by insurance    | Integer              |
| `smoker`          | Smoking status (0 for Non-smoker, 1 for Smoker) | Integer (0 or 1)     |
| `region`          | U.S. geographic region (1: NW, 2: NE, 3: SW, 4: SE) | Integer (1, 2, 3, or 4)|
| `charges`         | Annual insurance charges in USD            | Float                |

Further details on data processing and feature usage are available in the Jupyter Notebook.

## Methodology

The project follows these key steps:

1.  **Data Loading and Cleaning**:
    *   Load the `medical_insurance_dataset.csv` using `pandas`.
    *   Handle missing values by imputation, using mean for continuous `age` and most frequent value for categorical `smoker`.
    *   Correct data types and format the `charges` column.

2.  **Exploratory Data Analysis (EDA)**:
    *   Visualize relationships between features and `charges` using regression and box plots.
    *   Calculate and analyze the correlation matrix.

3.  **Model Development**:
    *   Develop and evaluate Linear Regression models:
        *   Simple Linear Regression (using `smoker` only).
        *   Multiple Linear Regression (using all features).
        *   Pipeline model with `StandardScaler`, `PolynomialFeatures`, and `LinearRegression`.

4.  **Model Refinement with Ridge Regression**:
    *   Split data into training and testing sets (80/20 split).
    *   Implement Ridge Regression to refine linear models and improve generalization, including using polynomial features.

5.  **Libraries Used**:
    *   `pandas`, `numpy`, `seaborn`, `matplotlib`, `scikit-learn` (details in the previous version).

## Results

*   **Exploratory Data Analysis**: Key insights included the impact of smoking status and BMI on insurance charges, as detailed in the correlation matrix and visualizations.

*   **Model Performance (R² Scores)**:  Model performance progressively improved with complexity, with the Ridge Regression model using polynomial features achieving the best R² score on the test set (approximately 0.78). For specific R² scores of each model, please refer to the Jupyter Notebook.

## Conclusion

The project demonstrates successful prediction of insurance costs using refined linear regression models. Ridge Regression with polynomial features offered the best performance. Future work could explore more advanced models and feature engineering for further improvement.




