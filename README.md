# 🏥 Hospital Workforce Intelligence Dashboard

## Project Overview

This project analyses hospital workforce data to uncover patterns in staff distribution, salary structures, job satisfaction, sick day trends and overtime across departments. The goal is to provide hospital management with clear, data-driven insights that support better HR decision making.

The analysis was carried out using **Power BI** for data cleaning, transformation and dashboard visualisation.

\---

## Tools Used

* **Power BI Desktop** — Data cleaning (Power Query), Dashboard building
* **Microsoft Excel / CSV** — Raw dataset format

\---

## Dataset Description

The dataset contains **1,500 records** of hospital staff across 8 departments and 5 hospitals.

### Columns in the dataset:

|Column|Description|
|-|-|
|Staff ID|Unique identifier for each staff member|
|Full Name|Full name of the staff member|
|Gender|Gender of the staff member|
|Age|Age of the staff member|
|Department|Hospital department the staff belongs to|
|Job Role|Specific role within the department|
|Hospital|Hospital the staff member is assigned to|
|Employment Type|Full-Time, Part-Time or Contract|
|Shift Type|Morning, Afternoon or Night|
|Years of Experience|Number of years the staff member has worked|
|Annual Salary ($)|Yearly salary of the staff member|
|Hours Per Week|Total hours worked per week|
|Overtime Hours Per Week|Hours worked beyond the standard 40 hours|
|Sick Days Taken|Number of sick days taken in the year|
|Job Satisfaction|Staff satisfaction level — High, Medium or Low|
|Employment Status|Active, Resigned or On Leave|
|Year|Year the record was captured|

\---

## Data Cleaning Steps

The raw dataset was intentionally dirty to simulate real world data quality issues. The following cleaning steps were carried out in **Power Query (Power BI)**:

1. **Removed duplicate rows** — 28 duplicate records were identified and removed
2. **Standardised Gender values** — Inconsistent entries like male, M, MALE, female, F, FEMALE were all standardised to Male / Female
3. **Standardised Department names** — Typos and casing issues like Emergancy, EMERGENCY, I.C.U, Paediatrics, Surgrey were corrected to their proper names
4. **Standardised Employment Type** — Variations like FullTime, full-time, FULL TIME, Contractor were cleaned and standardised
5. **Standardised Shift Type** — Entries like AM, MORNING, Night Shift, NIGHT were standardised to Morning, Afternoon, Night
6. **Handled missing numerical values** — Missing Hours Per Week values were replaced with **32** (the column average rounded to the nearest whole number)
7. **Handled missing categorical values** — Missing Shift Type and Job Satisfaction entries were replaced with **Unknown** rather than being removed or guessed. Unlike numerical columns where a missing value can be replaced with an average, categorical columns like Shift Type and Job Satisfaction cannot be assumed — there is no logical or statistical basis to decide what shift someone worked or how satisfied they were if that information was not recorded. Replacing with Unknown preserves the record in the dataset while honestly acknowledging the gap in the data
8. **Removed salary outliers** — Impossible salary entries (0, 1000, 500000, 999999) were identified and removed as they were clearly data entry errors
9. **Trimmed whitespace** — Extra spaces found in Full Name entries were removed

\---

## Dashboard Overview

The dashboard was built on a single page in Power BI with a purple theme and contains the following visuals:

### KPI Cards

* **Total Staff** — Overall headcount across all departments and hospitals
* **Average Annual Salary** — Mean salary across all staff
* **Average Overtime Hours** — Mean overtime hours per week per staff member
* **Average Sick Days** — Mean sick days taken per staff member per year

### Charts

* **Average Salary by Department** — Bar chart showing which departments pay the most and least
* **Staff Count by Shift Type** — Pie chart showing the distribution of staff across Morning, Afternoon and Night shifts
* **Employment Type Split** — Donut chart showing the proportion of Full-Time, Part-Time and Contract staff
* **Job Satisfaction Breakdown** — Bar chart showing how many staff fall into High, Medium and Low satisfaction levels
* **Staff Count by Department** — Horizontal bar chart showing headcount across all 8 departments

\---

## Key Insights \& Recommendations

### 1\. Salary by Department

Surgery and Oncology pay the most, which reflects the specialized skills required in those roles. However Oncology has the lowest staff count despite being the highest paying department. The hospital should use the high salary as a recruitment tool to attract more Oncology professionals and close that staffing gap before it affects patient care.

### 2\. Shift Type Distribution

Morning, Afternoon and Night shifts are covered almost equally which shows the hospital maintains consistent 24 hour coverage. However Night shift workers should be monitored regularly as working nights long term takes a toll on health and energy levels. A wellbeing check in programme for Night shift staff is recommended.

### 3\. Employment Type Balance

Full-Time, Part-Time and Contract staff are almost evenly split at roughly 33% each. This is a healthy and flexible staffing model that gives the hospital stability while maintaining workforce flexibility. This balance should be maintained going forward.

### 4\. Job Satisfaction

More staff fall in the Medium and Low satisfaction range than High which is a warning sign. The hospital should run an anonymous staff survey to identify root causes and introduce practical remedies such as flexible scheduling, clear promotion paths, training opportunities and a staff recognition programme. If left unaddressed this risks increasing resignations which is far more costly than investing in staff wellbeing upfront.

### 5\. Department Staffing

Radiology has the highest staff count while Oncology has the lowest despite being the highest paying department. A targeted recruitment drive for Oncology is recommended to investigate and address this imbalance.

### 6\. Sick Days

Nearly 10 sick days per staff member per year across 1,400+ staff represents a significant number of lost working days for the hospital. Management should break this down by department to identify which areas are most affected and investigate whether the cause is health related, workload related or a wider workplace culture issue.

### 7\. Overtime

The average overtime of 2.85 hours per week is not alarming and no major overtime crisis exists in the current data. However overtime should continue to be monitored, particularly in high pressure departments like ICU and Emergency, to ensure it does not increase quietly over time.

### 8\. General Ward Salary vs Headcount

General Ward has 176 staff, one of the larger departments, yet records the lowest average salary. These are frontline workers doing day to day patient care and feeling underpaid compared to colleagues in other departments puts them at higher risk of leaving. The hospital should review General Ward salary bands and introduce incremental pay increases tied to years of experience and performance. If General Ward staff are also showing low job satisfaction, low salary is very likely a contributing factor and the case for a pay review becomes even stronger.

\---

## Recommendations Summary

1. Use Oncology's high salary as a recruitment tool to attract more specialized staff
2. Introduce a wellbeing check in programme specifically for Night shift staff
3. Maintain the current balanced split between Full-Time, Part-Time and Contract staff
4. Run an anonymous staff survey to identify root causes of low job satisfaction
5. Introduce flexible scheduling, promotion paths, training and staff recognition programmes
6. Break down sick days by department to identify the most affected areas
7. Continue monitoring overtime especially in ICU and Emergency departments
8. Review and increase salary bands for General Ward staff tied to experience and performance

\---

## Author

**Chisom**
Aspiring Data Analyst | Currently building skills in Excel, SQL, Python and Power BI

\---

*This project was completed as part of a data analytics portfolio building journey.*

