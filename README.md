# credit_risk_score
This repository contains a Credit Risk Modelling project that evaluates the default risk of loan applicants using a machine learning model. It predicts the probability of default, assigns a credit score, and provides a risk rating for individuals based on their financial and personal details. The project is implemented using Streamlit for the frontend and scikit-learn for machine learning functionalities.

## Project Overview

The project comprises two main components:

Machine Learning Backend:

Prepares input features for the model using prediction_helper.py.

Utilizes a trained logistic regression model to predict default probabilities.

Scales numerical data with MinMaxScaler to ensure normalized inputs for accurate predictions.

Interactive Web Application:

Built with Streamlit (main.py).

Provides a user-friendly interface for data input and risk assessment.

Features

Backend (prediction_helper.py)

Input Preparation:

Ensures inputs match the required feature set using dummy variables for missing fields.

Scales numerical inputs with the pre-trained MinMaxScaler.

Credit Risk Calculation:

Computes the default probability using logistic regression.

Derives a credit score scaled between 300 and 900.

Assigns a risk rating (Poor, Average, Good, Excellent) based on the score.

Dynamic Prediction:

Calculates predictions on-the-fly for the given user inputs.

Frontend (main.py)

User Inputs:

Collects user data (e.g., age, income, loan amount, delinquency ratio).

Provides dropdown options for categorical variables (e.g., residence type, loan purpose).

Loan Insights:

Calculates and displays the Loan-to-Income Ratio.

Interactive Buttons:

"Calculate Risk" button processes inputs and displays:

Default Probability

Credit Score

Risk Rating

Streamlit-Based Design:

Modular and responsive layout using rows and columns.

Key Insights from Code

Feature Engineering:

New features like loan_to_income and one-hot encoded variables enhance model interpretability and prediction accuracy.

Scalability:

The use of cols_to_scale ensures that only the necessary numerical features are scaled, making it adaptable for other datasets.

Credit Scoring Logic:

The credit score system aligns with industry standards by mapping non-default probabilities to a 300-900 scale, aiding financial decision-making.

Model Performance:

Achieved AUC > 85, Gini > 85, and KS statistic > 40.

Maximum KS statistic observed in the first three deciles, ensuring strong discriminatory power.

Significant Variables:

Credit Utilization Ratio (IV = 2.35): Higher usage significantly increases default risk.

Delinquency Ratio (IV = 0.71): Strongly linked to increased default risk.

Loan-to-Income Ratio (IV = 0.47): Higher loan amounts relative to income increase default likelihood.

Average Days Past Due per Delinquency (IV = 0.40): Correlates with higher default risk.

Loan Purpose (IV = 0.36): Certain purposes are more associated with default.

Residence Type (IV = 0.24): Moderate impact on default risk.

Loan Tenure Months (IV = 0.21): Longer tenures increase default risk.

Loan Type (IV = 0.16): Minor influence on default risk.

Age (IV = 0.08): Younger or older age has minimal impact.

Number of Open Accounts (IV = 0.08): More accounts can lead to higher default risk.

Modular Structure:

prediction_helper.py separates model-related logic, ensuring clean and maintainable code.

main.py focuses on user interaction, keeping the app user-centric.

## Installation and Usage

Prerequisites

Python 3.8+

Required Python packages:

streamlit

numpy

pandas

scikit-learn

joblib
