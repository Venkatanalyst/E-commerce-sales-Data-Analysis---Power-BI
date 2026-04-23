# 🛒 E-Commerce Sales Analysis using Power BI

---

## 📌 Project Overview

This project provides a comprehensive analysis of an E-commerce Sales dataset to evaluate business health, customer behavior, and regional performance. By transforming raw transactional data into an interactive Power BI dashboard, the project offers a Single Source of Truth (SSOT) for stakeholders to optimize inventory, marketing spend, and sales strategies,
The goal is to transform raw sales data into meaningful insights through **data preprocessing, modeling, and interactive dashboards**.

The project highlights core data analyst skills including **data cleaning, DAX calculations, data modeling, and business insight generation**.

---

## 🎯 Project Objectives

* **Sales Performance Tracking:** Analyze revenue trends across different months and regions.
* **Product Insights:** Identify top-performing categories (Sports, Electronics, etc.) and low-volume products.
* **Customer Segmentation:** Understand spending patterns based on gender and loyalty levels.
* **Operational Efficiency:** Evaluate the impact of payment methods (PayPal, Credit Card, COD) on total revenue.
* **Regional Benchmarking:** Compare sales across the North, South, East, and West regions to identify growth opportunities.

---

## ❓ Problem Statement

Businesses often struggle to understand:

* Which regions are underperforming?
* What is the correlation between customer demographics and purchase volume?
* Are there seasonal dips that require promotional intervention?

This project addresses these gaps by providing clear, data-driven visibility into the end-to-end sales lifecycle.

---

## 📂 Data Source

**Dataset:** E-commerce Sales Data (Multi-table Excel/CSV)

**Tables:** SalesOverall, Customer_Data, Product_Data, Store_Data

**Domain:** E-commerce / Retail Analytics

**Timeline:** 2023 – 2025

---

## 🧾 Attribute Details

| Attribute        | Type      | Description                                           | Usage                              |
|-----------------|----------|----------------------------------------------------|------------------------------------|
| Sales_ID        | Key       | Unique transaction identifier                     | Data modeling & counting           |
| Final Revenue   | Fact      | Total amount earned after discounts               | Main KPI for all visuals           |
| Loyalty_Level   | Dimension | Customer tier (Bronze, Silver, Gold, Platinum)    | Segmentation analysis              |
| Region          | Dimension | Geographic area (North, South, etc.)              | Regional performance comparison    |
| Category        | Dimension | Product group (Beauty, Electronics, Home)         | Category-wise breakdown            |
| Profit Estimate | Measure   | Calculated margin per sale                        | Profitability tracking             |
| Order Date      | Dimension | Date of transaction                               | Time intelligence & trends         |

---

## 🧹 Data Preprocessing Steps

* **Data Cleaning:** Handled missing values in the Cost column and removed leading/trailing spaces in Customer Names.

* **Standardization:** Ensured Date formats were uniform across tables for proper relationship building.

* **Column Engineering:** Created a Category Type column by concatenating Category and Sub-Category.

* **Date Table:** Generated a custom Calendar Table to enable month-over-month (MoM) and Year-to-Date (YTD) analysis.
  
---

## ⚙️ Data Modeling

* **Fact Table:** SalesOverall

* **Dimension Tables:** Customer_Data, Product_Data, Store_Data, Calendar

* **Schema:** Star Schema with One-to-Many (1:*) relationships for optimized query performance.
  
---

## 🧮 DAX Calculations

**Calculated Columns**

**Revenue per Order:** [Amount] * [Quantity]

**Sales Category:** IF([Amount] > [Avg Revenue], "Above Average", "Below Average")


**Measures**

| Measure            | DAX Formula                                                         | Business Use Case                |
|-------------------|----------------------------------------------------------------------|---------------------------------|
| Order Count       | `COUNT('List of Orders'[Order ID])`                                  | Tracks transaction volume       |
| Total Revenue     | `SUM('SalesOverall'[Final Revenue])`                                 | Measures top-line growth        |
| Current YTD       | `TOTALYTD([Total Revenue], 'Calendar'[Date])`                        | Tracks annual progress          |
| Avg Profit Delhi  | `CALCULATE([Avg Profit], FILTER('Store', 'Store'[City] = "Delhi"))`  | Localized performance tracking  |
---

## 📊 Analysis & Visualizations

### 📈 Sales Analysis

* Total Sales, Profit, and Quantity KPIs
* Monthly and yearly sales trends

### 🛍 Category Analysis

* Sales contribution by product category
* Top-performing categories

### 🌍 Regional Analysis

* Sales by region/state
* Identification of high-performing locations

### 👥 Customer Insights

* Customer segmentation
* High-value customers

---

## 📉 Performance Insights

* Certain regions contribute significantly to total revenue
* A few product categories dominate sales
* Sales show seasonal trends across months
* Customer segmentation helps identify key business opportunities

---

## 💡 Key Insights

* **Peak Season:** September is the highest revenue month ($57,511), while June and February are the slowest periods.

* **Regional Dominance:** The North Region is the powerhouse, contributing over 57% of total revenue.

* **Gender Trends:** Females have a higher average revenue ($1,232) compared to males ($1,065), with the largest gap found in the South region.

* **Payment Preference:** PayPal and Credit Cards are the preferred methods, nearly equal in usage, while COD usage peaks significantly in late summer.

---

## 📸 Dashboard Preview


<img width="736" height="328" alt="Screenshot 2026-04-01 022828" src="https://github.com/user-attachments/assets/ad97b018-17f8-47e3-b433-08e48767f14b" />


<img width="648" height="328" alt="image" src="https://github.com/user-attachments/assets/4d7fed0d-e8c1-4a8b-be5c-50501bc2d431" />


<img width="736" height="327" alt="image" src="https://github.com/user-attachments/assets/742cc034-369f-4cb3-8485-227f3dcd02c9" />


---

## 🛠 Tools Used

* **Microsoft Excel:** Initial data exploration and descriptive statistics.

* **Power Query (ETL):** Cleaning nulls, standardizing "Loyalty Level" naming, and merging customer/product details.

* **Power BI:** Data modeling and building the interactive Executive Dashboard.

* **DAX:** Creating calculated measures for YTD Sales, Average Revenue, and Regional Ranks.

---

## 🎯 Outcome

The project delivers an interactive dashboard that helps:

* Track sales performance
* Identify business opportunities
* Support data-driven decision making

---

## 📌 Conclusion

This project successfully converts raw e-commerce transactions into a strategic tool. It highlights that while the North region is stable, targeted marketing towards male customers in the South and promotional activities in June/February could further drive growth.It showcases strong skills in **data analysis, visualization, and business understanding**.

---

## 👨‍💻 Author

**V.Venkatesh**
Data Analyst | Power BI Developer

🌐 **GitHub:** https://github.com/Venkatanalyst 

💼 **LinkedIn:** [Venkatesh Venugopal](https://www.linkedin.com/in/venkatesh-v-dataanalyst/)

📧 **Email:** Calepsundar08@gmail.com

If you found this project useful or have feedback, feel free to reach out!

## 📚 Tags

#PowerBI #DataAnalysis #E-Commerce #SalesAnalytics
#DAX #DataVisualization #ExcelPowerQuery

---
