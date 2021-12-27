
# Module 3 Final Project


## Overview 

Our client, SyriaTel, is a telecommunication company and is suffering from a loss of valuable customers to competitors.

Understanding customer churn is essential to evaluating the effectiveness of the company’s marketing efforts and the overall satisfaction of the customers. It’s also easier and less expensive to keep existing customers versus to acquire new ones.

Therefore, we are hired to help the management team understand what features are primary determinants of the customer churn. We will further build a classification model to predict whether a customer will (“soon”) stop doing business with SyriaTel.


## Objectives

- Perform exploratory data analysis on current data. The raw data is downloaded from Kaggle.
- Build up baseline model: logistic regression
- Apply multiple machine learning algorithms to build classifier: K-Nearest Neighbors, Decision Trees, Random Forest, AdaBoost, Gradient Boost, XGBoost, and Support Vector Machine
- Select the best model for classification


## Project Summary

### Exploratory Data Analysis

1. Current Churn Rate = 14.5%

2. Churn vs International Plan and Voice Mail Plan

![](https://github.com/carlearn/dsc-mod-3-project-v2-1/blob/master/charts/churn%20vs%20intl%20plan%20and%20voice%20mail%20plan.png)

3. Churn vs Customer Service Calls

![](https://github.com/carlearn/dsc-mod-3-project-v2-1/blob/master/charts/churn%20vs%20customer%20service%20calls.png)

4. Churn vs Average Monthly Charge

![](https://github.com/carlearn/dsc-mod-3-project-v2-1/blob/master/charts/churn%20vs%20average%20monthly%20charge.png)

5. Churn vs Average Total Day Minutes

![](https://github.com/carlearn/dsc-mod-3-project-v2-1/blob/master/charts/churn%20vs%20average%20total%20day%20minutes.png)


### Baseline Model

We built our baseline model following the below process:
(1) Set target variable, features (using one-hot encoding on state), and train / test split
(2) Instantiate a Logistic Regression
(3) Preprocess the model with StandardScaler and SMOTE:
(4) Reduce regularization
(5) Alternative solver, using saga.
(6) Adjusting gradient descent parameters

The results (Confusion Matrix) are:

![](https://github.com/carlearn/dsc-mod-3-project-v2-1/blob/master/charts/Confusion%20Matrix%20of%20Baseline%20Model%20-%20Logistic%20Regression.png)


### Classification Methods

We applied K-Nearest Neighbors, Decision Tree, Random Forest, Boosting Strategies (including AdaBoost, Gradient Boost, XGBoost) and Support Vector Machine.


### Best Model - XGBoost

According to the recall score, weighted f1 score and especially the amount of AUC, XGBoost is the best classifier we want to choose for the churn prediction model. We further tuned the model with GridSearch CV.

The final results (Confusion Matrix) are:

![](https://github.com/carlearn/dsc-mod-3-project-v2-1/blob/master/charts/Confusion%20Matrix%20of%20Final%20Model%20-%20Tuned%20XGBoost.png)


### Primary Determinants of Churn (Feature Importance)

![](https://github.com/carlearn/dsc-mod-3-project-v2-1/blob/master/charts/Feature%20Importance%20-%20Top%2010%20primary%20determinants%20of%20churn.png)


### Recommendations and Next Steps

1. Market research on competitors and industry benchmark - Pricing Strategy
2. Customer experience measurement and design
3. Partnership with local carriers


## Final Deliverables

1. [Technical Codes on Jupyter Notebook](https://github.com/carlearn/dsc-mod-3-project-v2-1/blob/master/student.ipynb)

2. [Business Presentation](https://github.com/carlearn/dsc-mod-3-project-v2-1/blob/master/SyriaTel%20Churn%20Analysis.pdf)

3. [Blog re SyriaTel Churn Analysis](https://medium.com/@carrielearn/syriatel-churn-analysis-bc2de1574968)

