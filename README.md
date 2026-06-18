# Amazon Supply Chain Analytics Dashboard

## Project Overview

This project is an end-to-end Business Intelligence solution developed using **MySQL** and **Power BI** to analyze supply chain sales performance, product profitability, and business trends.

The objective of this project is to transform raw transactional data into actionable insights through data modeling, SQL-based data preparation, DAX calculations, and interactive Power BI dashboards.

---

## Business Problem

Organizations need visibility into:

- Revenue performance
- Product profitability
- Sales trends
- Order volume
- Category performance
- Product-level contribution

This dashboard provides executives and business users with an interactive platform to monitor KPIs and identify high-performing products and categories.

---

## Tools & Technologies

| Tool | Purpose |
|--------|----------|
| Power BI | Dashboard Development & Visualization |
| MySQL | Data Storage & Data Modeling |
| SQL | Data Cleaning & Transformation |
| DAX | KPI and Business Calculations |
| Power Query | Data Preparation |
| GitHub | Version Control & Project Portfolio |

---

## Dataset

Data Source: DataCo Supply Chain Dataset

The dataset contains:

- Orders
- Products
- Customers
- Shipping Information
- Sales Transactions
- Profit Metrics

---

## Data Modeling

A Star Schema model was implemented.

### Fact Table

- Fact_Sales

### Dimension Tables

- Dim_Product
- Dim_Customer
- Dim_Date
- Dim_Shipping

### Schema

```text
                Dim_Date
                    |
                    |
Dim_Product ---- Fact_Sales ---- Dim_Customer
                    |
                    |
              Dim_Shipping
```

---

## Data Preparation

The following data preparation steps were performed:

- Data Cleaning using SQL
- Handling Null Values
- Date Transformation
- Creating Date Dimension
- Fact and Dimension Table Design
- Relationship Creation
- Data Validation

---

## Key Performance Indicators (KPIs)

### Executive Dashboard

- Total Revenue
- Total Profit
- Total Orders
- Profit Margin %
- Revenue Trend
- Profit Trend

### Product Analytics Dashboard

- Total Products
- Top 10 Products by Revenue
- Revenue by Category
- Profit by Category
- Product Performance Analysis

---

## DAX Measures

### Total Revenue

```DAX
Total Revenue =
SUM(fact_sales[sales])
```

### Total Profit

```DAX
Total Profit =
SUM(fact_sales[order_profit_per_order])
```

### Total Orders

```DAX
Total Orders =
DISTINCTCOUNT(fact_sales[order_id])
```

### Profit Margin

```DAX
Profit Margin =
DIVIDE(
    [Total Profit],
    [Total Revenue]
)
```

### Year-over-Year Growth

```DAX
YoY Growth % =
DIVIDE(
    [Total Revenue] -
    [Previous Year Revenue],
    [Previous Year Revenue]
)
```

---

# Dashboard Pages

## 1. Executive Dashboard

Features:

- Revenue KPI
- Profit KPI
- Order KPI
- Profit Margin KPI
- Revenue Trend Analysis
- Profit Trend Analysis
- Revenue by Category
- Interactive Filters

### Key Metrics

| Metric | Value |
|----------|----------|
| Revenue | 9.64M |
| Profit | 1.05M |
| Orders | 27K |
| Profit Margin | 10.89% |

---

## 2. Product Analytics Dashboard

Features:

- Total Products
- Top 10 Products by Revenue
- Revenue by Category
- Profit by Category
- Revenue vs Profit Scatter Analysis
- Product Category Filtering
- Year Filtering

### Key Metrics

| Metric | Value |
|----------|----------|
| Products | 98 |
| Revenue | 9.64M |
| Profit | 1.05M |
| Profit Margin | 10.89% |

---

## 3. Product Performance Drillthrough

Features:

- Product-Level Analysis
- Revenue
- Profit
- Order Count
- Quantity Sold

Allows users to drill from category-level insights down to individual product performance.

---

## Dashboard Screenshots

### Executive Dashboard

![Executive Dashboard](Images/ExecutiveDashboard.png)

### Product Analytics Dashboard

![Product Analytics](Images/ProductAnalytics.png)

### Product Drillthrough

![Product Drillthrough](Images/ProductDrillthrough.png)

---

## Key Insights

- Generated total revenue of **9.64M**
- Achieved total profit of **1.05M**
- Maintained a profit margin of **10.89%**
- Cleats and Camping & Hiking categories generated the highest revenue
- Identified top-performing products through revenue and profitability analysis
- Enabled detailed product-level investigation through drillthrough functionality

---

## Future Enhancements

- Customer Analytics Dashboard
- Supply Chain Performance Dashboard
- Shipping Delay Analysis
- Geographic Sales Analysis
- Forecasting Models
- Advanced Tooltips
- Dynamic KPI Selection

---

## Project Structure

```text
amazon-supply-chain-analytics-powerbi
│
├── PowerBI
│   └── Amazon Dashboard.pbix
│
├── SQL
│   ├── Database Creation.sql
│   ├── Data Cleaning.sql
│   ├── Fact Sales.sql
│   └── Dimension Tables.sql
│
├── Images
│   ├── ExecutiveDashboard.png
│   ├── ProductAnalytics.png
│   └── ProductDrillthrough.png
│
└── README.md
```

---

## Author

**Ayush Vibhor**

Data Analyst | Supply Chain Intelligence & Business Analytics

Skills:
- Power BI
- SQL
- MySQL
- Data Visualization
- Business Intelligence
- DAX
- Supply Chain Analytics

---

### Connect

If you found this project useful, feel free to connect and provide feedback.
