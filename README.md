# BankCustomersChurn-Data-Analysis-and-Visualization-PowerBI-Project
Customer Churn Analysis for the Royal Bank of Canada using Power BI.


## Table of Contents
- [Project Description](#project-description)
- [Project Objective](#project-objective)
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


## Project Objective
In this project, I analyzed data from multiple sources, including ActiveCustomer, Bank_Churn, CreditCard, CustomerInfo, ExitCustomer, Gender, and Geography, to uncover key insights into customer churn. The analysis explored critical factors such as credit score, age, tenure, balance, number of products, credit card usage, active membership, estimated salary, and customer demographics.

The primary business objective was to identify the underlying causes of customer churn and devise effective loyalty programs and retention campaigns. Through this analysis, I provided actionable insights aimed at enhancing customer experience and satisfaction. The findings were presented in a comprehensive report with clear visualizations and strategic recommendations for the bank to improve its customer retention efforts.



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

Following are the DAX measures used for the customer churn analysis

- Active Customers = CALCULATE(COUNT(Bank_Churn[CustomerId]),ActiveCustomer[ActiveCategory]="Active Member")

- Churn % = 
  VAR EC = [Exit Customers]
  VAR TC = [Total Customers]
  VAR ChurnPer = DIVIDE(EC,TC)
  RETURN
  ChurnPer

- Credit Card Holders = CALCULATE(COUNT(Bank_Churn[CustomerId]),CreditCard[Category]="credit card holder")

- Exit Customers = CALCULATE([Total Customers],ExitCustomer[ExitCategory]="Exit")

- Inactive Customers = CALCULATE(COUNT(Bank_Churn[CustomerId]),ActiveCustomer[ActiveCategory]="Inactive Member")

- Non Credit Card Holders = CALCULATE(COUNT(Bank_Churn[CustomerId]),CreditCard[Category]="non credit card holder")

- Previous Month Exit Customers = CALCULATE([Exit Customers],PREVIOUSMONTH(DateMaster[Date]))

- Retain Customers = CALCULATE([Total Customers],ExitCustomer[ExitCategory]="Retain")

- Total Customers = COUNT(Bank_Churn[CustomerId])


I had also created a seperate Date table as shown below for calculating all the DAX measures

![Screenshot 2024-08-17 143256](https://github.com/user-attachments/assets/94ad09bc-3deb-4050-bebe-d903492f0127)



## Dashboard Overview




## Key Insights




## Recommendations
**Enhance Customer Experience:** The analysis indicates a strong correlation between customer satisfaction and churn. To address this, the bank should prioritize improving the overall customer experience through personalized services, swift issue resolution, and effective communication channels.

**Strengthen Loyalty Programs:** Developing and enhancing loyalty programs can provide significant incentives for customers to remain with the bank. These programs could include cashback rewards, service discounts, and exclusive offers tailored to customer preferences.

**Retain High-Balance Customers:** The analysis highlights that customers with higher balances are less prone to churn. The bank should focus on retaining these valuable customers by offering personalized services, premium perks such as higher interest rates, and priority support.

**Boost Active Membership:** With active members showing a lower likelihood of churning, the bank should work on increasing active membership. This can be achieved by promoting the benefits of being an active member and offering incentives that encourage greater engagement with the bank.

**Encourage Credit Card Usage:** Customers who actively use credit cards are less likely to churn. The bank should promote credit card usage by providing rewards and benefits for transactions made using credit cards, thereby increasing customer retention.

**Proactively Address Customer Concerns:** Customer concerns and unresolved issues are major contributors to churn. The bank should proactively address these concerns by ensuring prompt and satisfactory resolutions, which will help build trust and reduce attrition.

**Engage Younger Customers:** The analysis reveals that younger customers have a higher propensity to churn. The bank should target this demographic by offering customized products and services that align with their needs and preferences, thus fostering long-term loyalty.



## Conclusion

This project will enable the RBC bank management team to make data-driven decisions to improve customer retention and drive business growth. The insights gained from the analysis can inform business decisions and help to reduce customer churn rate, improve customer satisfaction, and drive revenue growth.
