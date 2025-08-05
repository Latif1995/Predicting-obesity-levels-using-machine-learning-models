# Predicting obesity levels using machine learning models

### Project Overview
---
Obesity has been linked with numerous diseases including cardiovascular infections, diabetes, kidney problems, as well as psychological problems such as depression, anxiety etc. Therefore, there is an urgent need for early detection of individuals at high  risk of becoming obese. This project therefore aims at building machine learning models to predict levels of obesity. This will aid in earlier identification of individuals who are likely to become obese in order to provide them with the needed support.

### Data Sources
The data for this project is from Nikhita et al.(2024). The dataset contains 2111 cases and 17 variables. These variables covers data about demographics, lifestlye factors, physical activities,and dietary patterns. For more information about the data, readers should consult Nikhita et al.(2024). Also, to download the data, readers should visit [UC Irvine Machine Learning Repository].(https://archive.ics.uci.edu/dataset/544/estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition).

Tools
RStudio - Data Cleaning and Manipulation
Python - Building Machine Learning Models
Data Cleaning
During the initial preparation of the data, we performed the tasks below:

Data Loading and inspection in Rstudio
Checking for missing data in tne variables of interest
Renaming variables
creating dummy variables for the categorical predictors
Finally, exporting the data in "csv" format to be analysed using Python Programming Software
Data Preprocessing
The "csv" file was imported in Python and the following tasks were performed:

Creating three seperate datasets for each target variable (i.e., continuous, binary, and ordinal) by following the guidelines in the Paulo Cortez and Alice Silva.
Splitting the data into testing and training datasets
Standardizing the continuous features in the testing and training datasets seperately to prevent any information leakage from the testing to the training data.
For the datasets with binary and ordinal outcomes, SMOTE was employed to handle class imbalances.
Three separate notebooks were created for the three datasets, namely:
"math_continuous.ipynb" for modelling the data with continuous outcome variable
"math_binary.ipynb" for modelling the data with binary outcome variable
"math_multicategorical.ipynb" for modelling the data with multicategorical outcome variable
Data analysis
To predict students mathematics performance, the eight machine learning models below were utilzed:

Linear regression (for the continuous target variable) and logistic regression (for the ordinal and binary target variables)
Decision Tree
Random Forest
Gradient Boosting
Support Vector Machine
Lasso regression
Ridge regression
Elastic Net regression
Model evaluation
The models were evaluated using the following metrics:

R-square values were used to evaluate the predictive performance of the models in the analysis of the data with continuous target variable.
Sensitivity, Specificity, and Accuracy metrics were used to evaluate predictive performance of the models in the analysis of the data with binary target variable.
Accuracy metric was used to evaluate predictive performance of the models in the analysis of the data with multicategorical target variable.
Results
The Decision Tree algorithm produced the highest predictive performance (i.e., R_squared value) in the analysis of the data with continuous outcome
For the analysis of the data with binary target variable, the Support Vector Machine algorithm yielded the best performance accross all three evaluations metrics, namely:
Sensitivity
Specificity
Accuracy
Similarly, the Support Vector Machine algorithm yielded the best performance (;e., the highest accuracy) in the analysis of the data with multicategorical target variable


### References
1. Nikhita, G. N., Varma, P. S., Teja, S. P., & Rao, G. S. (2024, December). Obesity level prediction using ML based on eating habits and physical condition. In 2024 9th International Conference on Communication and Electronics Systems (ICCES) (pp. 1811-1816). IEEE.
2. Hastie, T., Tibshirani, R., & Friedman, J. (2009). An introduction to statistical learning.
3. [SKlearn](https://scikit-learn.org/stable/)
