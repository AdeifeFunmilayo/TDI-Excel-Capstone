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
|Column Name |Description|
|------------|-----------|
|id           | Unique identifier for each loan record.|
|address_state| Abbreviation of the state where the borrower resides.|
|application_type| Type of loan application, e.g., INDIVIDUAL.|
|emp_length| Length of employment of the borrower, in years.|
|emp_title|	Job title of the borrower.|
|grade|	Grade assigned to the loan, indicating the risk level (e.g., A, B, C).|
|home_ownership|	Home ownership status of the borrower (R-RENT,MO- MORTGAGE, O-OWN).|
|issue_date|	Date the loan was issued.|
|last_credit_pull_date|	Date of the last credit pull on the borrower.|
|last_payment_date|	Date of the last payment made by the borrower.|
|loan_status|	Current status of the loan (Charged Off, Fully Paid, etc.).|
|next_payment_date|	Date when the next payment is due.|
|member_id|	Unique identifier for the borrower.|
|urpose|	Purpose of the loan (e.g., car).|
|sub_grade|	Subgrade of the loan, providing more granularity to the grade.|
|term|	Term of the loan (e.g., 36 months, 60 months).|
|verification_status|	Status of verification of borrower information (V-Verified,NOT V- Not Verified,SV- Source Verified).|
|annual_income|	Annual income of the borrower in USD.|
|dti|	Debt-to-income ratio of the borrower.|
|installment|	Monthly installment amount for the loan.|
|int_rate|	Interest rate of the loan.|
|loan_amount|	Total amount of the loan in USD.|
|total_acc|	Total number of credit lines the borrower has.|
|btotal_payment|	Total amount paid by the borrower by the end of the loan period in USD.|
________
# Methodology
________
## Data Cleaning:
![Screenshot (102)](https://github.com/user-attachments/assets/2fe85595-4460-414b-b115-64e303326e9a)
**Remove Duplicates**
- Action: Highlighted all data (Ctrl + A) and used Data > Remove Duplicates. This removed 15 duplicate entries, leaving 38,574 unique records.
- Reason: Eliminating duplicates improves data accuracy by removing repeated entries that could distort loan performance metrics, leading to more reliable analysis.

**Handle Missing Values**  
- Action: Replaced empty cells in the emp_title column with "Unknown" to standardize entries.
- Reason: Filling missing values helps maintain data completeness, ensuring that visualizations and calculations include all records accurately.

**Convert Abbreviations to Standard Terms**  
- Action: Converted abbreviated entries to their full terms in specific columns:
1. Address_State: Replaced state abbreviations (e.g., "CA" to "California").
2. Home_Ownership: Expanded ownership types (e.g., "O" to "Owned").
3. Verification_Status: Standardized verification abbreviations (e.g., "V" to "Verified").
- Reason: Using full terms enhances readability and ensures consistent interpretation, especially when sharing the data with others who might not be familiar with the abbreviations.

**Text Formatting**
- Action: Applied the PROPER function to the application_type and purpose columns to convert text from uppercase to proper case.
- Reason: Consistent text formatting enhances readability and helps prevent issues with case sensitivity during filtering or analysis.

**Column Naming**
- Action: Renamed columns for clarity and corrected typos (e.g., home_Oership to Home_Ownership, emp_title to Emp-Title).
- Reason: Clear and accurate column names improve understanding and make it easier to work with data, especially in collaborative environments.

**Date Format Standardization**
- Action: Standardized date formats by using Find and Replace to replace hyphens (-) with slashes (/) in columns like issue_date, last_credit_pull_date, last_payment_date, and next_payment_date.
- Reason: Consistent date formatting ensures accurate date-based sorting, filtering, and analysis. It also reduces formatting issues in time-based visualizations.
![Screenshot (105)](https://github.com/user-attachments/assets/68efe21f-df49-434c-b81f-3436bdefb616)
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
#### Loan Default Rates by grades:
## Approach
To analyze the loan default rates, we used a pivot table to organize and summarize the data, as follows:
- Columns: Loan status categories (Fully Paid, Charged Off, Current) to show the distribution of loan outcomes.
- Rows: Loan grade categories (A, B, C, D, E, F, G) to compare default rates across different grades.
- Values: Loan ID (using the Count function to calculate the number of records in each category), enabling us to evaluate the loan performance for each grade.
- After setting up the pivot table, we calculated the default rate for each loan grade using the formula:
```Excel
=GETPIVOTDATA("ID",$A$3,"Grade","A","Loan_Status","Charged Off")/GETPIVOTDATA("ID",$A$3,"Grade","A")
```
- Converted the result to a percentage format to make the default rates easy to interpret.
**This calculation provides the percentage of loans that were charged off within each grade, helping to identify high-risk segments.**
## Findings
- Grade A: This grade has the lowest risk, with 93.9% of loans fully paid and only 5.7% charged off. This indicates that loans in Grade A are the most stable, showing minimal default risk.
- Grades B and C: These grades show a gradual increase in risk but maintain relatively lower default rates compared to the lower grades. Grade B has a 12% default rate, while Grade C has a 16% default rate, indicating they are generally safer than grades D and below but less secure than Grade A.
- Grades D, E, F, and G: These grades exhibit significantly higher default rates, with risk escalating as the grade decreases. Grade D has a 21% default rate, Grade E has 25%, Grade F has 30%, and Grade G has the highest default rate at 31%. This indicates that loans in these grades are the riskiest, with nearly a third of Grade F and G loans being charged off.
- Overall Trend: As the loan grade decreases from A to G, the default rate increases consistently, indicating a strong correlation between lower loan grades and higher risk. This trend suggests that TDI should consider implementing stricter loan approval criteria for lower-grade loans (D-G) to mitigate potential risks and default rates effectively.
   ## Results
![Screenshot (107)](https://github.com/user-attachments/assets/4a089326-9616-422e-8fee-f51bafd1b07a)
![Defaut Rate by Grade](https://github.com/user-attachments/assets/78ff2135-4876-492d-ad49-76f979f3ae0e)
________
#### Interest Rate Impact on Loan Performance.
  ## Approach
- Rows: Loan status categories (Fully Paid, Charged Off, Current) to segment loans by performance.
- Values: Average of int_rate to calculate the mean interest rate for each loan status.
  ## Findings
- Charged Off Loans: Higher interest rates for charged-off loans suggest a potential link between borrower risk profiles and defaults. Borrowers in this category may face financial strain, leading to non-repayment.
- Current Loans: Current loans have the highest average interest rate, which could reflect ongoing loans provided to higher-risk borrowers. These loans might be actively monitored to prevent transitioning to default status.
- Fully Paid Loans: Fully paid loans have the lowest average interest rate, indicating that borrowers with lower risk profiles are more likely to complete their loan payments.
  ## Results
  ![Screenshot (108)](https://github.com/user-attachments/assets/86a31c80-0f44-4ae4-86d7-13ea89bcea93)
![Average int Rate by Loan Status](https://github.com/user-attachments/assets/7e779e2c-10c0-42d1-ad00-e45490eb5d13)
________
#### Analysis of Loan Amount by Home Ownership and Purpose
  ## Approach
- Columns: Home ownership categories to compare loan amounts across different borrower home ownership statuses.
- Rows: Loan purpose to analyze how the loan amounts are distributed based on the intended use of the loan.
- Values: Sum of loan_amount to calculate the total loan amount for each combination of home ownership and purpose.
  ## Findings
**Top Borrowing Purposes:**
- Debt Consolidation dominates with a total of $232.5M, indicating that borrowers prioritize restructuring and reducing their debt burdens.
- Credit Card purposes come second with $58.9M, suggesting heavy reliance on loans to manage credit card debts.
**Home Ownership Influence:**
- Borrowers with "Rent" status account for $185.76M (42.6%) of the total, indicating a significant share of the borrowing market.
- Borrowers with a "Mortgage" status follow with $219.37M (50.3%), showing strong borrowing activity for secured homeownership.
**Least Borrowing Purposes:**
- Renewable Energy and Vacation loans have minimal totals, reflecting limited demand in these categories.
**Educational Loans:**
- Educational loans are modest at $2.16M, potentially signaling limited reliance on private loans for education financing.
   ## Results
  ![Screenshot (109)](https://github.com/user-attachments/assets/546a286d-64df-4477-97c5-00fd19b6747a)
![Loan Amount by Home Ownership and Purpose](https://github.com/user-attachments/assets/0ffd2ae5-0672-4f4d-9f08-70d9674d01ec)
________
#### Analysis of Loan Status by State
## Approach
- Rows: Address_State to represent each U.S. state.
- Columns: Loan_Status to display categories (Charged Off, Current, Fully Paid).
- Values: Count of Loan_Status to measure the number of loans per category in each state.
  ## Findings
**States with Highest Loan Activity:**
- California: Recorded the highest number of loans (6,897), with 5,697 fully paid loans and 1,057 charged off.
- New York: A significant volume of loans (3,701), with 3,123 fully paid loans and 468 charged off.
- Texas: High activity with 2,666 loans, of which 2,298 were fully paid.
**States with Lowest Loan Activity:**
- Idaho: Minimal loan activity with just 6 loans, all in the Fully Paid category.
- Maine and Nebraska: Recorded only 3 and 5 loans respectively.
**Regional Observations:**
- Urban Centers: States with large metropolitan areas (e.g., California, New York, Texas) dominate loan activity, suggesting a concentration of borrowers in these regions.
- Rural States: States with smaller populations or rural profiles (e.g., Idaho, Wyoming) show significantly lower loan volumes.
   ## Results
  ![Screenshot (110)](https://github.com/user-attachments/assets/3895e085-d264-4d8c-af99-9846edda1c9c)
![Loan_Status Count by State](https://github.com/user-attachments/assets/5d89d8de-8617-41e2-9ccb-8409a99ec29e)
________
#### Analysis of Average Interest Rates by Month
## Approach
- A new column named Loan_Issue_Month was created using the formula:
```excel
=TEXT([@[Issue_Date]],"mmmm")
```
This formula extracts the month from the Issue Date column and formats it as the full month name.
- Rows: Used the Loan_Issue_Month column to categorize data by month.
- Values: Calculated the Average of Interest Rate (Int_Rate) for each month, allowing for a clear comparison.
## Findings
- January and July recorded the lowest average interest rates (10%).
- May had the highest average rate (16%).
- September through November maintained a consistent rate of 12%.
- February, August, and December saw slightly higher rates (11%) compared to the lowest months.
## Results
![Screenshot (111)](https://github.com/user-attachments/assets/d731e706-74c6-461f-a3a2-ca7fb8744dcb)
![Average Interest Rate Overtime](https://github.com/user-attachments/assets/caf4dbbe-49e9-421f-97f8-02bd7190d80d)
________
#### Analysis of Loan Amount Overtime
## Approach
- Rows: Used Loan_Issue_Month to categorize data by the month the loan was issued.
- Values: Calculated the Sum of Loan Amount for each month to analyze the distribution of loan disbursement.
## Findings
- November had the highest loan disbursement, with a total of $253,222,325.
- October and September also recorded high disbursement volumes ($119,571,300 and $46,301,350, respectively).
- January, February, May, and December saw significantly lower loan disbursement amounts.
- Loan disbursement appears to build momentum from mid-year, with August marking the start of a significant increase in loan volumes.
## Results
![Screenshot (112)](https://github.com/user-attachments/assets/4235f2e2-5ba5-4e79-b862-e643dc33d126)
![Loan Amount Overtime](https://github.com/user-attachments/assets/ac014fe9-2a95-4a92-b1c4-18a635ede02a)
________
#### Analysis of Average Interest Rates by Month
## Approach
## Findings
## Results
________
#### Analysis of Average Interest Rates by Month
## Approach
## Findings
## Results
________
#### Analysis of Average Interest Rates by Month
## Approach
## Findings
## Results
________
#### Analysis of Average Interest Rates by Month
## Approach
## Findings
## Results
________
#### Analysis of Average Interest Rates by Month
## Approach
## Findings
## Results
________
#### Analysis of Average Interest Rates by Month
## Approach
## Findings
## Results
________
#### Analysis of Average Interest Rates by Month
## Approach
## Findings
## Results
________
#### Analysis of Average Interest Rates by Month
## Approach
## Findings
## Results
________
#### Analysis of Average Interest Rates by Month
## Approach
## Findings
## Results
________
#### Analysis of Average Interest Rates by Month
## Approach
## Findings
## Results
________
#### Analysis of Average Interest Rates by Month
## Approach
## Findings
## Results
________
#### Analysis of Average Interest Rates by Month
## Approach
## Findings
## Results
________
#### Analysis of Average Interest Rates by Month
## Approach
## Findings
## Results
________
#### Analysis of Average Interest Rates by Month
## Approach
## Findings
## Results
________
#### Analysis of Average Interest Rates by Month
## Approach
## Findings
## Results
________
#### Analysis of Average Interest Rates by Month
## Approach
## Findings
## Results
________
#### Analysis of Average Interest Rates by Month
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
![Screenshot (113)](https://github.com/user-attachments/assets/baf7b987-7f40-43b8-aa42-45ca7015b02d)
________
## Recommendation

