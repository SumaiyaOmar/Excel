# 📈 Sales Forecasting Model in Excel

## Project Overview

This project analyzes historical Walmart weekly sales data and builds a time-series forecasting model in Microsoft Excel.

The goal was to prepare and validate the historical data, analyze company-wide weekly sales patterns, evaluate the accuracy of an Excel forecasting model using a holdout period, and generate a 12-week future sales forecast.

The project combines Power Query, PivotTables, Excel forecasting functions, model evaluation metrics, data analysis, and dashboard visualization.

---

## Dataset

The dataset contains **6,435 records** covering weekly sales across **45 Walmart stores**.

**Historical period:** February 2010 – October 2012  
**Weekly dates:** 143  
**Stores:** 45

The dataset includes:

- Store
- Date
- Weekly Sales
- Holiday Flag
- Temperature
- Fuel Price
- CPI
- Unemployment

---

## Data Preparation

The dataset was imported and validated using **Power Query**.

Data preparation included:

- Checking column quality, errors, and missing values
- Assigning appropriate data types
- Converting the Date column using the correct locale
- Checking for duplicate Store-Date combinations
- Validating the weekly structure of the dataset

After validation, all **6,435 records** were retained.

---

## Sales Analysis

A PivotTable was used to aggregate sales from all 45 stores into company-wide weekly sales.

This produced **143 historical weekly observations** for forecasting and analysis.

### Historical Performance

- **Average Weekly Sales:** $47,113,419
- **Peak Weekly Sales:** $80,931,416
- **Weeks Analyzed:** 143

The historical trend showed relatively stable weekly sales with several significant sales spikes.

---

## Forecasting Model

The forecasting model was built using Excel's **FORECAST.ETS** function.

To evaluate the model before forecasting future sales:

- The first **131 weeks** were used as training data.
- The final **12 historical weeks** were held out as a test period.
- Forecasts were generated for those 12 weeks.
- Forecast values were compared with the actual sales results.

Forecast errors, absolute errors, and absolute percentage errors were calculated for each test week.

---

## Model Evaluation

Two metrics were used to evaluate forecast accuracy:

| Metric | Result |
|---|---:|
| Mean Absolute Error (MAE) | $1,248,622 |
| Mean Absolute Percentage Error (MAPE) | 3% |

The test-period comparison showed that the forecast generally followed the direction of actual sales while producing a smoother sales pattern.

---

## 12-Week Future Forecast

After evaluating the model, a final 12-week forecast was generated using all **143 weeks of historical sales data**.

### Forecast Summary

- **Forecast Horizon:** 12 Weeks
- **Average Forecast Sales:** $48,451,202
- **Peak Forecast Sales:** $54,652,552
- **Highest Forecast:** 23 November 2012

The forecast indicates a noticeable increase in sales during late November, with forecast sales reaching approximately **$54.65 million**.

---

## Dashboard

The final Excel dashboard presents:

- Average Weekly Sales
- Peak Weekly Sales
- Forecast MAPE
- Average Forecast Sales
- Historical Weekly Sales Trend
- Actual vs Forecast Weekly Sales
- 12-Week Sales Forecast
- Interactive Monthly Sales by Store
- Store slicer for interactive analysis

![Sales Forecasting Dashboard](screenshots/dashboard.png)

---

## Analysis

A dedicated analysis sheet summarizes historical performance, model performance, the future sales outlook, and key business insights.

![Sales Forecasting Analysis](screenshots/analysis.png)

---

## Forecast Model

The forecasting worksheet contains the train/test structure, forecast calculations, error measurements, model evaluation metrics, and future forecast values.

![Excel Forecast Model](screenshots/forecast-model.png)

---

## Excel Skills Demonstrated

- Power Query
- Data validation and cleaning
- PivotTables
- PivotCharts
- Slicers
- Time-series analysis
- FORECAST.ETS
- Train/test forecasting approach
- Forecast error calculation
- MAE and MAPE
- Data visualization
- Dashboard design
- Business insight presentation

---

## Tools Used

**Microsoft Excel**

Power Query was used for data preparation, while Excel formulas, PivotTables, charts, and slicers were used for analysis, forecasting, evaluation, and visualization.
