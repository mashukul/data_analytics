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
![image](https://github.com/mashukul/data_analytics/assets/71208684/18a6f194-2082-4d49-899c-66d6880eebca)



## Data Description

1.	Predict whether income exceeds $50K/yr based on census data. Also known as "Census Income" dataset
2.	Extraction was done by Barry Becker from the 1994 Census database. 
3.	Data Size: number of rows: 32561 
4.	number of columns: 15

## Dataset Sample
![image](https://github.com/mashukul/data_analytics/assets/71208684/b7c5fc8e-f38f-4986-9c11-1b8f5dc3d927)


## Cleaning Data
1.	This is already a set of reasonably clean records
2.	The data has only few outliers but no missing values
3.	Most of the outliers have been eliminated 

![image](https://github.com/mashukul/data_analytics/assets/71208684/7934c967-fcf0-4410-a127-53a4eee27ef6)


## Exploring, Visualizing and Feature engineering of Data

![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig4.jpg)


## Exploring, Visualizing and Feature engineering of Data
![image](https://github.com/mashukul/data_analytics/assets/71208684/2d4d0c25-b0fd-4fe8-90c8-fcfa894d2681)

![image](https://github.com/mashukul/data_analytics/assets/71208684/4568c7aa-c4bb-405f-825b-53722835e1c3)

#### Encoding of Education based on Target:
![image](https://github.com/mashukul/data_analytics/assets/71208684/100f9d07-4ca3-410c-bf3d-2e40db0eaf7e)

![image](https://github.com/mashukul/data_analytics/assets/71208684/0553fc82-4337-4b34-8eca-99f5aaa78114)
#### kbest feature selection:
![image](https://github.com/mashukul/data_analytics/assets/71208684/e81781a8-9115-40e4-b010-37b8bcf7e430)


## Machine Learning model algorithms and accuracy
![image](https://github.com/mashukul/data_analytics/assets/71208684/c354e7d0-c05f-431d-abfa-d28a86002615)

#### Confusion Matrix
![image](https://github.com/mashukul/data_analytics/assets/71208684/62a47b1d-31b8-4e1f-b9cf-b15e48169d23)

#### ROC Curve
![image](https://github.com/mashukul/data_analytics/assets/71208684/67dc28ba-200e-4fe0-9739-dbf1cca9bc00)

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
