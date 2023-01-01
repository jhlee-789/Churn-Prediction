# Credit card applicant detection using machine learning and deep learning 


## 1) Introduction

Credit risk detection is one of the hot applications for machine learning and deep learning. 
This project used customer profile information along with credit records of customers to build machine learning models to detect risky credit card applicants. 
The project has 5 stages: data cleansing, data exploration and visualization, imbalance data problem discussion, 
machine learning model building and finally deep learning network implementation on risky cases predictions. 
This project also gave some insights on how to tune models to solve imbalanced dataset problems.


## 2) Data cleansing

### 1. application_record.csv

* It is about personal information on customers, the card users. It includes their ID, age, salary, occupation type and other 14 of column names.


DAYS_EMPLOYED: Greater than 300,000 days of employed days do not make sense so that we acknowledged this sort of values as outliers, and these values have been dropped
Plus, values on this column did not look intuitive to understand at a glance. Thus, we converted values like -1134 into employed years like 3. DAYS_BIRTH column was also processed as well.


OCCUPATION_TYPE: There were null values on this column. Rows with this null value were 2 out of 9 on this dataset, these null values were dropped


FLAG_MOBIL: There is only one kind of value on this column, which is that people have mobile phones. It is meaningless because it cannot help anything in machine learning for classification.


### 2. credit_record.csv

* credit_record is about customers’ debt payment status, which includes their ID and debt status for each month.

STATUS: There were credibility status values like X and C. They did not look intuitive to understand at a glance. We divided them into ‘risky’ or ‘safe’, if the default is over 2 months and converted them into 1 and 0 for machine learning models.


### 3. Dataset merging

* Lastly, we merged two of the datasets into one dataset by using merge function through Id to make it fit for machine learning. We created the final dataset in this process.


