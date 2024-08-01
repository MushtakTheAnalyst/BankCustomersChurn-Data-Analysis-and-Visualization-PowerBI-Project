# BankCustomersChurn-Data-Analysis-and-Visualization-PowerBI-Project
Customer Churn Analysis for the Royal Bank of Canada using Power BI.


## Table of Contents
- [Project Description](#project-description)
- [Project Goal](#project-goal)
- [Data Dictionary](#data-dictionary)
- [Project Requirement](#project-requirement)
- [Stakeholders List](#stakeholders-list)
- [Data Structure and Source](#data-structure-and-source)
- [Introduction](#introduction)
- [Data Cleaning and Transformation](#data-cleaning-and-transformation)
- [Data Processing](#data-processing)
- [Data Analysis](#data-analysis)
- [Visualization and Dashboard Overview](#visualization-and-dashboard-overview)
- [Key Insights](#key-insights)
- [Recommendations](#recommendations)
- [Conclusion](#conclusion)


## Project Description
Customer Churn Analysis for the Royal Bank of Canada delivers vital insights into customer retention. By analyzing key factors that impact churn rates, including customer demographics and service usage patterns, this analysis uncovers actionable strategies to mitigate churn and boost customer loyalty. These insights are designed to help the bank enhance its overall performance and customer satisfaction.

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

Data Gathering:
The following data assets are used to pull the data related to Bank customer and associated details.
- ActiveCustomer
- Bank_Churn
- CreditCard
- CustomerInfo
- ExitCustomer
- Gender
- Geography


## Stakeholders List
- Bank Manager
- Customer Relationship Manager
- CEO


## Data Structure and Source
The dataset used for this analysis is in CSV format and contains 10,000 rows and 12 columns. It contains accident details with fields like RowNumber, CustomerId, CreditScore, GeographyID, GenderID, Age, Tenure, Balance, NumOfProducts, HasCrCard, and others. There are 7 excel files in total with the below names.

- ActiveCustomer
- Bank_Churn
- CreditCard
- CustomerInfo
- ExitCustomer
- Gender
- Geography

The datasets are attached in this repository.


## Introduction

Before diving in, let’s familiarize ourselves with a few key terminologies relevant to this project:

- Churn: The number or percentage of customers who discontinue their business relationship or subscription with a company.
- Customer Churn: The rate at which customers stop doing business with a company.
- Churn Analysis: The process of examining and understanding the rate at which customers discontinue their relationship with a company over a specific period of time.


## Data Cleaning and Transformation

I opened the data in excel and inspected the columns for relevance to the business task (This can equally be done directly on Power Query), I was able to confirm that there is sufficient data to aid my analysis. However, data needed to be cleaned and properly transformed in the format that would be useful for the analysis.

Limitations: The data provided by the business user is only that of salary-earning customers.


**Preview of a section of the data sheet -**
![Screenshot 2024-08-01 173954](https://github.com/user-attachments/assets/74b3d482-48a7-4711-9b74-e10c8e2ea7d2)



## Data Processing

Part of the requested KPIs by the client is to showcase the dashboard in monthly and yearly insight, but from our data, we only have an Accident_Date column with the full date for each data entry. Therefore, there is a need to create month and year columns to get the requested insight. The process of doing this is as follows;

1. Create two blank columns, and name them ‘Month’ and ‘Year’ respectively

2. Use the Excel Text function to extract the month and year from the Accident_Date column.
 - =TEXT(B2, “mmm”) for the newly created ‘Month’ column
 - =TEXT(B2, “yyyy”) for the newly created ‘Year’ column


![Screenshot 2024-07-13 134108](https://github.com/user-attachments/assets/c52d4855-3f72-4bbf-8048-94861f2a9978)


## Data Analysis

#### Primary Key Performance Indicators (KPIs)

- The Excel-Pivot Table was utilized to determine the total number of casualties after the accident in 2021 and 2022.
- The Accident_Severity is of 3 types- Fatal, Serious and Slight. PivotTable was utilized to determine the total number of casualties for each Accident_Severity type, and the Excel function was used to calculate the percentage of total casualties for each Accident_Severity type.
- The same PivotTable was used to determine the Vehicle_Type with maximum casualties.

#### Secondary Key Performance Indicators (KPIs)

- Categorized total casualties based on vehicle types using Excel PivotTable, and casualties for agricultural vehicles, cars, buses, vans, bikes, and others were identified. This breakdown facilitates a detailed understanding of the impact across various vehicle categories.
- Utilized Excel Pivot Table to compare monthly casualties for the current and previous years. This analysis helps identify patterns, seasonality, and potential contributing factors to accidents with time.
- Identified and analyzed the road types associated with the highest casualties. Excel Pivot Table was instrumental in summarizing and visualizing this data.
- Utilized Pivot Table to break down casualties based on road surface conditions. This analysis provides insights into the impact of road conditions on accident severity.
- Excel PivotTable was employed to analyze the correlation between casualties' location and time of day. Understanding the relationship between these variables contributes to targeted safety measures, especially in specific areas.


## Visualization and Dashboard Overview

1. Visualization:

A dedicated ‘Data Analysis’ sheet was created for comprehensive data visualization. Excel’s ‘Insert Function’ feature was utilized to pick suitable charts for each table derived from PivotTable data analysis.

- Primary KPIs: Doughnut charts were employed to visualize and represent primary KPIs. The charts were formatted for clarity, ensuring a clean and easily interpretable presentation.
- Secondary KPIs: Different visualization tools, including Doughnut chart, Treemap, Line graph, and Bar chart, were utilized to convey insights from secondary KPIs.


![Screenshot 2024-07-13 164038](https://github.com/user-attachments/assets/e9957059-0808-49cb-9999-981d9c88da7c)


  
2. Dashboard:

An interactive dashboard with key features to enhance usability and understanding was developed.

- The timeline button was integrated to visualize road accidents in 2021 and 2022 separately or collectively. This enables a more detailed examination of trends and patterns over each year.
- Slicer functionality was incorporated into the dashboard, using Rural/Urban categorization as a filter. This allows users to view the dashboard based on specific KPIs and choose between Urban, Rural, or overall perspectives for a targeted analysis.
- The dashboard is intricately linked with the ‘Data Analysis’ sheet, and providing seamless navigation to internet resources. This integration ensures easy mobility and quick access to related information. This can be interacted with with the use of icons on the left-hand side of the dashboard.


**Final Dashboard:**
![Screenshot 2024-07-13 164705](https://github.com/user-attachments/assets/9de6a973-9571-4bac-b27f-bc6a4ab24be3)



## Key Insights

**Total Casualties Analysis:** The dashboard reveals an alarming 417,883 casualties occurred due to accidents over the two-year period.

**Peak Months:** Casualties were slightly higher in 2021 compared to 2022. The highest number of casualties occurred in October and November in both years, while the lowest casualties were in January and February.

**Casualties by Vehicle Type:** Car accidents accounted for the majority of casualties, contributing to 79.8% of the total. Casualties were minimal in accidents involving other vehicle types.

**Casualties by Accident Severity:** Slight severity accidents accounted for the majority of casualties (84.1%), while fatal severity casualties were only 1.7%.

**Road Type Analysis:** The highest number of casualties occurred on single carriageway roads (309.7K), and the lowest on slip roads (4.7K).

**Casualties Distribution by Road Surface:** The majority of casualties (66.9%) occurred on dry road surfaces.

**Casualties Relation by Area/Location:** Urban areas accounted for 61% of the casualties after accidents.

**Casualties Distribution by Light Condition:** 73% of casualties occurred during daylight conditions.


## Recommendations

1. **Focus on High-Risk Periods:** By comparing casualty trends between the current and previous years on a monthly basis, the dashboard identifies critical periods in October and November. Traffic police and other stakeholders should increase safety measures and monitoring during these high-risk months.

2. **Target Car Drivers:** Since car drivers account for the bulk of casualties, they should be the focus of awareness campaigns, strict monitoring, and periodic check-ups on safe driving.

3. **Improve Single Carriageway Roads:** Extra safety measures should be implemented on single carriageway roads, and wherever possible, these roads should be upgraded to double lanes.

4. **Enhance Road Surface Conditions:** Understanding casualty distribution based on different road surface conditions helps pinpoint areas where road maintenance and surface improvements are essential.

5. **Interventions in Urban Areas:** Urban areas should be targeted for specific interventions to improve road safety, particularly during daylight hours.


## Conclusion

The Road Accident Analytics Dashboard facilitates data-driven decision-making, enabling stakeholders to implement evidence-based decisions that enhance road safety. It serves as a valuable tool for policymakers, traffic authorities, and police departments alike.
