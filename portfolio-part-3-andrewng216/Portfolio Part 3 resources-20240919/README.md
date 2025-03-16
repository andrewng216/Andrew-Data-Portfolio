# COMP6200: Data Secience Portfolio 3
## Overview

This repository serves the purpose of analysing loan approved data, building and evaluating predictive models from other available features for the COMP6200 Data Science unit at Macquarie University. This involves handling the dataset, building logistic regression models, identifying effective features, reporting performance metrics, studying performance change in the KNN classifier and evaluating observations and results. This portfolio primarily aims to determine how accurate those predictive models ckassify whether a loan application is approved based on remaining features.


## Task Sections
- Load the dataset, show and describe basic information
- Clean and preprocess the dataset
    - Handling missing values
    - Remove rows in categorical columns having missing values
    - Perform a missing value imputation with the average of the column for numerical columns
- Handle categorical attributes by using `OneHotEncoding` to convert into numerical values
- Build a logistic regression model
    - Specific the prediction target label and split into training and testing data
    - Train model and report two classification metrics - accuracy and F1-score
    - Perform RFE technique to identify retained features 
- Build K-NN Classification Model and discover best case of K using grid search and cross validation technique
- Visualise model performance with three distance parameters 

## Results
- After cleaning, handling categorical features using `OneHotEncoding` technique and splitting the dataset based on the prediction attribute `LoanApproved`, the model achieves slightly higher accuracy and F1-score values on testing data compared to the training data (89.6% and 0.77 vs. 88.88% and 0.75 respectively). This means that the model is not overfitting, which explains how well it has learnt to predict underlying patterns.
- Regarding the application of RFE technique with logistic regression, the optimal number of eliminated features is 20 when accuracy and F1-score rate reaches its maximum. This means there are 29 retained features in total.
- When building K-NN classifer, both accuracy and F1-score of the 1NN model (K = 1) achieve 100%, resulting in a perfect prediction performance on training data; however, those levels significantly drop on testing data, indicating the model is ovetfitting since it finds difficulty in generalising unseen data.
- To smooth out prediction performance and reduce accurate distinctions, increasing K value by using **grid search** and **cross validation technique** should be applied. In this case, **the best K value is 20** where the two performance metrics achieve their highest points since they consider more neighbours for preductions and have the most fine-grained, consistent forecasting by being less sensitive to outer variances.
- Meanwhile, using 3 distance types - `euclidean`, `l1` and `cosine` for both accuracy and F1-score, shows that `cosine` disrance has the best prediction performance in the K-NN classifer as it balances out biases and variances effectively. Although `euclidean` distance is a popular parameter, it returns the worst performance given its sensitivity to relative data point neighbours.

## Database
- loan_approval.csv
- 46233148_Portfolio3.ipynb

## Author
- Student Name: Tuan Dat Nguyen
- Student ID: 46233148