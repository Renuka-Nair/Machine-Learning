# SBA(Small Business Administration) Loan Approval 

## Introduction
Small business owners often seek out SBA (Small Business Association) loans because they guarantee part of the loan. This basically means that the SBA will cover some of the losses should the business default on the loan, which lowers the risk involved for the business owner(s). This increases the risk to the SBA however, which can sometimes make it difficult to get accepted for one of their loan programs. 
The main purpose of the project was to classify and predict if loan is going to be approved or denied based on the different feature values that we have in our data. Further, our goal was also to analyze how accurately different ML models can perform in this prediction.

## Data Source 
The data was sourced from Kaggle : 
https://www.kaggle.com/kevinm6720/sba-loan-approval-analysis/data 
There are 899,164 rows of data and 27 feature columns.

## Models 
We have tried to analyse the dataset using below models :
1. kNN
2. SVM
3. Logistic Regression
4. Random Forest
5. Naive
6. Neural Networks

## Data Exploration and Feature Engineering 

![image](https://user-images.githubusercontent.com/91768855/151626135-1df6b749-441f-4576-8928-74d43eb45195.png)

We obtained the above plot from the data, where we can see the state-wise distribution of loan that was charged off vs. loan that was paid in full. It can be seen that North Carolina, Illinois and California are the top states with high defaulter rate.
