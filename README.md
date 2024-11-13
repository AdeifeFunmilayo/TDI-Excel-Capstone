# TDI-Excel-Capstone
 Data Analysis Repository for TDI to analyze loan performance, borrower demographics, and risk factors. Includes data cleaning, analysis with pivot tables, and visualizations in Excel, enabling data-driven decisions for loan approvals, risk management, and profitability optimization.
________
## Title:  Loan Data Analysis for TDI
________
## Outlines
[Abstract Summary](#abstract-summary)

[Introduction](#introduction)

[Data Description](#data-description)

[Methodology](#methodology)

[Analysis](#analysis)

[Discussion](#discussion)

[Conclusion](#conclusion)

## Abstract Summary: 
This project provides an in-depth loan data analysis for The Data Immersed (TDI), a financial services company. By examining loan performance, borrower demographics, and risk factors, it offers insights to optimize loan approval criteria, manage risk, and enhance profitability. Key elements include data cleaning, pivot tables, and visualizations that enable TDI's management to make informed, data-driven decisions. The analysis focuses on understanding default rates, customer risk profiles, and the impact of interest rates on loan outcomes, ultimately improving loan portfolio performance and customer satisfaction.
________
# Introduction
________
## Background: 
The financial services sector faces increasing demands to understand and manage risks associated with loan issuance and repayment. With the growing complexity of loan portfolios, lenders need data-driven insights to guide decision-making in areas like risk assessment, loan approval, and customer satisfaction. As part of The Data Immersed (TDI) team, the objective is to conduct a comprehensive analysis of TDI's loan data to identify key trends, risks, and areas for improvement. By examining factors like borrower demographics, loan terms, and repayment performance, this project will help TDI refine its loan issuance criteria, manage interest rates effectively, and improve overall profitability while mitigating default risk.
________
## Problem Statement
The goal of the Loan Data Analysis is to reduce TDI’s loan default rates and optimize loan performance by analyzing borrower risk profiles, interest rates, and customer demographics. We aim to provide actionable insights that will allow TDI to improve loan approval criteria, optimize interest rates based on risk, and identify key factors that influence loan default, thus enhancing overall profitability and customer satisfaction.
________
## Objectives
- Define Key Challenges: Identify and outline TDI's primary challenges, such as high default rates, borrower risk profiling, and optimizing interest rates for different customer segments.
- Clean and Prepare Data: Perform data cleaning in Excel, including handling missing values, removing duplicates, and standardizing formats. Create calculated columns (e.g., debt-to-income ratio) for enhanced analysis.
- Analyze Loan Performance and Customer Segmentation: Use Excel formulas, pivot tables, and charts to explore key metrics, such as loan default rates by demographics, interest rate impacts, loan amounts, and approval rates across segments.
- Provide Interactive Insights: Develop an Excel-based interactive experience with slicers, filters, and conditional formatting to allow users to explore data by factors like loan purpose and credit score.
- Identify High-Risk Loans: Analyze relationships between credit score, loan amount, and interest rate to identify high-risk loans. Provide insights for risk mitigation, such as setting minimum credit score thresholds.
- Optimize Loan Approval: Detect patterns in loan approval and rejection rates by borrower demographics and loan conditions. Suggest improvements to enhance profitability while minimizing risk.
- Generate Recommendations: Summarize actionable recommendations in a report, advising TDI on improving loan approval criteria, reducing defaults, and optimizing profitability.
________
# Data Description
________
## Data Source:
he loan dataset used in this analysis was provided by The Data Immersed (TDI) and includes anonymized information on borrower demographics, loan details, interest rates, payment history, and loan status. This dataset serves as the foundation for analyzing loan performance, identifying risk factors, and exploring customer profiles to support TDI's decision-making.
________
## Data Characteristics
- id- Unique identifier for each loan record.
- address_state- Abbreviation of the state where the borrower resides.
- application_type-	Type of loan application, e.g., INDIVIDUAL.
- emp_length-	Length of employment of the borrower, in years.
- emp_title-	Job title of the borrower.
- grade-	Grade assigned to the loan, indicating the risk level (e.g., A, B, C).
- home_ownership-	Home ownership status of the borrower (R-RENT,MO- MORTGAGE, O-OWN).
- issue_date-	Date the loan was issued.
- last_credit_pull_date-	Date of the last credit pull on the borrower.
- last_payment_date-	Date of the last payment made by the borrower.
- loan_status-	Current status of the loan (Charged Off, Fully Paid, etc.).
- next_payment_date-	Date when the next payment is due.
- member_id-	Unique identifier for the borrower.
- purpose-	Purpose of the loan (e.g., car).
- sub_grade-	Subgrade of the loan, providing more granularity to the grade.
- term-	Term of the loan (e.g., 36 months, 60 months).
- verification_status-	Status of verification of borrower information (V-Verified,NOT V- Not Verified,SV- Source Verified).
- annual_income-	Annual income of the borrower in USD.
- dti-	Debt-to-income ratio of the borrower.
- installment-	Monthly installment amount for the loan.
- int_rate-	Interest rate of the loan.
- loan_amount-	Total amount of the loan in USD.
- total_acc-	Total number of credit lines the borrower has.
- btotal_payment-	Total amount paid by the borrower by the end of the loan period in USD.
________
# Methodology
________
## Data Cleaning:
![Screenshot (102)](https://github.com/user-attachments/assets/2fe85595-4460-414b-b115-64e303326e9a)
1. **Remove Duplicates**
- Action: Highlighted all data (Ctrl + A) and used the Data tab > Remove Duplicates option. This removed 15 duplicate entries, leaving 38,574 unique records.
- Reason: Removing duplicates ensures data accuracy by eliminating repeated entries that could skew loan performance metrics and lead to unreliable analysis.
2. **Handle Missing Values**
- Action: Replaced empty cells in the emp_title column with "Unknown" to standardize entries.
- Reason: Filling missing values maintains data completeness, which helps avoid gaps in analysis and ensures that visualizations and calculations reflect all records accurately.
3. **Data Type Formatting**
- Action: Adjusted data types to ensure each column reflects the correct data type (e.g., numbers for income, dates for application and payment records).
- Reason: Correct data types prevent calculation errors and make analysis easier. For instance, formatted dates enable chronological sorting, and numeric formats support aggregations.
4. **Text Formatting**
- Action: Applied the PROPER function to application_type and purpose columns to convert text from uppercase to proper case.
- Reason: Consistent text formatting enhances readability and prevents issues with case sensitivity when filtering or analyzing text data.
5. **Column Naming**
- Action: Renamed the column home_Oership to Home_Ownership to correct the spelling and make it more intuitive.
- Reason: Clear, accurate column names improve data readability, reducing the risk of errors during analysis and making the dataset more accessible for other users.
6. **Date Format Standardization**
- Action: Standardized date formats by using Find and Replace to replace hyphens (-) with slashes (/) in the issue_date, last_credit_pull_date, last_payment_date, and next_payment_date columns.
- Reason: Consistent date formatting allows for accurate date-based sorting, filtering, and analysis. It also prevents formatting issues when creating time-based visualizations.
7. **Emp_Length Conversion**
- Action: Created an additional column, Emp_Length_Numeric, using the formula
```Excel
=IFS([@[emp_length]]="< 1 year",0, [@[emp_length]]="1 year",1, [@[emp_length]]="2 years",2, [@[emp_length]]="3 years",3, [@[emp_length]]="4 years",4, [@[emp_length]]="5 years",5, [@[emp_length]]="6 years",6, [@[emp_length]]="7 years",7, [@[emp_length]]="8 years",8, [@[emp_length]]="9 years",9, [@[emp_length]]="10+ years",10)
```
   to convert the textual emp_length values into numeric format.

Reason: Converting emp_length into a numeric format allows for easier data analysis, as numeric values are more suitable for statistical calculations and comparisons. This ensures that employment length is standardized and ready for analysis or modeling.
  ![Screenshot (101)](https://github.com/user-attachments/assets/9cc64065-d0be-4793-919a-d71aa4faf418)
___________
## Exploratory Data Analysis (EDA):
- Total Sales
- Total Profit.
- Average Sales per Order
- Profit Margin.
  ________
# Analysis
  ________
## Analysis Questions
________
#### What is the distribution of loan statuses (Fully Paid, Charged Off, Current) across different grades?
  ## Approach
  To analyze the breakdown of loan status by loan grade, we used a pivot table to organize and summarize the data.
- Columns: Loan status (Fully Paid, Charged Off, Current).
- Rows: Loan grade (A, B, C, D, E, F, G).
- Values: Loan ID (using the Count function to count the number of records in each category).
  ## Findings
- Grade A loans represent the lowest risk, with a high percentage of fully paid loans (93.9%) and a very low percentage of loans that are charged off (5.7%).
- Grades B and C maintain a relatively lower default risk but show an increasing number of charged-off loans as the grade decreases.
- Grades D, E, F, and G show higher proportions of charged-off loans, with Grade G exhibiting the highest risk of defaults (31.3% charged off), followed closely by Grade F (30.3% charged off).
- As the loan grade decreases from A to G, the risk of default (charged-off loans) increases significantly, suggesting that more stringent loan approval criteria may be needed for lower-grade loans.
   ## Results
  ![Screenshot (103)](https://github.com/user-attachments/assets/cec6681f-c1d6-4b44-87d9-93bcc470e5c2)
![Picture1](https://github.com/user-attachments/assets/02b610d6-c869-4945-aa81-3802b374fd12)
   ________
#### Customer Segment and Region Performance: Assess sales and profitability across customer segments and regions to identify high-value markets for strategic marketing focus.
  ## Approach
  ## Findings
   ## Results
   ________
#### Sales Trend Analysis: Analyse seasonal sales trends to time marketing efforts effectively, maximizing impact during peak sales periods.
  ## Approach
  ## Findings
   ## Results
   ________
#### Impact of Discounts on Profitability: Explore how discount rates affect overall sales and profit. This will inform pricing and promotional strategies.
  ## Approach
  ## Findings
   ## Results
   ________
## Findings Summary
________
## Visualization
________
# Discussion
________
## Interpretation of Results
________
## Implications
________
## Actionable Insights
________
# Conclusion
________
## Summary
________
## Recommendation

