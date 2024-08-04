# Predicting Insurance Charges

## Project Overview

Dive into the heart of data science with a project that combines healthcare insights and predictive analytics. As a Data Scientist at a top Health Insurance company, this project aims to predict customer healthcare costs using the power of machine learning. These insights will help tailor services and guide customers in planning their healthcare expenses more effectively.

## Dataset Summary

### `insurance.csv`
This dataset contains information on health insurance customers, which is crucial for uncovering patterns in healthcare costs. The dataset includes the following columns:

| Column    | Data Type | Description                                                      |
|-----------|-----------|------------------------------------------------------------------|
| `age`     | int       | Age of the primary beneficiary.                                  |
| `sex`     | object    | Gender of the insurance contractor (male or female).             |
| `bmi`     | float     | Body mass index, a key indicator of body fat based on height and weight. |
| `children`| int       | Number of dependents covered by the insurance plan.              |
| `smoker`  | object    | Indicates whether the beneficiary smokes (yes or no).            |
| `region`  | object    | The beneficiary's residential area in the US, is divided into four regions. |
| `charges` | float     | Individual medical costs billed by health insurance.             |

## Project Steps

### 1. Data Cleaning and Preprocessing

- **Load Dataset**: Import the `insurance.csv` dataset.
- **Handling Missing Values**: Ensure there are no missing values.
- **Feature Selection**: Select features (`age`, `sex`, `bmi`, `children`, `smoker`, `region`) and target variable (`charges`).
- **Encoding Categorical Data**: Convert categorical features (`sex`, `smoker`, `region`) into dummy variables.
- **Scaling Numerical Data**: Standardize numerical features (`age`, `bmi`, `children`) using `StandardScaler`.

### 2. Model Building

- **Model Selection**: Use Linear Regression for prediction.
- **Model Pipeline**: Create a pipeline to streamline preprocessing and model training.
  - Steps in the pipeline:
    1. Scaling numerical data.
    2. Fitting the Linear Regression model.

### 3. Model Training and Cross-Validation

- **Split Data**: Use K-Fold Cross-Validation (6 splits) to evaluate the model.
- **Performance Metrics**: Calculate Mean Squared Error (MSE) and R² score to assess model performance.

### 4. Predictions on New Data

- **Load Validation Data**: Read `validation_dataset.csv` for predictions.
- **Preprocess Validation Data**: Encode categorical features similar to the training data.
- **Predict Charges**: Use the trained model pipeline to predict insurance charges.
- **Adjust Predictions**: Set a minimum basic charge of 1000 for any predicted values below this threshold.

### 5. Evaluation and Results

- **Evaluation Metrics**:
  - Mean MSE: Calculated from cross-validation.
  - Mean R²: Calculated from cross-validation.
- **Validation Predictions**: Save predictions to the validation dataset.

## How to Run the Project

1. **Install Dependencies**:
   ```bash
   pip install pandas numpy scikit-learn
   ```
2. **Execute the Notebook**: Run all cells in the provided Jupyter Notebook to perform data cleaning, model training, cross-validation, and predictions.

## Conclusion

This project showcases the application of data science techniques to predict healthcare costs using a structured dataset. The insights gained can be used by health insurance companies to better manage customer plans and provide tailored services based on predicted expenses.
