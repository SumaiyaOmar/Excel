# 🏢 Apartment Management & Financial Tracking System

## 📌 Project Overview

The **Apartment Management & Financial Tracking System** is an Excel-based property management solution designed to combine day-to-day apartment operations, financial tracking, automated calculations, and management reporting within one connected workbook.

Rather than creating a collection of independent worksheets, the project was designed to behave like a lightweight business application. Apartment, tenant, rent payment, maintenance, and expense data flow into a centralized analysis layer and executive dashboard.

The workbook uses fictional property-management data and was created as a practical portfolio project to demonstrate Excel automation, structured data management, financial analysis, dashboard development, and business-focused workbook design.

---

## 🗂️ System Structure

The workbook contains eight interconnected worksheets:

| Sheet | Purpose |
|---|---|
| **🏠 Home** | Application-style landing page and workbook navigation |
| **🏢 Apartments** | Master apartment, rental rate, and occupancy records |
| **👥 Tenants** | Tenant information, apartment assignments, and lease records |
| **💳 Rent Payments** | Rent transactions, balances, payment status, and payment timing |
| **🔧 Maintenance** | Maintenance requests, priorities, costs, vendors, and management alerts |
| **💰 Expenses** | Property operating expense transactions |
| **📊 Analysis** | Consolidated financial and operational performance analysis |
| **📈 Dashboard** | Executive KPI and property-performance dashboard |

---

## ⚙️ Key Features

### 🏠 Apartment & Tenant Management

The Apartments sheet acts as the master unit database, storing information such as:

- Apartment ID
- Building
- Floor and unit number
- Apartment type
- Bedrooms
- Monthly rent
- Occupancy status

Tenant and lease information is maintained separately so apartment records remain independent of individual tenants.

The Tenants sheet uses **XLOOKUP** to automatically retrieve monthly rent based on the apartment assigned to each tenant.

---

### 💳 Rent Payment Tracking

Rent payments are stored using a **transaction-based structure**, with each payment represented as an individual record rather than creating separate columns for individual months.

The system automatically calculates or retrieves:

- Apartment ID
- Rent due
- Outstanding balance
- Payment status
- Payment timing

Payment status distinguishes between:

- Paid
- Partial
- Unpaid

Payment timing is tracked separately as:

- On Time
- Late
- Not Paid

Separating payment amount status from payment timing allows a payment to be correctly represented as both **Paid and Late**, for example.

A configurable **Rent Due Day** is referenced using an absolute cell reference so payment-timing calculations can be updated without rewriting the formulas.

---

### ✅ Controlled Data Entry

Data Validation is used throughout the workbook to standardize important fields and reduce inconsistent entries.

Examples include:

- Tenant IDs
- Apartment IDs
- Payment methods
- Maintenance categories
- Maintenance priorities
- Maintenance status
- Expense categories
- Buildings

Dynamic table-based lists allow relevant dropdowns to expand as the underlying tables grow.

---

### 🔧 Maintenance Management

The Maintenance module tracks:

- Service requests
- Apartment
- Request date
- Category
- Description
- Priority
- Status
- Completion date
- Cost
- Vendor
- Days open
- Attention status

`Days_Open` is calculated automatically. Completed requests use the difference between the request and completion dates, while unresolved requests continue aging using `TODAY()`.

An automated **Attention Flag** classifies requests as:

- 🔴 Urgent
- 🟠 Needs Attention
- 🟢 Normal
- ⚪ Closed

Conditional formatting provides visual management alerts based on these classifications.

---

### 💰 Expense Tracking

The Expenses sheet records operating costs across multiple categories, including:

- Utilities
- Cleaning
- Security
- Internet
- Supplies
- Insurance
- Administration
- Landscaping
- Pest Control

Expenses can also be associated with Building A, Building B, or both buildings.

The raw expense table is intentionally kept focused on transaction entry, while calculations and summaries are handled in the Analysis layer.

---

## 📊 Financial & Operational Analysis

The Analysis sheet consolidates information from the operational worksheets into a management-level report.

### 🏢 Property Overview

Tracks:

- Total apartments
- Occupied apartments
- Vacant apartments
- Occupancy rate
- Potential monthly rent

### 💵 Rent Performance

Analyzes:

- Total rent due
- Rent collected
- Outstanding balance
- Collection rate
- Late payments

### 💰 Financial Summary

Calculates:

- Rental income
- Operating expenses
- Maintenance costs
- Total costs
- Net operating result

### 📅 Monthly Financial Performance

Provides month-level analysis of:

- Rent due
- Rent collected
- Outstanding rent
- Operating expenses
- Maintenance costs
- Total costs
- Net result

Date-based analysis uses `SUMIFS` with monthly date boundaries created using `EDATE`.

Where rental data is unavailable, the report preserves **N/A** rather than incorrectly treating missing information as zero.

### ⚠️ Management Attention

The analysis also highlights operational items requiring attention, including:

- Outstanding rent
- Urgent maintenance requests
- Vacant units

---

## 📈 Executive Dashboard

The workbook includes a professionally designed executive dashboard that summarizes the most important property and financial indicators.

### 🎯 KPI Cards

The dashboard displays:

- **Occupancy Rate**
- **Rent Collected**
- **Outstanding Rent**
- **Net Operating Result**

Month-over-month indicators provide additional context for financial performance.

### 📊 Dashboard Visuals

The dashboard includes:

- **Monthly Financial Performance** – comparison of rent collected, total costs, and net result
- **Building Performance** – occupied versus vacant units by building
- **Expense Breakdown** – distribution of major operating expense categories
- **Maintenance Status** – completed, in-progress, and pending requests

### 💡 Quick Insights

A dynamic **Quick Insights** panel translates key calculations into management-friendly statements, including:

- Changes in rent collection
- Changes in outstanding rent
- Changes in net operating result
- Vacant unit count
- Urgent maintenance requests

Semantic colors are used throughout the dashboard so positive and negative changes can be interpreted quickly.

---

## 🧭 Home & Navigation Interface

The Home worksheet was designed as an application-style landing page rather than another analytical dashboard.

It provides direct navigation to:

- 📈 Dashboard
- 🏢 Apartments
- 👥 Tenants
- 💳 Rent Payments
- 🔧 Maintenance
- 💰 Expenses
- 📊 Analysis

Hyperlinks and visual navigation cards allow users to move through the workbook like a lightweight Excel application.

The Dashboard also contains a persistent navigation sidebar for quick access to the operational and reporting sheets.

---

## 📌 Sample Performance Results

The fictional dataset currently produces the following property-level results:

| KPI | Result |
|---|---:|
| 🏢 Total Apartments | **16** |
| ✅ Occupied Apartments | **12** |
| 🔑 Vacant Apartments | **4** |
| 📊 Occupancy Rate | **75%** |
| 💵 Potential Monthly Rent | **$41,900** |
| 🧾 Total Rent Due | **$62,200** |
| 💰 Rent Collected | **$60,650** |
| ⚠️ Outstanding Rent | **$1,550** |
| 📈 Collection Rate | **97.5%** |
| 💸 Operating Expenses | **$20,675** |
| 🔧 Maintenance Cost | **$3,455** |
| 💵 Net Operating Result | **$36,520** |

---

## 🛠️ Excel Skills Demonstrated

- Excel Tables
- XLOOKUP
- Structured References
- Cross-Sheet References
- SUMIFS
- COUNTIF / COUNTIFS
- AVERAGEIF
- IF and Nested IF
- AND
- MAX
- DAY
- TODAY
- EDATE
- Absolute References
- Date Calculations
- Data Validation
- Dynamic Dropdown Lists
- Conditional Formatting
- KPI Development
- Month-over-Month Analysis
- Financial Analysis
- Operational Analysis
- Chart Creation and Formatting
- Dashboard Design
- Workbook Navigation and Hyperlinks
- Data Quality Checks
- Transaction-Based Data Organization
- Business-Rule Logic
