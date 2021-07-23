# Data-Scientist-Salary-Prediction: Project Overview
This project predicts the salary of data scientist salaries based on various factors.
* Created a model that estimates data science salaries(RMSE~$11k) that can help data scientists predict their salaries for incoming jobs. 
* Feature engineered the data to quantify the value that companies and different types of positions put on certain coding languages(python,SQL,etc)
* Used Linear Regression, Lasso, Regression, and Random Forest Regressors and optimized them using GridSearchCV

## Code and Resources Used
**Python Version:** 3.8
**Packages:** numpy,pandas,matplotlib,seaborn,sklearn
**Data Taken From:** https://github.com/therrshan/Salary-Predictions

## Data Cleaning
The first step was to clean the data to make it usable for the model. Here are the steps I took and the new variables I created.
* Parsed salary to get numeric value
* Made a column for company state
* Added a column for if the job location was in the same state as the headquarters
* Added a column for Job Description Length
* Parsed out Age of company based on the Founded Year
* Parsed Job Description to create a column for the seniority of the job
* Column for simplified job title
* Made columns for if different coding skills were listed in the job description
  *Python
  *SQL
  *Spark
  *AWS
  *R

## EDA
I looked at the distribution and correlations between the continuous variables and also made pivot tables to measure the relatioships between different variables and salary. Here below are some highlights from this data analysis. 
![alt text](https://github.com/akirainoue72/Data-Scientist-Salary-Prediction/blob/master/correlation_heatmap.png)
![alt text](https://github.com/akirainoue72/Data-Scientist-Salary-Prediction/blob/master/Salaries.PNG)
![alt text](https://github.com/akirainoue72/Data-Scientist-Salary-Prediction/blob/master/distribution_salary.png)

## Model Building

First, I transformed all the catagorical variables into dummy variables and then I split the data into train and test splits with a test size of 25%. 

I then tried three different models Linear Regression, Lasso Regression, and Random Forest Regressor and initially evaluated them based on the Mean Absolute Error as it is the easiest to analyze and outliers are not that bad for the models I used. 

After doing all three models, the Random Forest model gave the best results so I decided to optimize with GridSearchCV.

# Model Results

Using GridSearchCV, I used root mean squared error to evaaluate the result on the test data as it was the best parameter based on the GridSearchCV outcomes. 
Here is the final result
**Random Forest** : RMSE=12.07






