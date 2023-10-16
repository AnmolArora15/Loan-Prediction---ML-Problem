# Loan Prediction Machine Learning Problem
![IMG](https://github.com/AnmolArora15/Loan-Prediction---ML-Problem/blob/main/Images/loan.jpeg "IMG")

- Dream Housing Finance is a company that deals with all kinds of home loan.
- They want to automate the process the loan eligibility.
- In this project we have developed various models including Logistic Regression, Tree Based Model and XG Boost. 
- Best Accuracy on Real Test DataSet was achived with Logistic Regression.

# Table of Contents

- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Importing & Installing Libraries](#importing--installing-libraries)
- [Data Acquisition & Description](#data-acquisition--description)
- [Data Pre-Processing](#data-pre-processing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Preparation](#data-preparation)
- [Modelling](#modelling)
- [Summary](#summary)
- [Contact Information](#contact-information)

## Introduction
- Our Client for this Project is Dream Housing Finance. The company deals in all kinds of home loans.
- They have a presence across all urban, semi-urban and rural areas.
- Customer first applies for home loan and after that company validates the customer eligibility for loan.
- Company wants to automate the loan eligibility process (real time) based on customer detail provided while filling online application form.
- To automate this process, they have provided a dataset to identify the customers segments that are eligible for loan amount so that they can specifically target these customers.

## Problem Statement
![IMG](https://github.com/AnmolArora15/Loan-Prediction---ML-Problem/blob/main/Images/loan2.jpeg)
- The Current process is a manual process and time consuming.
- Company has hired us as a Data Scientist to resolve their problem.

![IMG](https://github.com/AnmolArora15/Loan-Prediction---ML-Problem/blob/main/Images/OIP.jpeg)

## Importing & Installing Libraries
We have used several libraries in our project, including:
- pandas
- numpy
- matplotlib
- seaborn
- sklearn
  
## Data Acquisition & Description
**Train Set:**

- The train dataset contains 614 rows and 12 columns.
- **Loan_Status** is our target variable.
- The training dataset can be downloaded from [here](https://raw.githubusercontent.com/AnmolArora15/Loan-Prediction---ML-Problem/main/Dataset/train1.csv).

**Test Set:**

- The test dataset contains 367 rows and 11 columns.
- The test set doesnt contain the `Loan_Status` column.
- It needs to be predicted for the test set.
- The test dataset can be downloaded from [here](https://raw.githubusercontent.com/AnmolArora15/Loan-Prediction---ML-Problem/main/Dataset/test_lAUu6dG%20(2).csv).

Our Dataset has the following features along with there dtypes 
| Column Name  | Description  |
| ------------ | ------------ |
| Loan_ID  | object   |
| Gender  | object  |
| Married  | object  |
| Dependents  | object  |
| Education  | object  |
| Self Employed  | object  |
| Applicant Income  | int64  |
| Coapplicant Income  | float64  |
| LoanAmount | float64   |
| Loan Amount Term| float64 |
| Credit History | float64 |
| Property Area | object |
| Loan Status | object |

## Data Pre-Processing
- We have imputed our missing values.
- Data types of Dependents and Credit History are changed.
- We have replaced '3+' with '3' in 'dependent' feature.

## Exploratory Data Analysis

![IMG](https://github.com/AnmolArora15/Loan-Prediction---ML-Problem/blob/main/Images/loan_status.png)
![IMG](https://github.com/AnmolArora15/Loan-Prediction---ML-Problem/blob/main/Images/gender.png)
![IMG](https://github.com/AnmolArora15/Loan-Prediction---ML-Problem/blob/main/Images/credit_history.png)
![IMG](https://github.com/AnmolArora15/Loan-Prediction---ML-Problem/blob/main/Images/marital_status.png)
![IMG](https://github.com/AnmolArora15/Loan-Prediction---ML-Problem/blob/main/Images/self_employed.png)
![IMG](https://github.com/AnmolArora15/Loan-Prediction---ML-Problem/blob/main/Images/heatmap.png)
![IMG](https://github.com/AnmolArora15/Loan-Prediction---ML-Problem/blob/main/Images/applicant_income%26status.png)
![IMG](https://github.com/AnmolArora15/Loan-Prediction---ML-Problem/blob/main/Images/loan_amount%26status.png)


**Observations**
- Distribution of Gender is fairly unequal. Lots of Male as compared to females.
- People with marital status 'Married' are more compared to 'Unmarried'.
- More Graduate people than not Graduate.
- Most of the people are not self employed.
- Outliers present in Applicant Income,Coapplicant Income,Loan Amount and Loan Amount Term.
- Very few people with Credit History 0
- In terms of Property Area Semiurban > Urban > Rural.
- People having Loan are almost double of people not having Loan. 
- Using the chi2 contigency test we saw -
	- Gender and Loan Status are Independent with p = 0.66
	- Education and Loan_status are dependent with p =0.03
	- Credit_History has 100% dependency with Loan_status with p =0.00
	- Self_employed and Loan_status are Independent with p =0.93
	- Property Area and Loan Staus are higly dependent on each other with p =0.0

## Data Preparation
- We have created a new column of Total Income = ApplicantIncome + CoapplicantIncome.
- We have converted our Categorical features into Numerical using Label Encoder.
- To bring Continous features on the same scale we have used Standard Scaler.

## Modelling
- We have splitted our Data into Dependent and Independent features.(x and y)
- We have used sklearn train_test_split to split our Data into x_train,x_test,y_train,y_test.

We have deployed the following models - 
| Model Name | Train Accuracy | Test Accuracy|
| ---------------| ---------------- | ---------------|
| Logistic Reg.  | 0.81      | 0.81|
| Decision Tree | 0.83      | 0.77|
| Random Forest | 1.0 | 0.77 |
| Ada Boost | 0.83 | 0.80|
| XG Boost| 0.80|  0.79|

- We tried performing hyperparamter tuning on Ada Boost and XG Boost and saw an increase in Accuracy.
- We made an app using **Gradio** to show whether a person is eligible for Loan or not.

## Summary
- After removing all the missing values and correcting inconsistencies we applied our model on Real Test Dataset.
- **Logistic Regression** was performing best with 77.77% accuracy on Analytics Vidya Hackathon.
- We have secured top 5% position on Analytics Vidya Hackathon with the above approch.
- We can further tune our other models for better accuracy.
- We can also try removing few features which are less important in **predicting Loan Status** and see if our model performance increases.
- We can try and work on the outliers in our continous features using domain knowledge or with client's inputs.  

  Thanks.

## Contact Information
Open for questions and suggestions.

**You can contact me on Email - anmol.1591@outlook.com
LinkedIn - www.linkedin.com/in/anmol-arora-71371318**

### Thank You







