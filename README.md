# Titanic Survival Prediction

## Overview
This project predicts whether a passenger survived the Titanic disaster using machine learning techniques. It includes data preprocessing, feature engineering, multiple classification models, model evaluation, and explainability.

## Dataset
- Titanic Survival Dataset
- Source: Kaggle

## Features Used
- Pclass
- Sex
- Age
- SibSp
- Parch
- Fare
- Embarked
- Title (Extracted from Name)
- FamilySize
- CabinPresent

## Feature Engineering
- Extracted passenger titles from the Name column.
- Created a FamilySize feature using SibSp + Parch + 1.
- Created a CabinPresent feature to indicate whether cabin information is available.

## Missing Value Handling
- Filled missing Age values using the median.
- Filled missing Embarked values using the mode.
- Used Cabin information to create the CabinPresent feature.

## Models Used
- Logistic Regression
- Random Forest Classifier
- Gradient Boosting Classifier

## Model Explainability
- SHAP Explainability
- Random Forest Feature Importance

## Evaluation Metrics
- Accuracy
- Classification Report
- Confusion Matrix

## Saved Model
The trained Random Forest model is saved as:

```
Titanic_Model.pkl
```

## Inference Example

```python
import joblib
import pandas as pd

model = joblib.load("Titanic_Model.pkl")

sample = X.iloc[[0]]
prediction = model.predict(sample)

print(prediction)
```

## Project Structure

```
Titanic-Survival-Prediction/
│── Titanic_Survival_Prediction.ipynb
│── Titanic_Model.pkl
│── README.md
```

## Author

Ankit Singh Bungla
