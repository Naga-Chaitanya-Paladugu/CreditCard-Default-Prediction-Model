# Prediction of Loan Defaults
## Personal Note
This is my first Machine Learning project, developed from learning the Bayesian way of predictive modeling in my fully online degree coursework. I have gone through many reiterations and crossroads of making judgment calls at various steps during the project. Overall, I enjoyed the learning process and will improvise on my next project utilizing the lessons learned. 

Here is the link to **full detailed report** of this project: https://naga-chaitanya-paladugu.github.io/Taiwan-Credit-Default/.

Below is a **quick summary** of project's main details.
## Project Overview
This project aims to predict credit card loan defaults using a dataset from the UCI Machine Learning Repository. The dataset includes demographic details and past payment behavior of clients from Taiwan during the 2005 financial crisis.

## Dataset
- **Source**: UCI Machine Learning Repository - Default of Credit Card Clients Dataset
- **Size**: 30,000 observations, 25 variables
- **Key Variables**:
  - **Demographic Details**: Age, gender, marital status, education level
  - **Past Payment Behavior**: Payment history, bill amounts, previous default status
  - **Target Variable**: Default payment next month (Yes/No)

## Objective
To predict whether a customer will default on their loan repayment for the month of October 2005 using demographic and past payment behavior data.

## Methodology
1. **Data Preprocessing**:
   - Handled missing values
   - Adjusted variable classes
   - Created new features and transformed variables

2. **Exploratory Data Analysis (EDA)**:
   - Analyzed distributions and relationships of key variables
   - Visualized data using bar plots, histograms, and density plots

3. **Feature Engineering**:
   - Created aggregate features like average repayment status and billed-to-paid ratio

4. **Model Building**:
   - Used Bayesian logistic regression to predict loan defaults
   - Implemented two models:
     - **Model 1**: Included all available predictors
     - **Model 2**: Focused on significant predictors (Credit Limit and Average Repayment Status)

5. **Model Evaluation**:
   - Performed 10-fold cross-validation
   - Compared models using sensitivity, specificity, overall accuracy, and Expected Log-Predictive Density (ELPD)

## Key Findings
- **Significant Predictors**: Credit Limit and Average Repayment Status
- **Model Performance**:
  - **Model 1**:
    - Sensitivity: 40.8%
    - Specificity: 91.6%
    - Overall Accuracy: 71.6%
  - **Model 2**:
    - Sensitivity: 40.5%
    - Specificity: 91.7%
    - Overall Accuracy: 71.6%
  - **Cross-Validation (10-fold)**:
    - **Model 1**:
      - Sensitivity: 75.6%
      - Specificity: 56.0%
      - Overall Accuracy: 63.7%
    - **Model 2**:
      - Sensitivity: 74.3%
      - Specificity: 59.9%
      - Overall Accuracy: 65.5%
  - **Expected Log-Predictive Density (ELPD)**:
    - Model 1: Higher ELPD, but within the two standard error range of Model 2
    - Model 2: Slightly lower ELPD, indicating comparable performance to Model 1

## Conclusions
- **Predictive Power**: Average Repayment Status is a stronger predictor than demographic factors
- **Model Choice**: Model 2 is better over 1 as it is built with reduced features that were found to have more predictive power from model 1 and gives almost same performance as the model1 does.
- **Implications**: The model can help financial institutions identify potential defaulters and manage credit risk more effectively

## Future Work
- Explore the impact of economic factors on default rates
- Incorporate behavioral data such as spending habits and financial literacy

