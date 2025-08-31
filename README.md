Heart Disease Prediction using Decision Trees and Random Forest

📌 Project Overview

This project applies Decision Tree and Random Forest classifiers to predict the presence of heart disease based on basic patient health parameters:

Age

Sex

Blood Pressure (BP)

Cholesterol

The objective is to compare single-tree models with ensemble methods, analyze feature importance, and evaluate model performance after hyperparameter tuning.

📂 Dataset

The dataset used contains patient records with the following features:

Feature	Description
age	Age of the patient (years)
sex	Gender (1 = male, 0 = female)
BP	Resting blood pressure
cholestrol	Serum cholesterol level
heart disease	Target variable (1 = disease, 0 = no disease)
⚙️ Methods

Exploratory Data Analysis (EDA):

Examined distributions of age, cholesterol, and blood pressure.

Visualized relationships between features and heart disease occurrence.

Model Building:

Decision Tree Classifier (baseline model).

Random Forest Classifier (ensemble method).

Hyperparameter Tuning:

Performed using GridSearchCV on parameters such as:

max_depth

min_samples_leaf

max_features

n_estimators

Model Evaluation:

Accuracy, Confusion Matrix, Classification Report.

Compared Train vs Test performance to check for overfitting/underfitting.

Feature Importance Analysis:

Identified which factors contributed most to heart disease prediction.

📊 Results
Decision Tree

Train Accuracy: ~72%

Test Accuracy: ~62%

Struggled with overfitting and limited generalization.

Random Forest (after tuning)

Best Parameters:

max_depth=5, 
min_samples_leaf=5, 
max_features=3, 
n_estimators=30


Train Accuracy: ~80%

Test Accuracy: ~80%

Much better balance between bias and variance.

Feature Importances
Feature	Importance
Age	39%
Cholesterol	22%
Sex	20%
Blood Pressure	18%
✅ Conclusion

Random Forest significantly outperformed the single Decision Tree, achieving ~80% accuracy on test data.

Age was found to be the most critical predictor, followed by Cholesterol and Sex.

Results align with medical knowledge, strengthening the interpretability of the model.

Ensemble learning (Random Forest) is highly effective for healthcare-related classification problems.
