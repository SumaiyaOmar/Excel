# HR Employee Data Cleaning & Analysis

## Project Overview

This project demonstrates an end-to-end HR data cleaning and analysis workflow in Microsoft Excel.

The dataset contained employee records with data quality issues such as duplicate records, missing values, inconsistent text formatting, mixed date formats, invalid salary values, and combined department/region information.

The goal was to transform the raw HR data into a clean, analysis-ready dataset and build an interactive dashboard that provides insights into workforce distribution, salaries, employee performance, remote work, and employees requiring HR attention.

---

## Tools Used

- Microsoft Excel
- Power Query
- PivotTables
- PivotCharts
- Excel formulas
- Slicers

---

## Data Cleaning

Power Query was used to clean and transform the raw employee dataset.

Key cleaning steps included:

- Removed duplicate employee records
- Trimmed unnecessary spaces from text fields
- Standardized capitalization
- Removed the redundant Name column
- Split `Department_Region` into separate Department and Region fields
- Standardized employee status values
- Converted salary values to numeric format
- Standardized email formatting
- Standardized Remote Work values into logical TRUE/FALSE values
- Handled missing and invalid values
- Converted unparseable date values to null rather than making assumptions about ambiguous dates

The `Join_Date` field contained multiple inconsistent date formats. Dates that could not be reliably interpreted were treated as missing values instead of being guessed.

---

## Excel Analysis

After cleaning the data, I performed HR analysis using Excel formulas including:

- `COUNTIF` / `COUNTIFS`
- `SUMIFS`
- `AVERAGEIF` / `AVERAGEIFS`
- `XLOOKUP`
- `IF`
- `AND` / `OR`
- `IFERROR`
- `MIN` / `MAX`
- `SUM` / `AVERAGE`

The analysis covered:

- Workforce status
- Salary statistics
- Age distribution
- Remote vs non-remote employees
- Department workforce and salary analysis
- Regional workforce analysis
- Employee performance
- Department status breakdown
- HR attention flags
- Priority employee reviews

---

## HR Classification

Two employee-level classifications were created to support HR review.

### Needs Attention

An employee is flagged as **Needs Attention** when:

- Performance = Needs Improvement

**OR**

- Status = Pending

### Priority Review

An employee is classified as **Priority Review** when:

- Performance = Needs Improvement

**AND**

- Status = Active

---

## Dashboard

An interactive HR dashboard was created to summarize the most important results.

### KPI Cards

- Total Employees
- Active Employees
- Average Salary
- Remote Employees
- Employees Needing Attention

### Visualizations

- Employee Count by Department
- Average Salary by Department
- Remote vs Non-Remote Performance
- Employees Needing Attention by Department

Interactive slicers allow users to explore the PivotChart results by:

- Department
- Region
- Employee Status

---

## Key Insights

- Sales has the largest workforce with **11 employees**.
- Cloud Tech has the highest average salary at approximately **$15,556**.
- Jeddah has the highest employee count among the analyzed regions.
- **Good** is the most common employee performance rating, with **24 employees**.
- Remote employees have higher counts in the Good and Average performance categories than non-remote employees.
- Data Analytics, Cloud Tech, and Marketing are tied for the highest number of employees flagged as Needs Attention.

---

## Data Quality & Validation

Final quality checks were performed to ensure consistency across the workbook.

- Final cleaned dataset contains **69 employee records**
- Active, Inactive, and Pending employee totals were validated against the total workforce
- Remote and Non-Remote totals were checked against the cleaned dataset
- PivotTable totals were validated against formula-based analysis
- Dashboard KPIs were checked against analysis results
- Power Query refresh functionality was tested
- Dashboard slicers were tested with connected PivotCharts

---

## Project Workflow

Raw HR Data  
→ Power Query Cleaning  
→ Clean Employee Dataset  
→ Formula-Based Analysis  
→ PivotTables & PivotCharts  
→ Interactive HR Dashboard  
→ HR Insights  
→ Final Quality Checks

---

## Skills Demonstrated

This project demonstrates practical experience with:

- Excel data cleaning
- Power Query
- Data transformation
- Data quality validation
- Excel formulas
- Multi-criteria analysis
- XLOOKUP
- PivotTables
- PivotCharts
- Slicers
- Dashboard design
- HR data analysis
- Business insight generation

---

## Dataset

The dataset used for this project is synthetic and was designed to simulate common HR data-quality and employee-management scenarios. No real employee information is included.
