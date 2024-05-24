# SyriaTel Customer Churn Analysis

![depositphotos_25360821-stock-photo-communication-towers](https://github.com/pkruga/Tel_Churn_Repo/assets/91247293/c26a625f-3c66-4d68-b38e-477802bceade)

## Introduction

This project aims to leverage machine learning techniques to analyze telecommunications data and customer behavior patterns at SyriaTel, a telecommunications company. The primary objective is to accurately identify potential churners among SyriaTel's customer base, enabling the company to implement targeted strategies and interventions to retain those customers, mitigate revenue loss, and enhance overall business performance and profitability.

## Problem Statement

SyriaTel aims to mitigate revenue loss and enhance business performance by identifying customers at risk of churning. By leveraging machine learning techniques, the project focuses on predicting customer churn based on telecommunications data and behavior patterns.

## Objectives

1. **Customer Churn Prediction**: Predict whether a customer will churn or not based on their telecommunications data and behavior patterns.
2. **Model Evaluation and Selection**: Evaluate and select the best-performing machine learning model for churn prediction.
3. **Model Interpretation**: Understand how the selected model makes predictions and which features are most important in predicting churn.
4. **Model Fine-Tuning**: Optimize the selected model's hyperparameters to improve its performance.

## Data

The project utilizes a dataset containing telecommunications data and customer behavior patterns. The dataset includes features such as total day minutes, total eve minutes, total night minutes, international plan, customer service calls, and more. These features will be used to train and evaluate machine learning models for predicting customer churn.

## Methodology

1. **Data Loading and Exploratory Data Analysis (EDA)**:
  - Import necessary libraries.
  - Load the dataset from a CSV file.
  - Explore data structure, distribution, and key characteristics.
  - Perform data cleaning and preprocessing.


2. **Data Preprocessing**:
  - Handle missing values, if any.
  - Encode categorical features, if necessary.
  - Split the dataset into training and testing sets.

3. **Model Training and Evaluation**:
  - Train and evaluate multiple machine learning models (e.g., logistic regression, decision trees, random forests, gradient boosting) on the training set.
  - Evaluate model performance using appropriate metrics (e.g., accuracy, precision, recall, F1-score, area under the ROC curve).
  - Select the best-performing model based on the evaluation metrics.

4. **Model Interpretation**:
  - Analyze the feature importance scores of the selected model.
  - Understand how the model makes predictions and which features contribute the most to predicting churn.

5. **Model Fine-Tuning**:
  - Optimize the selected model's hyperparameters using techniques like grid search or random search to improve its performance.
  - Explore techniques like SMOTE (Synthetic Minority Over-sampling Technique) to handle class imbalance.

6. **Deployment and Monitoring**:
  - Develop a strategy for deploying the trained model into a production environment.
  - Implement monitoring and maintenance procedures to ensure the model's performance over time.

## Results

### Model Performance

After evaluating multiple models, the best-performing model was a Tuned Random Forest with SMOTE (Synthetic Minority Over-sampling Technique) applied to handle class imbalance. The key performance metrics of this model are as follows:

- **Accuracy Score**: 0.902 (90.2%)
- **Confusion Matrix**:
  - True Positives (Churned and correctly predicted): 92
  - True Negatives (Not churned and correctly predicted): 810
  - False Positives (Not churned but incorrectly predicted as churned): 45
  - False Negatives (Churned but incorrectly predicted as not churned): 53
- **Classification Report**:
  - Precision for Churn Class: 0.67
  - Recall for Churn Class: 0.63
  - F1-score for Churn Class: 0.65

This model demonstrated a reasonable balance between precision and recall in identifying churn cases, which is crucial for SyriaTel to mitigate revenue loss and enhance business performance.

### Feature Importance

The most influential features in predicting customer churn were:

1. Total Day Minutes
2. Total Day Charge
3. Customer Service Calls
4. International Plan
5. Total Eve Minutes

Features related to daytime usage (both minutes and charges) and customer service interactions were the most significant predictors of churn.

### Further Considerations

While the best model shows improvement compared to previous versions, further tuning and evaluation may still be necessary to optimize its performance and ensure it meets the project objectives effectively. Additional analysis, such as feature importance and model interpretation, can provide insights into how the model makes predictions and which features are most influential in identifying churn cases.

# Insights on Customer Churn

## Overview

- **Daytime Usage Matters**: Customers who spend more time and money on daytime calls are more likely to churn. Also, those who make frequent customer service calls are at higher risk of leaving.
  
- **Evening Usage Patterns**: Evening call habits also impact churn prediction. High usage or charges during evening hours might indicate potential churn behavior.
  
- **International Usage**: Customers with significant international calling activity or charges may have different churn probabilities.
  
- **Account Length**: Longer-tenured customers show different churn behaviors compared to newer subscribers.

## Model Performance

- The model correctly predicts churn or non-churn for about 90.2% of customers.
  
- Precision, recall, and F1-score provide more detailed insights into how well the model performs for churn and non-churn cases.
  
- The model predicts 912 customers as non-churners and 88 customers as churners.

- Overall, the model effectively predicts churn based on customer behavior. However, continuous refinement may be needed for better accuracy and understanding.

# Recommendations

## 1. Know Your Customers
   - Split customers into groups based on their likelihood to leave and how they behave. This helps tailor efforts to keep them.

## 2. Stay Connected
   - Reach out to customers before they think of leaving. Send them personalized messages, offers, and solve problems quickly.

## 3. Make Services Better
   - Focus on improving areas like customer service, especially if they're linked to churn.

## 4. Offer Incentives
   - Give discounts or rewards to customers who might leave to keep them around.

## 5. Listen and Learn
   - Ask customers what they think and use their feedback to make things better.

## 6. Keep Getting Better
   - Keep an eye on how well the churn prediction model works and find ways to make it even more accurate.

## 7. Suggest More
   - Offer customers other things they might like based on what they already use.

## 8. Make Things Easy
   - Make sure customers have a smooth experience whenever they interact with your company.

## 9. Stay in Touch
   - Create special offers or messages for customers who might be thinking of leaving.

## 10. Train Your Team
  - Make sure everyone who talks to customers knows how to help and make them happy.

By following these suggestions, the company can reduce the chances of losing customers, make them happier, and grow its business in the long run.

## Future Work

Potential areas for future work, feature engineering,  try decision tree classifier, more model refinement can be attemmpted.

## Dependencies

### Resources used

* Google Colab (notebook)

* Microsoft Powerpoint

## Acknowledgments

Stock images from https://depositphotos.com/photos/telecommunications.html

Dataset sourced from https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset/code







