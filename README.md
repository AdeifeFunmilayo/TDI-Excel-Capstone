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
- Initial Dataset: The dataset initially contained 9,995 rows and 21 columns.
- Duplicate Check: 
- Missing Values: 
- Column Removal: Certain columns were removed to focus on essential data:
  1. A Shipping Time column was calculated by subtracting the Order Date from the Ship Date to gauge delivery timelines, potentially useful for further analysis.
- Final Dataset: After cleaning, the dataset retained 9,995 rows and 17 columns, containing only the most relevant fields for a focused analysis of sales revenue.
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
  ## Business Questions
  ________
## Analysis Questions
________
#### Top Revenue and Profit Products: Identify products and categories that drive the most revenue and profit. These insights will guide targeted marketing.
  ## Approach
  ## Findings
   ## Results
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

