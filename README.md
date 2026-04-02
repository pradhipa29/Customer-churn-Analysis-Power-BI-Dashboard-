# Customer-churn-Analysis-Power-BI-Dashboard-
Customer Churn Analysis - Interactive Power BI Dashboard

### Telecom Customer Retention Dashboard | Power BI · DAX · Power Query

## Overview

This project showcases an interactive Power BI dashboard built to analyze customer churn and revenue impact using telecom data.

The dashboard allows users to:
- Monitor churn metrics  
- Identify high-risk customers  
- Explore data with filters and slicers  
- Make data-driven decisions  

## Business Objective

**Understand customer churn patterns and reduce revenue loss through actionable insights.**

## Dashboard Features

- **KPI Cards**
  - Total Customers  
  - Churn Rate  
  - Revenue Lost  
  - Avg Monthly Charges  

- **Visualizations**
  - Churn by Contract Type  
  - Churn by Tenure  
  - Churn by Payment Method  
  - Monthly Charges vs Churn  

- **Slicers**
  - Contract Type  
  - Gender  
  - Senior Citizen  
  - Tenure
    
## Key Insights

- Churn Rate: **26.6%** (1 in 4 customers)  
- Month-to-Month: **42.7% churn (highest risk)**  
- Two-Year Contract: **2.8% churn (lowest risk)**  
- Revenue Lost: **$2.86M**  
- High monthly charges → higher churn  
- New customers → higher churn  
- Electronic check → highest churn  

## Business Recommendations

- Convert short-term customers to long-term plans  
- Focus on new customers (0–12 months)  
- Promote auto-pay over electronic check  
- Offer retention discounts for high-paying users  

## DAX Measures

Churn Rate =
DIVIDE(
    CALCULATE(COUNTROWS(Customers), Customers[Churn] = "Yes"),
    COUNTROWS(Customers)
)

Revenue Lost =
CALCULATE(
    SUM(Customers[TotalCharges]),
    Customers[Churn] = "Yes"
)

Avg Charge Churned =
CALCULATE(
    AVERAGE(Customers[MonthlyCharges]),
    Customers[Churn] = "Yes"
)
Project Structure
customer-churn-powerbi/
│
├── CustomerChurn.pbix
├── powerbi_dashboard.png
└── README.md

# Tools Used
Power BI Desktop
DAX
Power Query
Data Modeling

# Dataset
IBM Telco Customer Churn Dataset
7,032 Customers · 21 Features

# Author

Pradhipa S
Aspiring Data Analyst
pradhipasuresh16@gmail.com
https://www.linkedin.com/in/pradhipa29
