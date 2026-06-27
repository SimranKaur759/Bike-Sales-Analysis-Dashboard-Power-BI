# Bike Sales Analytics Dashboard

> An end-to-end Power BI solution for analyzing bike sales performance, customer behavior, product profitability, and revenue forecasting across global markets.

---

## 📊 Live Dashboard

🔗 [View Interactive Dashboard on Power BI Service](https://app.powerbi.com/groups/me/reports/a2c43215-ee37-4f7c-aa0a-fefcc6b4934f/d4ac1df977b57c502e19?experience=power-bi)

---

## 📁 Project Overview

| Detail | Info |
|---|---|
| **Tool** | Microsoft Power BI Desktop |
| **Data Source** | Excel / CSV |
| **Domain** | Retail Sales & Business Analytics |
| **Target Roles** | BI Developer · Data Analyst |
| **Report Pages** | 10 |

---

## 🎯 Business Problem

A bike retail business needed a centralized analytics solution to:
- Monitor revenue, cost, and profit performance against targets
- Understand what drives customer purchasing behavior and returns
- Identify low-margin products and high-return-rate items hurting profitability
- Simulate the financial impact of pricing and return-rate changes before acting
- Forecast future revenue to support planning decisions

---

## 📐 Data Model

The report is built on a **star schema** with the following tables:

**Fact Table**
- `Sales_facts` — transactional sales records (orders, revenue, cost, returns)

**Dimension Tables**
- `Customer_dim` — customer demographics (income level, occupation, children, priority)
- `Product_dim` — product details (price, margin rate, color, size)
- `Product_categories_dim` — category hierarchy
- `Product_subcategories_dim` — subcategory groupings
- `Territory_dim` — geographic data (country, continent)
- `Calendar_dim` — date table with Year, Month hierarchy

**Supporting Tables**
- `Measure Table` — centralized DAX measures
- `Target Return Rate` — return rate benchmarks
- `Price Increase %` — what-if parameter table
- `Bottom 5 Products by Margin Rate` — calculated product ranking table

---

## 🧮 DAX Measures

Key measures built in a dedicated **Measure Table**:

| Measure | Description |
|---|---|
| `Total Revenue v2` | Core revenue calculation |
| `Total Cost` | Aggregated cost of goods |
| `Total Profit` | Revenue minus cost |
| `Return Rate` | % of orders returned |
| `Repeat Customer Rate` | % of customers with multiple purchases |
| `Total Distinct Customers` | Unique customer count |
| `Total Distinct Orders` | Unique order count |
| `Average Revenue per Customer` | Revenue per unique customer |
| `Average Orders per Customer` | Order frequency per customer |
| `Revenue Impact from Returns` | Revenue lost due to returns |
| `Percentage of All Orders` | Share of orders by segment |
| `Percentage of All Returns` | Share of returns by segment |
| `Target Revenue / Cost / Profit` | KPI target comparisons |
| `Simulated Net Profit` | Profit under what-if scenario |
| `Simulated Return Impact` | Return revenue impact under simulation |
| `Full Simulated Revenue` | Combined revenue under price + return scenario |
| `Simulated Quantity Returned` | Projected returns after decrease |
| `Revenue Rank` | Product ranking by revenue |

---

## 📸 Dashboard Screenshots

| Overview | Scenario Simulation |
|---|---|
| ![Overview](screenshots/slide_1.png) | ![Scenario Simulation](screenshots/slide_2.png) |

| Sales | Customer |
|---|---|
| ![Sales](screenshots/slide_3.png) | ![Customer](screenshots/slide_4.png) |

| Product | Revenue Forecasting |
|---|---|
| ![Product](screenshots/slide_5.png) | ![Forecasting](screenshots/slide_6.png) |

---

## 📋 Report Pages

### 1. 🏠 Overview
![Overview Dashboard](screenshots/slide_1.png)

Executive summary with KPI cards for **Revenue**, **Cost**, and **Profit** vs. targets. Includes:
- Top 5 products by **high return rate** and **low margin %**
- Profit % breakdown by **customer priority type** (donut chart)
- Slicers for Year, Month, Country, and Category

---

### 2. 🔬 Scenario Simulation
![Scenario Simulation](screenshots/slide_2.png)

What-if analysis page powered by **dynamic parameters**:
- Simulates the revenue impact of a **price increase %**
- Simulates the revenue impact of a **return rate decrease**
- Combined full revenue impact KPI
- Simulated vs. Actual Revenue line chart comparison

---

### 3. 📈 Sales
![Sales Dashboard](screenshots/slide_3.png)

Geographic and temporal sales analysis:
- Revenue & cost trends with customer/order counts by month (combo chart)
- **Map visual** for geographic distribution
- **Revenue by Country** funnel chart
- **Customer Repeat Purchase Rate** gauge
- Slicers for Date, Country, Category, Subcategory, Product

---

### 4. 👥 Customer
![Customer Dashboard](screenshots/slide_4.png)

Customer segmentation and behavioral analysis:
- Revenue & return rate by **number of children**
- Revenue share by **number of children** (donut chart)
- Average revenue per customer & return % by **income level**
- % of orders by **occupation** (treemap)

---

### 5. 📦 Product
![Product Dashboard](screenshots/slide_5.png)

Product performance deep-dive:
- Revenue, return rate & margin rank (pivot matrix)
- Revenue share by **subcategory** (treemap)
- Revenue by **color & size** across Mountain Bikes, Road Bikes, and Touring Bikes (ribbon charts)

---

### 6. 📉 Revenue Forecasting (ARIMA)
![Revenue Forecasting](screenshots/slide_6.png)

Advanced forecasting page using **Python visual integration**:
- ARIMA time-series model for top product revenue over 6 months
- Forecast table with projected values

---

### 7–10. 📋 Drill-through Report Pages
Tabular detail pages for deep-dive analysis:
- **Sales by Country** — pivot table of sales by geography
- **Customer Report** — full customer-level pivot
- **Product Report** — product-level margin and return pivot
- **All Products** — complete product catalogue view

---

## ⚙️ Power Query Transformations

- Cleaned and shaped raw Excel/CSV data across all dimension and fact tables
- Built the `Calendar_dim` date table for time intelligence
- Created product category and subcategory hierarchy joins
- Applied data type corrections, null handling, and column renaming
- Merged geography tables to support continent/country slicing

---

## 🔑 Key Insights

- Identified the **top 5 products with the highest return rates**, enabling targeted quality review
- Found that **low-margin products** were concentrated in specific subcategories
- Scenario simulation showed that a **5% price increase combined with a 10% return rate reduction** could significantly lift net profit
- Customer segmentation revealed that **high-income customers** drive disproportionately higher revenue per order
- ARIMA forecasting provided a **6-month revenue outlook** by top product line

---

## 🚀 How to View

**Option 1 — Live (Recommended):**
Click the Power BI Service link above to interact with the live dashboard (no install required).

**Option 2 — Download & Open Locally:**
1. Download `Bike_Sales_Analytics_Dashboard.pbix`
2. Open with [Power BI Desktop](https://powerbi.microsoft.com/desktop) (free)
3. Explore all 10 report pages

---

## 🛠️ Tools & Technologies

- **Power BI Desktop** — report authoring
- **Power Query (M)** — data transformation and shaping
- **DAX** — 18+ custom measures including KPIs, what-if simulations, and time intelligence
- **Python (ARIMA)** — integrated via Power BI Python visual for revenue forecasting
- **Excel / CSV** — data source
- **Power BI Service** — cloud publishing and sharing

---

## 👤 Author

**Simran Kaur**
📧 skaurprofessional@gmail.com
🔗 [LinkedIn Profile](#)
🐙 [GitHub Profile](#)

---

*Feel free to fork this project, explore the data model, or reach out with any questions!*

