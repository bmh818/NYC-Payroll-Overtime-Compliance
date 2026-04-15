# NYC Managerial Overtime Compliance Audit: Fiscal Year 2025

## Project Overview
This repository contains a forensic payroll audit of New York City municipal employees for the 2025 fiscal year. By analyzing a dataset of over 6 million records from NYC Open Data, this study identifies potential labor law violations where employees classified as **Exempt (Managerial/Executive)** were paid overtime despite exceeding the legal salary threshold.

## Problem Statement
Under NY State and NYC labor standards, employees in managerial roles earning above **$64,350/year** are generally exempt from overtime pay. This analysis identifies instances where these thresholds were surpassed yet OT payments were still disbursed, representing potential budgetary leakage and administrative non-compliance.

---

## Analysis Methodology
* **Data Transformation:** Filtered 6M+ records to a subset of "Per Annum" employees with "Manager", "Director", or "Executive" titles earning > $64,350.
* **Compliance Logic:** Applied a boolean flag to any record where `Base_Salary > 64350` AND `OT_Paid > 0`.
* **Tech Stack:**
    * **SQL (BigQuery):** Heavy lifting for dataset subsetting and "Compliance Flag" engineering.
    * **Python (Pandas):** Exploratory Data Analysis (EDA) and identifying statistical outliers in OT payments.
    * **Tableau/Sheets:** Visualization of agency-wide non-compliance trends and the "Wall of Shame" dashboard.

---

## Key Discoveries

| Metric | Result |
| :--- | :--- |
| **Total Flagged Records** | [TBD - Count of Managers getting OT] |
| **Max Threshold Violation** | [TBD - Highest OT paid to a single Manager] |
| **Estimated Budget Impact** | [TBD - Total sum of all ineligible OT paid] |
| **Highest Risk Agency** | [TBD - Agency with the most flagged records] |

---

## Repository Contents

| File Name | Description |
| :--- | :--- |
| `NYC_Managerial_OT_Subset.csv` | Cleaned dataset of managers earning >$64,350. |
| `Compliance_Analysis.ipynb` | Python Notebook containing statistical summaries and outlier detection. |
| `Manager_Audit_Queries.sql` | SQL scripts for data cleaning, joining, and flag creation. |

---

## Contact and Professional Background
* **Benjamin Hough**
* **Education:** Bucks County Community College | Phi Theta Kappa Honor Society
* **Email:** [benh2734@gmail.com](mailto:benh2734@gmail.com)
* **LinkedIn:** [View Professional Profile](https://www.linkedin.com/in/benjamin-hough-34b6473a5)
