# BigQuery-Looker-Loan-Analysis
Loan health and portfolio analysis for TheLook Fintech using BigQuery and Looker. Evaluated risk exposure across states (notably California) and monitored outstanding balances ($3B+) to drive data-driven lending strategies and risk mitigation.
## 📊 Project Overview
This project focuses on collecting, storing, and analyzing loan health data for TheLook Fintech. By integrating internal datasets with external CSV sources using BigQuery and Looker Enterprise, the analysis provides a comprehensive view of portfolio performance and customer behavior. The final output is an interactive dashboard designed to support executive-level, data-driven decision-making regarding risk management and lending operations.
## 🏦 Business Problem
TheLook Fintech identified a critical need to assess its financial exposure and portfolio health. Key challenges addressed in this analysis include:

High-Risk Exposure: Identifying and flagging when the total outstanding loan amount exceeds the $3 billion threshold.

Default & Delinquency Tracking: Monitoring the distribution of loan statuses, specifically the 9.07% of charged-off loans and the 87.89% of active loans that require continuous oversight.

Geographic Risk Concentration: Analyzing regional data to address high default risks in specific areas, such as California, which currently shows the highest volume of outstanding loans.

Customer Profiling: Identifying high-income borrowers with active loans and home ownership to personalize financial products and ensure responsible lending.
## Project Diagram
<img width="2128" height="496" alt="Project Diagram (2)" src="https://github.com/user-attachments/assets/0bd6b25f-f6a3-4288-9de4-ef6961d1c85f" />
## Methodology
The project followed a systematic data engineering and analytics pipeline within Google BigQuery to transform raw fintech datasets into structured insights:

Data Integration (Inner Joins): Performed an Inner Join between the primary loan table and the state_region table to consolidate geographical data with financial records.

Intermediate Table Creation: Developed a specialized table, loan_with_region, to serve as the foundation for multi-dimensional analysis.

Nested Data Extraction: Utilized Distinct functions and targeted queries on nested data structures to create the loan_purpose table, ensuring the extraction of unique, high-quality values.

Time-Series Aggregation: Created final summary tables to calculate and visualize the total amount in loans issued per year, enabling trend analysis across the 2012–2019 period.

Dashboard Development: Connected the processed BigQuery tables to Looker Enterprise to build interactive visualizations for executive monitoring.

## Skills & Tools
BigQuery & SQL Engineering: Expertise in Inner Joins, managing nested data, and utilizing the DISTINCT keyword for data deduplication.

Data Modeling: Designing intermediate tables (loan_with_region) to optimize query performance and reporting.

ETL Pipeline Design: Implementing a step-by-step workflow from data ingestion to final year-over-year (YoY) financial aggregation.

Business Intelligence: Advanced dashboarding in Looker, focused on status segmentation (Current vs. Charged-off) and regional risk analysis.

Cloud Analytics: End-to-end management of fintech data within the Google Cloud Platform (GCP) ecosystem.

## Results 
The analysis of the loan portfolio revealed critical metrics regarding the organization's financial health and risk exposure:

Portfolio Growth: A consistent upward trend in loan issuance was identified, peaking in 2019 with 51,737 loans, compared to only 2,594 in 2012.

Total Exposure: The total outstanding loan portfolio reached $3,080,553,000, exceeding the high-risk designation threshold of $3B.

Loan Status Distribution: * 87.89% of the portfolio remains in "Current" status.

9.07% of loans have been "Charged-off," representing the primary loss category.

Late loans (31-120 days) account for 1.72% of the total volume.

Geographic Concentration: California (CA) was identified as the state with the highest volume of outstanding loans and elevated default risk.

High-Value Segment: Successfully isolated the top 10 clients characterized by high income, home ownership, and current loan standing for targeted financial products.

## Business Recommendations
Based on the data insights, the following strategic actions are recommended to mitigate risk and optimize the portfolio:

Risk Exposure Mitigation: Pause the issuance of new loans immediately to reassess the company’s risk appetite, as outstanding balances have surpassed the $3B safety limit.

Geographic Diversification: Suspend new loan approvals in California due to high regional concentration and default risk. A deeper geographic risk analysis is required to rebalance the portfolio across other states.

Enhanced Monitoring: Implement an early-warning system for the 87.89% of active loans. Since none are currently "Fully Paid," early detection of repayment risks is crucial to prevent further "Charged-off" losses.

Product Personalization: Leverage borrower income and home-ownership data to develop personalized financial products for the lowest-risk segments, supporting more responsible and profitable lending decisions.

## Final Report
<img width="816" height="1056" alt="Executive summary  (1)" src="https://github.com/user-attachments/assets/a79b4372-070f-41e2-88a4-b2058f921643" />

## Dashboard
<img width="1920" height="1080" alt="image (17)" src="https://github.com/user-attachments/assets/99b26372-fbbd-4b32-8711-ef2a72ab2c4b" />



