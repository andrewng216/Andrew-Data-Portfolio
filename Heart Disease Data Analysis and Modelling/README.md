# COMP6200: Data Secience Portfolio 4
## Overview

This repository sits within the COMP6200 Data Science course at Macquarie University. The purpose of this project is to build and evaluate two predictive models in identifying whether a patient has heart disease and how accurate such predictions are to ensure those with cardiovascular diseases can be diagnosed and receive timely care and treatment. Tasks involves performing exploratory data analysis, cleaning, preprocessing and visualisng the dataset to discover relationships and patterns between heart disease and other factors, splitting data to build Logistic Regression and KNN models before comparing their performance outcomes. It will then analyse and conclude with insights for best predictive algorithm practice to address the concerning problem of accurate heart disease prediction.


## Task Sections
- Load the dataset, show and describe basic information
- Perform Exploratory Data Analysis (EDA)
    - Clean the database by checking missing/null and duplicated values
    - Visualise data based on numerical, categorical attributes and target label `HeartDisease`
    - Analyse results and performance of some features with respect to the target variable
- Clean and preprocess the dataset
    - Handling missing values
    - Remove rows in categorical columns having missing values
    - Perform a missing value imputation with the average of the column for numerical columns
- Data Processing & Model Building
    - Split dataset for traing and testing
    - Convert categorical values into numerical using `OrdinalEncoder`
    - Build a logistic regression model
        - Train model and report two classification performance metrics - accuracy and F1-score
        - Perform RFE technique to identify retained features
        - Identify the best case of Logistic Regression model    
    - Build K-NN Classifier
        - Using `grid search` and `k-fold cross validation` to train model
        - Identify best K and report testing data performance on the most optimal case of KNN
- Compare the performance of two models, draw insights and conclude with a comprehensive answer to the problem 

## Results
- **Dataset Distribution:** Patients with CDVs are only predicted at a 55.3% chance, representing around 500 cases without running any predictive model.
- **Critical Features:** Some categorical features, such as `Sex`, are identifed as key risk factors related to heart disease. Specifically, males patients have a higher chance of getting this health issue rather than females. Meanwhile, numerical features like `Age` also presents certain range of distribution, with middle-aged adults are more likely to experience cardiovascular disease.
- **Compare Models:**
    - **Logistic Regression Model:** The best case for this model has a relatively high performance on classification metrics on Accuracy and F1-Score at 85.3% and 0.87 respectively after training the model based on defined retained features.
    - **KNN Classifier:** The best KNN is at K = 7 (after conducting cross validation and grid search) where Accuracy rate and F1-score are 85.3% and 0.868 respectively.
    - Both models are not overfitting and are observed as being well-suited to accurately predict heart disease due to their high performance level. The Logistic Regression model is given a slight edge over the KNN since its nature of computational efficiency.

## Database
- heart.csv
- 46233148_Portfolio 4.ipynb

## Author
- Student Name: Tuan Dat Nguyen
- Student ID: 46233148
