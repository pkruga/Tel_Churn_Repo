# Customer Churn Prediction
This project aims to predict customer churn using various machine learning techniques. The goal is to identify key features that contribute to customer churn and develop models to accurately predict churn rates.

Table of Contents
* Overview
* Dataset
* Features
* Models Used
* Evaluation Metrics
* Results
* How to Run
* Contributing
* License

## Overview
Customer churn prediction is critical for businesses to retain customers and improve services. This project uses a dataset to analyze and predict customer churn through feature selection and model tuning.
### Introduction
The SyriaTel Customer Churn project aims to leverage machine learning techniques for analyzing telecommunications data and customer behavior patterns. Let’s delve into the details:

**Project Overview**: The project focuses on accurately identifying potential churners among SyriaTel’s customer base. By employing machine learning techniques, the goal is to predict customers who are at risk of churning. This enables SyriaTel to implement targeted strategies and interventions to retain those customers, mitigate revenue loss, and enhance overall business performance and profitability.

### Problem Statement:

SyriaTel, a telecommunications company, aims to mitigate revenue loss and enhance business performance by identifying customers at risk of churning. Leveraging machine learning techniques, the project focuses on predicting customer churn based on telecommunications data and behavior patterns.

### Objectives

**Customer Churn Prediction**: Predicting whether a customer will churn or not based on their telecommunications data and behavior patterns.

**Model Evaluation and Selection**: Evaluating and selecting the best-performing machine learning model for churn prediction.

**Model Interpretation**: Understanding how the selected model makes predictions and which features are most important in predicting churn.

**Model Fine-Tuning**: Optimizing the selected model's hyperparameters to improve its performance.

## Dataset

Sourced from Kaggle https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset/data

The dataset contains customer information of telephone records kept by SyriaTel including account length, usage details, service plans, and whether the customer churned.

In total the preliminary data had 21 columns and 3333 data values.

Data collected was as follows

 0  state : Name of State where account holder resides
 1   account length  : Period of account registration  
 2   area code : Area code of account holder               
 3   phone number : telephone number of account holder           
 4   international plan : whether holder has an international plan     
 5   voice mail plan : whether holder has a voicemail plan        
 6   number vmail messages : how many voicemail messages they've left in the period
 7   total day minutes : how many minutes have they called in the day time hours.      
 8   total day calls : how many calls they placed in the day time hours         
 9   total day charge : how much money they spent calling during day time hours     
 10  total eve minutes : how many calls they placed in the evening hours       
 11  total eve calls : how many calls they placed in the evening hours         
 12  total eve charge : how much money they spent calling during evening hours       
 13  total night minutes : how many minutes have they called in the night time hours    
 14  total night calls :  how many calls they placed in the night time hours       
 15  total night charge : how much money they spent calling during night time hours     
 16  total intl minutes : how many minutes were spent on international calls     
 17  total intl calls : how many calls were placed to international lines       
 18  total intl charge : how much mony they spent making international calls      
 19  customer service calls : how often do they contact customer service   
 20  churn : if the customer has left rescently represented by true or false.                  

Exploratory Data Analysis

**Objective**: The objective of the Exploratory Data Analysis (EDA) is to understand the structure, distribution, and key characteristics of the churn dataset to inform subsequent data preprocessing and modeling steps.

**Summary**:

1. Data Overview:

Counted missing values in each column.

3. Distribution Analysis:

   Created histograms for numerical features to visualize their distributions.

![image](https://github.com/pkruga/Tel_Churn_Repo/assets/91247293/c4a4f344-4a5d-4ab2-a056-b3beeae7b351)

   Used boxplots to identify outliers.
![image](https://github.com/pkruga/Tel_Churn_Repo/assets/91247293/bb0b41b5-8e1b-499e-a2c1-b684e8146fa5)

3. Correlation and Relationships:

   Constructed a correlation heatmap to identify relationships between numerical features.

![image](https://github.com/pkruga/Tel_Churn_Repo/assets/91247293/72166649-e19e-4cfb-90bc-ec3348f67c90)

   Generated pairplots to explore potential feature interactions.

4. Categorical Data Analysis:

    Provided value counts for categorical columns to understand category distributions.

   Plotted a count plot for the target variable (Churn) to see churn rates.

![image](https://github.com/pkruga/Tel_Churn_Repo/assets/91247293/8613e82c-9b33-4474-a8b2-c6be59167313)

## Features

Our target variable was "Churn" which against which we used selected features to make our Classification models.

The key features used in the model are:

* Total day minutes
* International plan
* Voice mail plan
* Account length
* Total day calls
* Number of voicemail messages

## Models Used

**Random Forest Classifier**: An ensemble method that uses multiple decision trees to improve prediction accuracy.

Random Forest Classifier was chosen for accuracy and high cross validation score the model was fine tuned using hyperparameters and the final model was utilize in predictions of our churn patterns

**SMOTE**: Synthetic Minority Over-sampling Technique to handle class imbalance.

## Evaluation Metrics

The models were evaluated using:

**Cross Validation Score**: overall model performance.

**Confusion Matrix**: The overall number of correct preditions of our classification model

**Accuracy**: Overall correctness of the model.

**ROC AUC**: Area under the receiver operating characteristic curve, indicating the model's ability to distinguish between classes.

**Classification Report**: Includes precision, recall, and F1-score.

## Results
The first Random Forest Classifier achieved:

Accuracy: 94.6%

ROC AUC: 0.95

The tuned Random Forest classifier achieved:

Accuracy: 93.6%

ROC AUC: 0.926

Precision, Recall, F1-score: High accuracy for predicting customers who stay, moderate for those who churn.

The refined model accuracy was assesed using the confusion matrix.

![image](https://github.com/pkruga/Tel_Churn_Repo/assets/91247293/698c9d22-c850-4e37-a739-0ab8c360f0be)

From this confusion matrix, we can derive the following information:

True Negatives: 280
False Positives: 0
False Negatives: 42
True Positives: 12
 
Important Features were also assesed to check for their influence on the overall model 

Feature Importance Values:
account length           0.063971
area code                0.014705
international plan       0.005720
voice mail plan          0.007338
number vmail messages    0.027434
                           ...   
state_VT                 0.003142
state_WA                 0.002235
state_WI                 0.002889
state_WV                 0.003088
state_WY                 0.002620

![image](https://github.com/pkruga/Tel_Churn_Repo/assets/91247293/8d9564d3-6dde-4830-9f2d-b9b47f797cc2)

**Total Day Minutes**: More minutes used during the day means customers are less likely to leave.

**International Plan**: Customers with international plans are more likely to leave.

**Voice Mail Plan**: The presence of a voicemail plan also affects churn.

**Account Length**: Long-term customers are less likely to leave.



