
# Titanic Survival Prediction Project

This project aims to predict the survival of passengers aboard the Titanic using machine learning techniques. The dataset used for this project is provided by Kaggle.

## Project Overview

The objective of this project is to analyze the Titanic dataset, perform necessary data cleaning and feature engineering, build a predictive model, and visualize the results. The main goal is to predict whether a passenger survived or not based on various features such as age, gender, ticket class, etc.

## Table of Contents

- [Installation](#installation)
- [Data Exploration and Cleaning](#data-exploration-and-cleaning)
- [Feature Engineering](#feature-engineering)
- [Visualization and Insights](#visualization-and-insights)
- [Model Building and Evaluation](#model-building-and-evaluation)
- [Predictions and Submission](#predictions-and-submission)
- [License](#license)

## Installation

To get started, clone this repository and install the required dependencies.

```bash
git clone https://github.com/Lourdhu02/titanic_survival_prediction
cd titanic_survival_prediction
pip install -r requirements.txt
```

## Data Exploration and Cleaning

1. **Loading Data**: Imported the training and test datasets using `pandas`.
2. **Data Exploration**:
   - Checked the structure and basic statistics of the data using `.info()` and `.describe()`.
   - Identified missing values in the dataset using `.isnull().sum()`.
3. **Data Cleaning**:
   - Filled missing values for the 'Age' feature with the median age.
   - Filled missing values for the 'Embarked' feature with the mode.
   - Filled missing values for the 'Fare' feature in the test set with the median fare.
   - Dropped the 'Cabin' feature due to a high number of missing values.
   - Converted categorical features ('Sex' and 'Embarked') into numerical values for model training.

## Feature Engineering

1. **Selected Features**: Chose the following features for model training: `Pclass`, `Sex`, `Age`, `SibSp`, `Parch`, `Fare`, `Embarked`.
2. **Created New Features**:
   - **Family Size**: Combined `SibSp` and `Parch` to create a new feature representing family size.
   - **Title Extraction**: Extracted titles from the 'Name' feature to capture social status.

## Visualization and Insights

Visualizations were created to understand the patterns and relationships in the data. Some key insights include:
1. **Survival Count**: Visualized the count of survivors vs. non-survivors.
2. **Survival Rate by Gender**: Showed that females had a higher survival rate than males.
3. **Survival Rate by Passenger Class**: Indicated that passengers in higher classes (1st class) had better survival rates.
4. **Age Distribution**: Analyzed the age distribution of survivors and non-survivors.
5. **Fare Distribution**: Visualized fare distribution by passenger class and its impact on survival.

## Model Building and Evaluation

1. **Data Splitting**: Split the training data into training and validation sets for model evaluation.
2. **Model Selection**:
   - Chose the Random Forest Classifier for its robustness and ability to handle feature importance.
   - Trained the model using the training dataset.
3. **Model Evaluation**:
   - Evaluated the model's performance on the validation set using accuracy score.
   - Achieved an accuracy score of approximately `X.XX` on the validation set.

## Predictions and Submission

1. **Predictions on Test Set**: Used the trained Random Forest model to predict survival on the test dataset.
2. **Submission File**: Created a submission file with passenger IDs and predicted survival status.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to modify this README file to better fit your project specifics and add any additional sections or details as needed.
