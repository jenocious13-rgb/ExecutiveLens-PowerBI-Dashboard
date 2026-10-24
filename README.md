# ExecutiveLens | Power BI Sales & Margin Intelligence Dashboard

An executive business intelligence dashboard built in Power BI to monitor sales performance, profitability margins, and regional product trends.

---

## 📊 Dashboard Overview

![ExecutiveLens Dashboard](dashboard.png)

---

## 📌 Executive KPIs
* **Total Revenue:** $2.30M
* **Total Profit:** $286K
* **Profit Margin:** 10.2%
* **Total Orders:** 5,009

---

## 🛠️ Data Modeling & DAX Measures
Structured with a Star Schema connecting transactions to customer, product, and temporal dimensions.

* **Total Revenue:**
  `Total Revenue = SUM(fact_sales[Sales])`
* **Total Profit:**
  `Total Profit = SUM(fact_sales[Profit])`
* **Profit Margin %:**
  `Profit Margin % = DIVIDE([Total Profit], [Total Revenue], 0)`
* **Total Orders:**
  `Total Orders = DISTINCTCOUNT(fact_sales[Order ID])`
* **Calculated Columns:**
  * `YearMonth = FORMAT(fact_sales[Order Date], "YYYY-MM")`
  * `Year = YEAR(fact_sales[Order Date])`

---

## 🔍 Key Insights
1. **Top Profit Drivers:** Copiers and Phones generate the highest profit margins within the Technology segment.
2. **Regional Margin Dynamics:** The West and East regions lead overall sales volume and net profits.
3. **Seasonality:** Q4 shows a consistent revenue spike across all operating years.
