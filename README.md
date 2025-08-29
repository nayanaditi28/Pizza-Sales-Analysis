# 🍕 Pizza Sales Analytics (SQL + Power BI)

An end-to-end analytics project analyzing pizza sales data to generate KPIs, discover trends, and rank best/worst products.  
Uses **SQL** for querying and **Power BI** for building an interactive, executive-ready dashboard.

---

## 📌 Overview
This project covers:
1. Understanding raw sales data.
2. Importing data into SQL Server.
3. Writing queries for KPIs, trends, and rankings.
4. Connecting SQL to Power BI for visualization.
5. Delivering business insights.

---

## 📊 Dataset
- **File:** `pizza_sales.csv`
- **Granularity:** Each row = 1 pizza type in an order.
- **Columns:**
  - `order_id`, `order_date`, `pizza_name`
  - `pizza_category`, `pizza_size`
  - `quantity`, `total_price`

---

## 🛠 Tools & Tech
- **SQL Server** + SSMS
- **Power BI Desktop**
- **Power Query** for cleaning & transformation

---

## 🎯 Goals
- Calculate core KPIs.
- Identify daily & monthly order trends.
- Find revenue share by category & size.
- Rank pizzas by revenue, quantity, and orders.

---

## 📈 KPIs
- **Total Revenue:** ₹817,860.05  
- **Total Orders:** 21,350  
- **Total Pizzas Sold:** 49,574  
- **Average Order Value (AOV):** ₹38.31  
- **Avg Pizzas per Order:** 2.32  

---

## 🗂 SQL Analysis
### Trends
```sql
SELECT DATENAME(WEEKDAY, order_date) AS order_day,
       COUNT(DISTINCT order_id) AS total_orders
FROM pizza_sales
GROUP BY DATENAME(WEEKDAY, order_date);

SELECT DATENAME(MONTH, order_date) AS month_name,
       COUNT(DISTINCT order_id) AS total_orders
FROM pizza_sales
GROUP BY DATENAME(MONTH, order_date);
##Revenue Share

##By Category:

Classic – ₹220,053.10

Supreme – ₹208,197.00

Chicken – ₹195,919.50

Veggie – ₹193,690.45

By Size:

L – ₹375,318.70

M – ₹249,382.25

S – ₹178,076.50

XL – ₹14,076.00

XXL – ₹1,006.60

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
##Top & Bottom Products

##Top 5 by Revenue:

The Thai Chicken Pizza – ₹43,434.25

The Barbecue Chicken Pizza – ₹42,768.00

The California Chicken Pizza – ₹41,409.50

The Classic Deluxe Pizza – ₹38,180.50

The Spicy Italian Pizza – ₹34,831.25

##Bottom 5 by Revenue:

The Brie Carre Pizza – ₹11,588.50

The Green Garden Pizza – ₹13,955.75

The Spinach Supreme Pizza – ₹15,277.75

The Mediterranean Pizza – ₹15,360.50

The Spinach Pesto Pizza – ₹15,596.00
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

##Power BI Dashboard

Page 1 – Overview

KPIs

Daily & Monthly Trends

% Revenue by Category & Size

Page 2 – Best & Worst Sellers

Top/Bottom 5 pizzas by Revenue, Quantity, Orders

Category & Size filters

Navigation buttons






