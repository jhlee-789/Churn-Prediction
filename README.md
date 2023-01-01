# Credit Churn Prediction with Machine Learning and Deep Learning

## 1) Introduction

Credit risk detection is one of the hot applications for machine learning and deep learning. 
This project used customer profile information along with credit records of customers to build machine learning models to detect risky credit card applicants. 
The project has 5 stages: data cleansing, data exploration and visualization, imbalance data problem discussion, 
machine learning model building and finally deep learning network implementation on risky cases predictions. 
This project also gave some insights on how to tune models to solve imbalanced dataset problems.

</p>
</p>

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


## 3) Exploratory Data Analysis 

* From the data set, which was handled and managed in the second part, the data cleansing part, exploratory data analysis became easier. Therefore, we could easily find the following: in the data set, there are more females than males, there are more people with realty than those who do not have realty, and there are more people without kids than with kids. 

By plotting the par charts and pie charts, findings become clearer.


### 1. Income type

![image](https://user-images.githubusercontent.com/96342048/210169659-fb045a36-7289-4185-bf90-aaa570b89abb.png)

With the income types, the bar chart shows that over half was from working and 23% was from commercial.
 
### 2. Family type 

![image](https://user-images.githubusercontent.com/96342048/210169690-5b7dee9b-7ce8-4e7e-9d4c-829746450815.png)

For family status, marriage counted the most, almost 70%, and single came second about 13%. 
 
### 3. Housing type 

![image](https://user-images.githubusercontent.com/96342048/210169695-aa0052a8-bcab-43a7-9a24-4f5d78cfdcc6.png)

For housing type, apartment/ house was the most common type. 

### 4. Education Type

![image](https://user-images.githubusercontent.com/96342048/210169699-80673c7d-bd9f-410c-aefc-08e3a3826609.png)

Most people got secondary, or secondary special education. 

### 5. Occupation type

![image](https://user-images.githubusercontent.com/96342048/210169704-5617e34f-8485-40d3-a916-dd1147b70978.png)

The occupation type was diverse, with laborers counted the most. 
To figure out a relationship between the variables, we drew some violin plots between the variables. 

### 6. Violin plot between the car owners and total amount of income

![image](https://user-images.githubusercontent.com/96342048/210169711-bd5e576b-2dab-4aa9-9afe-2cabcd6f5fbe.png)

From the violin plot between the car owners and the total amount of income, we could find out that the car owners have higher income, and even the highest income came from the car owners. This implies that car owners tend to have higher income than those who do not own a car. 

### 7. Violin plot between the car owners and total amount of income + realty

![image](https://user-images.githubusercontent.com/96342048/210169719-76090472-3f67-4bfb-ae8c-30a5f1c70b34.png)

And when the reality was included in the analysis, we could conclude that higher-income people tend to have cars.
