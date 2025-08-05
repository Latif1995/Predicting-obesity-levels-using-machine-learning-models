# Predicting obesity levels using machine learning models

## Table of Content


### Project Overview
---
Obesity has been linked with numerous diseases including cardiovascular infections, diabetes, kidney problems, as well as psychological problems such as depression, anxiety etc. Therefore, there is an urgent need for early detection of individuals at high  risk of becoming obese. This project therefore aims at building machine learning models to predict levels of obesity. This will aid in earlier identification of individuals who are likely to become obese in order to provide them with the needed support.

### Data Sources
The data for this project is from Nikhita et al.(2024). The dataset contains 2111 cases and 17 variables. These variables covers data about demographics, lifestlye factors, physical activities,and dietary patterns. For more information about the data, readers should consult Nikhita et al.(2024). Also, to download the data, readers should visit [UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/dataset/544/estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition).

### Tools
- Python
   - Data manipulation
   - Building Machine Learning Models
  
### Data Cleaning
During the initial preparation of the data, we performed the tasks below:

- Data Loading and inspection
- Checking for missing data in tne variables of interest
- Renaming variables
- Creating dummy variables for the categorical predictors using one-hot encoding: ``` pd.get_dummies()```
- Merging some of the sub-categories with few cases for some of the categorical predictors

### Data Preprocessing
- Splitting the data into testing and training datasets
- Standardizing the continuous features in the testing and training datasets seperately to prevent any information leakage from the testing to the training data using ```StandardScaler()``` function.
- For the datasets with binary and ordinal outcomes, SMOTE was employed to handle class imbalances.
- To predict students mathematics performance, the eight machine learning models below were utilzed:

  - Linear regression (for the continuous target variable) and logistic regression (for the ordinal and binary target variables)
  - Decision Tree
  - Random Forest
  - Gradient Boosting
  - Support Vector Machine
  - Lasso regression
  - Ridge regression
  - Elastic Net regression

### Model evaluation
The models were evaluated using the following metrics:
- Precision, recall, and Accuracy metrics were used to evaluate predictive performance of the models in the analysis of the data with binary target variable.

### Results
The Random Forest algorithm produced the highest predictive performance (i.e., accuracy) with a value of 0.8132, follwed by the Support Vector Machine algorithm with an accuracy value of 0.8085.

<img width="1000" height="600" alt="comparing the performance of the models" src="https://github.com/user-attachments/assets/04f3163e-25c7-4f77-9b45-5385fbf9c87e" />

### Variable importance
By examining variable importance in models such as the Decision tree, Random forest, Lasso, Ridge, and Elastic Net, the following variables showed up as the most important variables in predicting level of obesity:
- Age
- Gender
- Frequency of vegatable consumption in meals
- Number of main meals consumed daily
- Daily water consumption
- Frequency of physical activity per week
- Time spent using technological devices daily
- Frequency of alcohol consumption
- Family history with overweight

### Recommendations
- Individuals should ferquently be screened in early stages of their life to identify those who are likely to be be obese.
- Adequate support and advice should be provided to the identified individual to limit their chances of becoming obese.
- Efforts should be made to encourage individuals to exercise frequently.

### Limitations
There are other important predictors including eating late in the night, education level, occupation, etc., which were not captured in the study. These are important variables that can help predict the obesity levels. Therefore, future studies should consider capturing data on some of these variables.

### References
1. Nikhita, G. N., Varma, P. S., Teja, S. P., & Rao, G. S. (2024, December). Obesity level prediction using ML based on eating habits and physical condition. In 2024 9th International Conference on Communication and Electronics Systems (ICCES) (pp. 1811-1816). IEEE.
2. Hastie, T., Tibshirani, R., & Friedman, J. (2009). An introduction to statistical learning.
3. [SKlearn](https://scikit-learn.org/stable/).
