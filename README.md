# **Salary Prediction Project**

## **Introduction**

The problem addressed in this project entails how HR department can offer reasonable salary to staff and thereby be able to reduce unnecessary cost to the company while maintaining positive employee motivation. If staff happens to be underpaid, there will be high employee dissatisfaction resulting in increased employee turnover within the company. While on the other hand, overpaying can increase company’s cost which could have been used to further the growth and expansion of the company. 

The datasets used in this project are the train salaries, test salaries and train features which are based on the salaries of 1 million previous job advertisements. The model is trained using train dataset which comprises the features, namely: jobid, companyid, jobtype, major, degree, and industry. Python 3 is the tool used in this project work in conjunction with its libraries and packages namely, pandas, numpy, seaborn, sklearn and matplotlib to perform the data manipulation, visualization as well as building the predictive model.

## **Preprocessing of Data**

The data was checked and cleaned for duplicate records, missing values and for invalid data. Consequently, there were neither any features with missing data nor duplicate records. However, five records under the feature ‘salary’ were deleted owing to having an invalid salary data (salary == 0).

## **Exploratory Data Analysis / EDA**

	The features with data type category were label encoded with average salary for the category in the given feature. Namely, Company Id, Job Type, Degree, Major and Industry.

	The features with numerical variables were also separately evaluated. Namely, yearsExperience, milesFromMetropolis and salary.


## **Visualizing the Target Variable / Salary**
![](Images/Image%201.png)
 

Utilizing the IQR rule, the upper bound of the target variable i.e salary was found to be 220.5 and with a lower bound of 8.5. It is observed that senior level roles were getting salaries above the upper bound. Surprisingly, however, there were also 16 junior level roles getting high salaries above the upper bound. It is quite plausible that these junior roles were able to earn salaries above the upper bound owing to reason that all of them have very high years of experience in their roles and that all of them belong to two of the high paying industry sectors: oil and finance.

## **Relationship between Target Variable (Salaries) and Input Variables**
 ![](Images/Image%202.png)
 
                                                   Salary is positively correlated with job type
![](Images/Image%203.png)
 
                                                   High salaries tend to correspond to advanced degrees
![](Images/Image%204.png)
 
                                     Employees with majors of engineering, business and math have corresponding high salaries
![](Images/Image%205.png)
 
                                                Higher salaries correspond to the oil, finance and web industry sectors
![](Images/Image%206.png) 

                                                   Salary is directly correlated with years of experience
![](Images/Image%207.png)
 
                                                  Salaries decrease as you go further away from the metropolis


## **Visualizing the Correlation across all Columns**
![](Images/Image%208.png) 

                     It can be seen that job type, degree, years of experience and major are most closely related to salaries 

## **Engineer Features**

New features were generated by calculating summary statistics for each group in accordance with groupings of job type, degree, major, and industry. These new groupings result in new features, namely: group_mean, group_max, group_min, group_std, and group_median. CompanyId, that has low importance, is excluded from these features so as to predict salaries for new companies. The trade of this is that precision will slightly be reduced by not accounting for the CompanyId.

## **Models**

The three models selected are Linear Regression, Random Forest Regressor and Gradient Boosting Regressor.

## **Setting Metrics**

The Metrics chosen is MSE and efficacy goal is <320

## **Best Model**

Gradient Boosting Regressor is the best model with the lowest MSE value of 313.14 as compared to values of 358.16 and 313.77 which correspond to Linear Regression and Random Forest Regression, respectively.

