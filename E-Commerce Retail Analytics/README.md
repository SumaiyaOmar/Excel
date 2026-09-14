# E-Commerce Retail Analytics | Power Query & Excel

## 📌 Project Overview

This project focuses on cleaning, transforming, analyzing, and visualizing a messy e-commerce retail dataset using **Microsoft Excel and Power Query**.

The original dataset contained **12,180 transactions** with issues including inconsistent date formats, invalid quantities, duplicate records, inconsistent categorical values, blank shipping cities, and missing discount and customer rating information.

I used Power Query to build a repeatable cleaning workflow, producing **11,814 analysis-ready transactions**. I then created a business-focused Analysis sheet and an interactive Excel dashboard to explore sales performance across time, products, countries, and order statuses.

---

## 🛠️ Tools & Skills

**Tools:** Microsoft Excel, Power Query, PivotTables, PivotCharts, Excel formulas, Slicers

**Skills:** Data Cleaning, Data Transformation, Data Profiling, Missing-Value Handling, Business-Rule Validation, Sales Analysis, KPI Development, Data Visualization, Interactive Dashboard Design

---

## 📂 Dataset

- **Raw Records:** 12,180
- **Final Clean Records:** 11,814
- **Original Columns:** 13
- **Transaction Period:** January 2024 – June 2026

The dataset includes transaction information such as products, quantities, prices, discounts, payment methods, shipping locations, countries, order statuses, and customer ratings.

---

## 🔄 Data Cleaning & Transformation

Using **Power Query**, I cleaned and prepared the raw dataset for analysis.

Key transformations included:

- Standardized mixed `Order_Date` formats into a valid Date field.
- Standardized inconsistent Country and Payment Method values.
- Removed **192 transactions** containing invalid quantities (`0` or `-1`).
- Replaced **499 blank Shipping City values** with `Unknown` rather than guessing locations.
- Removed **174 exact duplicate transactions**.
- Preserved missing discounts and customer ratings as null where the source did not provide enough information to make a reliable assumption.
- Created `Gross_Sales`, `Discount_Amount`, and `Net_Sales` calculated fields.
- Validated the final dataset before loading it into Excel for analysis.

### Row-Count Audit

| Stage | Records |
|---|---:|
| Raw Dataset | 12,180 |
| Invalid Quantity Records Removed | -192 |
| Exact Duplicates Removed | -174 |
| **Final Clean Dataset** | **11,814** |

---

## 📊 Data Analysis

I created a dedicated **Analysis** worksheet using PivotTables and Excel formulas to examine:

- Overall sales performance
- Monthly sales trends
- Product category performance
- Geographic performance
- Order status performance
- Payment methods
- Customer rating distribution
- Top shipping cities

### Headline Results

| KPI | Result |
|---|---:|
| Total Orders | 11,814 |
| Units Sold | 24,321 |
| Gross Sales | $1,500,541.86 |
| Net Sales | $1,309,641.17 |
| Average Order Value | $117.93 |
| Average Customer Rating | 3.90 |

An important consideration during the analysis was incomplete discount information. **709 transactions did not contain enough information to calculate Net Sales reliably**, so Gross Sales was used as the primary complete sales measure.

---

## 📈 Interactive Dashboard

I built a single-screen Excel dashboard to provide a clear overview of business performance.

### Dashboard KPIs

- Total Orders
- Units Sold
- Gross Sales
- Average Order Value

### Visualizations

- Monthly Gross Sales Trend
- Gross Sales by Product Category
- Orders by Status
- Gross Sales by Country

The dashboard includes interactive slicers for **Year, Product Category, and Country**, allowing users to filter all four visualizations dynamically.

Separate helper PivotTables were used to support the dashboard without changing the detailed Analysis worksheet.

---

## 💡 Key Insights

- The cleaned dataset contains **11,814 valid transactions** generating approximately **$1.50M in Gross Sales**.
- **Electronics** was the highest-grossing product category at approximately **$404.8K**.
- The **United Arab Emirates** recorded the highest Gross Sales among the seven countries at approximately **$226K**.
- **Delivered** was the most common order status with **6,472 orders**.
- **5,846 customer ratings** were available, with an average rating of approximately **3.90/5**.
- **709 transactions** lacked sufficient discount information to calculate Net Sales reliably, highlighting the importance of distinguishing missing information from actual zero values.

---

## 🏠 Workbook Structure

The workbook includes:

| Sheet | Purpose |
|---|---|
| **Home** | Project overview and navigation |
| **Analysis** | Detailed business analysis |
| **Dashboard** | Interactive KPI and visualization dashboard |
| **Cleaned Data** | Final dataset produced through Power Query |

The **Home page** provides direct navigation to the Analysis, Dashboard, and Cleaned Data sections.

---

## 📸 Screenshots

### Home Page
_Add Home page screenshot here._

### Cleaned Data
_Add cleaned dataset screenshot here._

### Analysis
_Add Analysis worksheet screenshot here._

### Dashboard
_Add interactive dashboard screenshot here._

---

## 📚 What I Learned

Through this project, I strengthened my ability to:

- Build a repeatable data-cleaning workflow using Power Query.
- Identify data-quality issues before beginning analysis.
- Apply business rules instead of relying only on technical data validation.
- Handle missing information without making unsupported assumptions.
- Build business-focused PivotTable analyses and KPIs.
- Create an interactive Excel dashboard using PivotCharts, slicers, and Report Connections.
- Present an Excel analytics project in a structured, portfolio-ready format.
