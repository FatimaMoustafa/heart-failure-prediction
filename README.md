# heart-failure-prediction
##Overview
This project aims to build a predictive system that helps determine whether a patient is at risk of heart failure or not. Using a real dataset containing multiple medical features per patient, machine learning techniques are applied to learn from past data and predict the risk for new patients.

##Project Components
####app.py
This file contains the training script. It reads the data, preprocesses it (such as splitting into training and test sets, scaling features using StandardScaler), and trains two popular models:

Random Forest classifier

MLP (Multi-Layer Perceptron) Neural Network
After training, it saves the models, the scaler, and test data files for later use without retraining.

####gradio_app.py
This script builds an interactive user interface using the Gradio library, allowing users to input patient data easily through a web form. Upon input, the script automatically selects the best-performing model (based on test accuracy) and provides a quick, clear prediction if the patient is at risk of heart failure or not.

####heart.csv
The original dataset file containing medical information for patients, including columns like age, anaemia, creatinine levels, smoking status, and the target column DEATH_EVENT which indicates if the patient died (used for prediction).

####Model and helper files
These files are created automatically when running app.py and include:

rf_model.pkl: the trained Random Forest model

mlp_model.pkl: the trained MLP model

scaler.pkl: the StandardScaler used for feature scaling

X_test_scaled.pkl: scaled test data

y_test.pkl: actual test labels for model evaluation

