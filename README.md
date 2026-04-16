# NYC Wage Compliance Audit: Fiscal Year 2025

## Project Overview
This repository contains a forensic payroll audit of New York City municipal employees for the 2025 fiscal year. By analyzing a dataset of over 6 million records from NYC Open Data, this study identifies potential labor law violations where employees classified as **Exempt (Managerial/Executive)** were paid overtime despite exceeding the legal salary threshold.

## Problem Statement
Under NY State and NYC labor standards, employees in managerial roles earning above **$64,350/year** are generally exempt from overtime pay. This analysis identifies instances where these thresholds were surpassed yet OT payments were still disbursed, representing potential budgetary leakage and administrative non-compliance.

---

## Analysis Methodology
* **Data Transformation:** Filtered 6.7M records to a verified sample based on active employment status, "Per Annum" pay basis, and managerial titles.
* **Compliance Logic:** Applied boolean flags (`is_manager`, `is_violation`) to records where Base Salary > $64,350 and OT Paid > 0.
* **Tech Stack:**
    * **SQL (BigQuery):** Primary data extraction, cleaning, and transformation.
    * **Google Sheets:** Statistical enrichment, data aggregation, and pivot table analysis.

---

## Key Discoveries

| Metric | Result |
| :--- | :--- |
| **Total Flagged Records** | 502 |
| **Max Threshold Violation** | $122,057.18 |
| **Financial Liability** | $10,616,321.19 |
| **Primary Risk Sectors** | DEPARTMENT OF SANITATION |

---

## Repository Contents

| File Name | Description |
| :--- | :--- |
| `NYC_Payroll_Transformed_Data.csv` | Processed dataset with calculated fields for hourly rates. |
| `Payroll_Aggregation_Summary.xlsx` | Workbook containing pivot tables and final liability calculations. |
| `analysis_queries.sql.txt` | Recovered SQL logic for data cleaning and transformation. |

---

## Contact and Professional Background
* **Benjamin Hough**
* **Education:** Bucks County Community College | Phi Theta Kappa Honor Society
* **Email:** [benh2734@gmail.com](mailto:benh2734@gmail.com)
* **LinkedIn:** [View Professional Profile](https://www.linkedin.com/in/benjamin-hough-34b6473a5)
