# Project Name: Predicting Salary

## Business perspective
1.	Based on features predict if a person’s salary is over $50k or not
2.	This model can be used by anyone in the job market – both employees and employers.
3.	Many companies which need this sensitive salary information to promote their product can also use the model.

## Models used for Predicting Salary
1.	Logistic Regression Classifier
2.	Kneighbors Classifier
3.	Gaussian Naïve Bayes Classifier
4.	Support Vector Machine Classifier
5.	Random Forest Classifier
6.	Stacking Classifier


## Pipeline
![image](https://github.com/mashukul/data_analytics/blob/main/Data%20Projects/assets/salary1.jpg)

## Data Description

1.	Predict whether income exceeds $50K/yr based on census data. Also known as "Census Income" dataset
2.	Extraction was done by Barry Becker from the 1994 Census database. 
3.	Data Size: number of rows: 32561 
4.	number of columns: 15

## Dataset Sample
![image](https://github.com/mashukul/data_analytics/blob/main/Data%20Projects/assets/salary2.jpg)


## Cleaning Data
1.	This is already a set of reasonably clean records
2.	The data has only few outliers but no missing values
3.	Most of the outliers have been eliminated 


## Exploring, Visualizing and Feature engineering of Data

![image](https://github.com/mashukul/data_analytics/blob/main/Data%20Projects/assets/salary3.jpg)


## Exploring, Visualizing and Feature engineering of Data
![image](https://github.com/mashukul/data_analytics/blob/main/Data%20Projects/assets/salary4.jpg)
![image](https://github.com/mashukul/data_analytics/blob/main/Data%20Projects/assets/salary5.jpg)

#### Encoding of Education based on Target:
![image](https://github.com/mashukul/data_analytics/blob/main/Data%20Projects/assets/salary6.jpg)

![image](https://github.com/mashukul/data_analytics/blob/main/Data%20Projects/assets/salary7.jpg)
#### kbest feature selection:
![image](https://github.com/mashukul/data_analytics/blob/main/Data%20Projects/assets/salary8.jpg)


## Machine Learning model algorithms and accuracy
![image](https://github.com/mashukul/data_analytics/blob/main/Data%20Projects/assets/salary9.jpg)

#### Confusion Matrix
![image](https://github.com/mashukul/data_analytics/blob/main/Data%20Projects/assets/salary10.jpg)
#### ROC Curve
![image](https://github.com/mashukul/data_analytics/blob/main/Data%20Projects/assets/salary11.jpg)

## Summary
1.	Dataset obtained from the census income data
2.	Data cleaned from missing values and outliers
3.	Categories of the Categorical Features encoded based on target
4.	Some feature eliminated based on Pearson’s correlation and Sklearn RFE method/kbest feature selection
5.	At first modelling done with individual classifiers with parameter tuning
6.	Later Ensamble methods were used with further data cross validation
7.	Ensamble method stacking has the estimators KNN, RF, SVC and final estimator was LR classifier
8.	Random forest and Stacking came up with highest accuracy


## Future scope
1.	If a dataset  with multi class salary field is available, this same model could be used for multi class classification.
2.	Multi class classification will make the predictions more targeted
3.	If a data field having Job category is available in the dataset, the salary prediction could be made in terms of job sectors
