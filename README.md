# Sales-Analytics_Dashboard
An interactive Power BI dashboard analyzing sales, product performance, executive efficiency, and outlet distribution using advanced DAX and data visualization techinques. 
# 📊 Sales Analytics Dashboard

## 📌 Project Overview
The **Sales Analytics Dashboard** is an interactive Power BI project designed to analyze and visualize sales performance across executives, products, outlets, and geographic locations. This dashboard provides actionable insights to support data-driven business decisions.

## 🎯 Objectives
- Monitor overall sales performance.
- Evaluate executive efficiency and contribution.
- Analyze product and brand performance.
- Assess outlet and geographic distribution.
- Track monthly sales trends and growth.
- Identify top-performing and underperforming areas.

## 📈 Key Features
- ✅ **Executive Performance Dashboard**
  - Sales by Executive
  - Top Performers
  - Executive-wise Orders and City Analysis

- ✅ **Product Insights Dashboard**
  - Sales by Brand and Category
  - Top-Selling Products
  - Orders by Category

- ✅ **Outlet Sales Performance Dashboard**
  - Sales by City and Outlet
  - Outlet Type Distribution
  - Geographic Sales Map

- ✅ **Overall Sales Performance Dashboard**
  - Monthly Sales Trend
  - Orders by Month
  - Sales per Outlet vs Average Order Value
  - Interactive Filters for City and Brand

## 📊 Key KPIs
| KPI | Description |
|-----|-------------|
| **Total Sales** | Overall revenue generated |
| **Total Orders** | Number of orders placed |
| **Total Products** | Count of unique products |
| **Total Outlets** | Number of active outlets |
| **Average Order Value** | Average revenue per order |
| **Sales per Outlet** | Average sales generated per outlet |

## 🛠️ Tools & Technologies
- **Microsoft Power BI**
- **DAX (Data Analysis Expressions)**
- **Power Query (ETL)**
- **Microsoft Excel**
- **Data Modeling (Star Schema)**

## 🧮 DAX Measures Used

```DAX
Total Sales = SUM('Fact Table'[Amount])

Total Orders = DISTINCTCOUNT('Fact Table'[Order ID])

Total Product = DISTINCTCOUNT('Fact Table'[Product Name])

Total Outlets = DISTINCTCOUNT('Fact Table'[Outlet ID])

Avg Order Value = DIVIDE([Total Sales], [Total Orders], 0)

Sales per Outlet = DIVIDE([Total Sales], [Total Outlets], 0)

Prev Month Sales =
CALCULATE(
    [Total Sales],
    DATEADD('Dim_Date'[Order Date], -1, MONTH)
)
RETURN DIVIDE([Total Sales] - Prev, P
