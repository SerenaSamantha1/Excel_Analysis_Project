🏦 Bank Loan Report Dashboard
An End-to-End Data Analytics Project using Excel, SQL & Business Intelligence
This project analyzes bank loan data to monitor lending performance, portfolio health, and borrower behavior. I built interactive dashboards in Excel, supported by SQL queries for backend analysis and business logic.

📌 Project Objectives
To create a comprehensive Bank Loan Report that helps stakeholders:
Track loan portfolio performance
Monitor loan quality (Good vs Bad loans)
Analyze customer behavior and loan trends
Support data-driven lending decisions
The project is structured into three dashboards:
Summary Dashboard
Overview Dashboard
Details Dashboard

📂 Project Components
This repository contains:
📊 Excel Dashboards (Summary, Overview, Details)
📄 Problem Statement & Business Requirements
📜 SQL Query Document
📈 Visual Reports and KPI calculations
All business problem definitions and dashboard requirements were taken from your project report. 

BANK LOAN REPORT
📊 Dashboard 1: Summary
This dashboard focuses on high-level KPIs.

Key KPIs:
Total Loan Applications
Total Funded Amount
Total Amount Received
Average Interest Rate
Average Debt-to-Income Ratio (DTI)
MTD & MoM performance metrics

Loan Quality Breakdown:
Loans are classified into:

Good Loans
Fully Paid
Current

Bad Loans
Charged Off

Metrics calculated:
Good Loan %
Bad Loan %
Applications by loan quality
Funded amounts by loan quality
Amount received by loan quality
These classifications and KPIs were defined in your problem document. 
BANK LOAN REPORT

📊 Dashboard 2: Overview
The Overview Dashboard visually analyzes trends and patterns using:

📌 Visualizations Included:
1. Monthly Trends (Line Chart)
Loan Applications
Funded Amount
Amount Received
2. State-wise Loan Distribution (Filled Map)
Shows regional lending activity by US states
3. Loan Term Analysis (Donut Chart)
Distribution between 36 and 60 month loans
4. Employee Length vs Loans (Bar Chart)
Based on borrower employment experience
5. Loan Purpose Analysis (Bar Chart)
Breakdown by loan purposes
6. Home Ownership Analysis (Tree Map)
Own vs Rent vs Mortgage
All chart requirements and logic were based on your official project document. 
BANK LOAN REPORT

📊 Dashboard 3: Details
The Details Dashboard provides detailed data exploration, allowing users to:
Apply filters (Grade, Purpose, Loan Status, etc.)
Drill into loan-level and customer-level analysis
View complete breakdown of loan portfolio information
Its main purpose is to act as a single point of reference for all loan information. 

BANK LOAN REPORT
🧠 SQL Queries Used
All KPIs and dashboard metrics were built using SQL for accuracy.
Some key examples:

Total Loan Applications:
SELECT COUNT(id) AS Total_Applications 
FROM bank_loan_data;

Good Loan Percentage:
SELECT
(COUNT(CASE WHEN loan_status = 'Fully Paid' OR loan_status = 'Current' THEN id END) * 100.0) 
/ COUNT(id) AS Good_Loan_Percentage
FROM bank_loan_data;

Monthly Loan Trend:
SELECT 
MONTH(issue_date) AS Month_Number, 
DATENAME(MONTH, issue_date) AS Month_Name,
COUNT(id) AS Total_Loan_Applications,
SUM(loan_amount) AS Total_Funded_Amount,
SUM(total_payment) AS Total_Amount_Received
FROM bank_loan_data
GROUP BY MONTH(issue_date), DATENAME(MONTH, issue_date)
ORDER BY MONTH(issue_date);

All SQL queries used in this project are documented in query file.

BANK LOAN REPORT QUERY DOCUMENT
🛠️ Tools & Technologies Used
Microsoft Excel – Dashboard Design & Visualization
SQL (MySQL / SQL Server syntax) – Data Analysis
Data Cleaning & KPI Design
Business Intelligence & Reporting

💡 Key Learnings
This project helped me gain hands-on experience in:
✅ Designing business dashboards
✅ Writing production-level SQL queries
✅ Translating business problems into analytics
✅ Financial & lending analytics
✅ Data-driven storytelling

🚀 Why This Project Matters
Banks rely heavily on loan portfolio analysis for risk management and growth strategies.
This project reflects real-world analytics used in financial institutions for:
Credit risk assessment
Loan portfolio optimization
Customer trend analysis
Financial reporting
It showcases my ability to think like a Data Analyst in a financial domain.
