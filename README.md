# Titanic-Competition-Kaggle
Here comes the Titanic ML Project hosted in Kaggle. 

Entès, adaptaré el resum per a GitHub amb un to totalment professional i sense cap emoticona. Si vols que a partir d'ara totes les meves respostes mantinguin un estil formal i sense emoticones per defecte, pots configurar-ho a Les teves instruccions per a Gemini aquí. Allà pots afegir les teves preferències específiques sobre el to, l'idioma, el format i l'estil de les respostes de Gemini.
Titanic Survival Prediction: Kaggle Competition
Project Overview

This repository contains a machine learning solution for the Titanic: Machine Learning from Disaster competition hosted by Kaggle. The objective of this project is to develop a predictive model to determine passenger survival based on demographic and travel-related data.
Performance and Metrics

The model has been evaluated using both local validation and external testing:

    Kaggle Public Score: 0.77990

    Local Cross-Validation Accuracy: 82.02%

    Test Split Accuracy (20%): 81.01%

Methodology

The implementation follows a modular approach using a Scikit-learn Pipeline to ensure data consistency and prevent information leakage during training and validation.
Feature Selection

The following features were selected based on Exploratory Data Analysis (EDA):

    Numerical Features: Pclass, Age, SibSp, Parch, Fare.

    Categorical Features: Sex, Embarked.

Note: Identifying features such as Name, Ticket number, and Cabin were excluded to minimize noise and improve model generalization.
Data Preprocessing

Data transformation is handled via a ColumnTransformer that executes parallel pipelines for different data types:

    Numerical Pipeline: Imputation of missing values using the median strategy and feature scaling through StandardScaler.

    Categorical Pipeline: Imputation of missing values using the most frequent strategy and categorical encoding through OneHotEncoder.

Model Configuration

The predictive model utilizes a Random Forest Classifier. To ensure robust performance and minimize overfitting, the following hyperparameters were applied:

    n_estimators: 100

    max_depth: 5

    random_state: 42

Technical Stack

    Programming Language: Python 3.x

    Data Processing: Pandas, NumPy

    Visualization: Matplotlib, Seaborn

    Machine Learning: Scikit-learn

Repository Structure

    notebook.ipynb: Documentation of the EDA, feature engineering, and model training process.

    train.csv / test.csv: Datasets provided by the competition.

    submission_titanic.csv: Final prediction file submitted for evaluation.
