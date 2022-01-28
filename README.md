# SBA(Small Business Administration) Loan Approval 

## Introduction
Small business owners often seek out SBA (Small Business Association) loans because they guarantee part of the loan. This basically means that the SBA will cover some of the losses should the business default on the loan, which lowers the risk involved for the business owner(s). This increases the risk to the SBA however, which can sometimes make it difficult to get accepted for one of their loan programs. <br />
The main purpose of the project was to classify and predict if loan is going to be approved or denied based on the different feature values that we have in our data. Further, our goal was also to analyze how accurately different ML models can perform in this prediction.

## Data Source 
The data was sourced from Kaggle : <br />
https://www.kaggle.com/kevinm6720/sba-loan-approval-analysis/data <br />
There are 899,164 rows of data and 27 feature columns.

## Models 
We have tried to analyse the dataset using below models :<br />
1. kNN <br />
2. SVM <br />
3. Logistic Regression <br />
4. Random Forest <br />
5. Naive <br />
6. Neural Networks <br />

## Data Exploration and Feature Engineering 
We obtained the above plot from the data, where we can see the state-wise distribution of loan that was charged off (light blue) vs. loan that was paid in full (dark blue). It can be seen that North Carolina, Illinois and California are the top states with high defaulter rate. <br />

![image](https://user-images.githubusercontent.com/91768855/151626135-1df6b749-441f-4576-8928-74d43eb45195.png)
<br />
Correlation matrix and other tools such as boxplots were employed to understand how the numerical variables interact with each other. <br />

![image](https://user-images.githubusercontent.com/91768855/151626511-c57bb2b6-c1e1-43d8-8f67-b3054624f8a2.png)

## Model Building 
Post data cleaning and data exploration phase we started with model building. The test set had 7500 data points and below is the summary: <br />

### 1. Naive Model 
Error rate: 0.016 <br />
The average performance for 5 folds:  0.9839 

![image](https://user-images.githubusercontent.com/91768855/151631230-e3fd216f-304c-42c7-a5b0-f29950b87b2f.png)

### 2. kNN 
Best k value : 5 <br />
Error Rate : 0.121 <br />
Accuracy : 0.88 <br />

Confusion Matrix : <br />
[[5510  365] <br />
[ 542 1083]]

### 3. Random Forest 
Test accuracy: 0.99133 <br />
out-of-bag accuracy: 0.99089 <br />
The average performance for 5 folds:  0.9907 <br />

![image](https://user-images.githubusercontent.com/91768855/151631390-32371c76-d087-4e6a-942d-3868128e1fb5.png)


### 4. Logistic Regression 
Error rate : 0.0184 <br />
Accuracy : 0.982 <br />

![image](https://user-images.githubusercontent.com/91768855/151632122-c0abcb04-5a7a-4ffb-ae0d-e4a1f714d799.png)

### 5. Logistic Regression with L1 regularisation SAGA solver
Error rate : 0.0353 <br />
Accuracy : 0.96 <br />

![image](https://user-images.githubusercontent.com/91768855/151633541-7e11c17d-5933-48b1-9ba1-b200c3ffb2ec.png)

### 6. Logistic Regression with L2 regularisation SAG solver
Error rate : 0.0301 <br />
Accuracy : 0.97 <br />

![image](https://user-images.githubusercontent.com/91768855/151633700-41cc0f78-405a-49b9-b54a-7ab2f0e7dee3.png)

### 7.SVM (Radial Kernel)
Error rate: 0.0459 <br />
Accuracy : 0.95 <br />

![image](https://user-images.githubusercontent.com/91768855/151633965-e112096a-5672-485d-bd80-1b97d3e6908f.png)

### 8.SVM (Polynomial Degree=3)
Error rate: 0.0672 <br />
Accuracy : 0.93 <br />

![image](https://user-images.githubusercontent.com/91768855/151634365-3ba6edf4-24f4-4684-a61a-04ecf9706a2d.png)

### 9.Neural Net (Three Layers)
Error rate: 0.0148 <br />
Accuracy : 0.99 <br />

![image](https://user-images.githubusercontent.com/91768855/151634557-7398fcd6-06d1-4161-8672-2ccb510acecb.png)

### 10.Neural Net (Four Layers)
Error rate: 0.135 <br />
Accuracy : 0.86 <br />

![image](https://user-images.githubusercontent.com/91768855/151634669-f03f274a-52a8-4ae1-9b98-3b1173c5b203.png)

## Conclusion

Some of the best performing models were Random Forests, Logistic Regression and Neural Net (3 layers) with minimal error rate.

