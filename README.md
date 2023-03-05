# ST704 Project

## Summary
As the dimension of the data grows with the evolution of science, being adept in computer programs becomes necessary for statisticians to deal with large-scale data. In this regard, we will analyze what computer programs are more attractive in the job market, and figure out which program is preferred for each specific field.

## Outline
We took a dataset related to a data scientist job from [Kaggle](https://www.kaggle.com/datasets/nikhilbhathi/data-scientist-salary-us-glassdoor). The data was made by scrapping the job postings related to the position of "Data Scientist" from Glassdoors. It contains metadata about the position (including job title, rating of the company, the location, the number of employees, etc) and dummy variables for required computer programming skills (including Python, Spark, AWS, Pytorch, and 12 more). The number of observations is 742.
We will set the average salary as the response variable, and the remaining as the predictor variables.

## Methods
In this project, we will consider which variables are significant in predicting the salary of data scientists. Since the data scientist is more likely to be proficient in one or more computer programs, we will apply **Ridge** and **Lasso** to investigate which computer skill is significantly effective in the job market. Furthermore, getting paid above the minimum livable wage is important in the job search. In this regard, we will focus on the lower quartile (the value under which 25\%) by applying **quantile regression** with a 0.25 quantile.
Moreover, the correlation between computer programming variables will happen again in the quantile regression setting. Thus, we will apply the lasso penalty to quantile regression, and compare how the lasso penalty changes the coefficient values in quantile regression.
In addition, we will apply the **least angle regression**, **Kernel regression method** to fit the regression model and **XGBoost** to predict the salary.
