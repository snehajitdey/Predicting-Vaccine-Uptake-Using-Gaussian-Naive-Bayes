# Probability_GaussianNB_vaccine
# Vaccine Prediction Project

This project aims to predict how likely individuals are to receive their xyz and seasonal flu vaccines using Gaussian Naive Bayes and evaluate the predictions using ROC AUC scores.

## Table of Contents
- [Project Overview](#project-overview)
- [Tech Stack](#tech-stack)
- [Data Preprocessing](#data-preprocessing)
- [Model Training](#model-training)
- [Evaluation](#evaluation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
The goal of this project is to predict the probabilities of individuals receiving the xyz and seasonal flu vaccines based on their survey responses. The model predicts two probabilities: one for `xyz_vaccine` and one for `seasonal_vaccine`.

## Tech Stack
- **Python**: Programming language used for developing the project.
- **Pandas**: Used for data manipulation and analysis.
- **Scikit-learn**: Machine learning library used for:
  - `GaussianNB`: Gaussian Naive Bayes classifier.
  - `roc_auc_score`: To calculate the Area Under the Receiver Operating Characteristic Curve (ROC AUC).
  - `LabelEncoder` and `OneHotEncoder`: For encoding categorical variables.
  - `ColumnTransformer` and `Pipeline`: For creating data preprocessing and modeling pipelines.
- **Numpy**: Used for numerical operations.

## Data Preprocessing
The data preprocessing steps include:
- Merging training and test datasets on `respondent_id`.
- Handling missing values using `SimpleImputer`.
- Encoding categorical variables using custom transformers (`LabelEncoder` for binary and ordinal features, `OneHotEncoder` for nominal features).
- Using `ColumnTransformer` to combine different preprocessing steps.

## Model Training
The model is trained using the Gaussian Naive Bayes algorithm. Separate pipelines are created for predicting `xyz_vaccine` and `seasonal_vaccine` probabilities.

## Evaluation
The model's performance is evaluated using the ROC AUC score, which measures the ability of the classifier to distinguish between classes. The mean of the ROC AUC scores for `xyz_vaccine` and `seasonal_vaccine` is calculated to get the overall score.

## Usage
To run the project:
1. Clone the repository:
   ```bash
   git clone https://github.com/tan-war/Probability_GaussianNB_vaccine.git
   cd vaccine-prediction
