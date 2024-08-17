# BankCustomersChurn-Data-Analysis-and-Visualization-PowerBI-Project
Customer Churn Analysis for the Royal Bank of Canada using Power BI.


## Table of Contents
- [Project Description](#project-description)
- [Project Goal](#project-goal)
- [Data Dictionary](#data-dictionary)
- [Project Requirement](#project-requirement)
- [Data Limitations](#data-limitations)
- [Data Structure and Source](#data-structure-and-source)
- [Introduction](#introduction)
- [Data Cleaning and Transformation](#data-cleaning-and-transformation)
- [Data Modelling](#data-modelling)
- [Data Analysis](#data-analysis)
- [Dashboard Overview](#dashboard-overview)
- [Key Insights](#key-insights)
- [Recommendations](#recommendations)
- [Conclusion](#conclusion)


## Project Description
By analyzing key factors that impact churn rates, including customer demographics and service usage patterns. Customer churn is a critical issue for banks as it can lead to revenue loss and damage to the bank's reputation. RBC bank management team is keen to understand the factors that contribute to customer churn and identify opportunities to improve customer retention. This analysis uncovers actionable strategies to mitigate churn and boost customer loyalty. These insights are designed to help the bank enhance its overall performance and customer satisfaction.

## Project Goal
This project aims to tackle the issue of customer attrition at the bank by utilizing Power BI for churn analysis. The bank is facing a significant rate of customer churn, which is adversely affecting its revenue and overall growth. This analysis aims to identify key trends and patterns in customer behavior that contribute to churn, helping to develop strategies to mitigate these losses.


## Data Dictionary
- RowNumber — corresponds to the record (row) number and has no effect on the output.
- CustomerId — contains random values and has no effect on customer leaving the bank.
- Surname — the surname of a customer has no impact on their decision to leave the bank.
- CreditScore — can have an effect on customer churn, since a customer with a higher credit score is less likely to leave the bank.

- Geography — a customer’s location can affect their decision to leave the bank.
- Gender — it’s interesting to explore whether gender plays a role in a customer leaving the bank.
- Age — this is certainly relevant, since older customers are less likely to leave their bank than younger ones.
- Tenure — refers to the number of years that the customer has been a client of the bank. Normally, older clients are more loyal and less likely to leave a bank.
- Balance — also a very good indicator of customer churn, as people with a higher balance in their accounts are less likely to leave the bank compared to those with lower balances.
- NumOfProducts — refers to the number of products that a customer has purchased through the bank.
- HasCrCard — denotes whether or not a customer has a credit card. This column is also relevant, since people with a credit card are less likely to leave the bank.
(•	1 represents credit card holder
•	0 represents non credit card holder)
- IsActiveMember — active customers are less likely to leave the bank.
(•	1 represents Active Member
•	0 represents Inactive Member)
- Estimated Salary — as with balance, people with lower salaries are more likely to leave the bank compared to those with higher salaries.
- Exited — whether or not the customer left the bank.
(•	1 represents Retain
•	0 represents Exit)
- Bank DOJ — date when the Customer associated/joined with the bank.

### Data Gathering:
The following data assets are used to pull the data related to Bank customer and associated details.
- ActiveCustomer
- Bank_Churn
- CreditCard
- CustomerInfo
- ExitCustomer
- Gender
- Geography



## Data Limitations
The data provided by the business user is only that of salary-earning customers.



## Data Structure and Source
The dataset used for this analysis is in CSV format and contains 10,000 rows and 12 columns. It contains accident details with fields like RowNumber, CustomerId, CreditScore, GeographyID, GenderID, Age, Tenure, Balance, NumOfProducts, HasCrCard, and others. There are 7 excel files in total with the below names.

- ActiveCustomer
- Bank_Churn
- CreditCard
- CustomerInfo
- ExitCustomer
- Gender
- Geography

The datasets are attached in this repository (zip file).



## Introduction

Before diving in, let’s familiarize ourselves with a few key terminologies relevant to this project:

- Churn: The number or percentage of customers who discontinue their business relationship or subscription with a company.
- Customer Churn: The rate at which customers stop doing business with a company.
- Churn Analysis: The process of examining and understanding the rate at which customers discontinue their relationship with a company over a specific period of time.



## Data Cleaning and Transformation

I opened the data in excel and inspected the columns for relevance to the business task (This can equally be done directly on Power Query), I was able to confirm that there is sufficient data to aid my analysis. However, data needed to be cleaned and properly transformed in the format that would be useful for the analysis.


**Preview of a section of the data sheet -**

![Screenshot 2024-08-01 173954](https://github.com/user-attachments/assets/74b3d482-48a7-4711-9b74-e10c8e2ea7d2)



## Data Modelling

Here, I explored the relationship between these tables and how they are connected. I also arranged them so that it will be easier to connect with the primary keys. This is to make visualisation easy. Power BI pre-detected most of the cardinality of the model relationship as many-to-one which is correct.


![Screenshot 2024-08-01 175735](https://github.com/user-attachments/assets/ae658edc-c09b-44fc-bf1b-6748cd18aa62)



## Data Analysis



## Dashboard Overview




## Key Insights




## Recommendations




## Conclusion

This project will enable the RBC bank management team to make data-driven decisions to improve customer retention and drive business growth. The insights gained from the analysis can inform business decisions and help to reduce customer churn rate, improve customer satisfaction, and drive revenue growth.
