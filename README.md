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
5. Delivering  business insights.

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





