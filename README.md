# 📊 Superstore Power BI Analytics

**End-to-End Business Intelligence Project using the Sample Superstore Dataset**

This repository contains a complete Power BI analytics solution built on the Sample Superstore dataset. It includes data cleaning, modeling, DAX measure development, and dynamic dashboards that highlight sales performance, profitability, customer behavior, and product insights. The project is designed for both business stakeholders and data teams seeking actionable retail and operations intelligence.

---

## 📁 Project Overview

This end-to-end BI project covers:

* Data preparation & normalization
* Dimensional modeling
* Creation of essential DAX measures
* Interactive dashboards for Sales, Profitability, Customer Analytics, and SKU Performance
* Insight summaries & actionable business recommendations

The goal is to deliver a production-ready analytics framework that can be extended with additional business data.

---

## 📂 Data Sources & Schema

**Primary Source File:** *Sample - Superstore* (order-level granularity)

**Key Fields Include:**

* **Order-Level:** Order ID, Order Date, Ship Date, Customer ID
* **Financials:** Sales, Profit, Discount, Quantity
* **Product:** Product ID, Category, Sub-Category
* **Geography:** Region, State, City

**Assumptions:**

* Shipping cost excluded unless provided
* Discounts applied at the order-line level
* Each row represents one product line

---

## 🔧 Transformations & Data Modeling

* Normalized orders ensuring **1 row = 1 product line**
* Built a **Date Dimension** with Year/Quarter/Month derived keys
* Calculated **Profit Margin** at the row level
* Identified **Repeat Customers** via distinct order counts
* Removed or imputed rows with missing Sales or Order Date
* Built relationships using a **star schema** (Fact Orders + Dimensions)

---

## 📐 DAX Measures & KPI Definitions

| KPI                           | Definition                                          |
| ----------------------------- | --------------------------------------------------- |
| **Total Sales**               | `SUM(Sales)`                                        |
| **Total Profit**              | `SUM(Profit)`                                       |
| **Profit Margin %**           | `Total Profit / Total Sales`                        |
| **Average Order Value (AOV)** | `Total Sales / DISTINCTCOUNT(Order ID)`             |
| **Repeat Purchase Rate**      | Customers with >1 order / total customers           |
| **YoY Sales %**               | Growth compared to same period in the previous year |

---

## 🔎 Analytical Steps Performed

### **1. Baseline KPIs & Time Intelligence**

* Calculated KPIs for recent periods vs prior periods
* Built YoY and QoQ trend visuals

### **2. Product & SKU Analysis**

* Identified **Top 10 SKUs** by sales and profit
* Flagged **high-sales, low-margin** products
* Assessed SKU risk and profitability distribution

### **3. Customer Analytics**

* Segmented **new vs repeat** customers
* Measured cohort AOV and contribution to sales
* Analyzed buying patterns across customer segments

### **4. Regional & Category Segmentation**

* Sales and margin by **Region, Category, Sub-Category**, and **Customer Segment**
* Detected geographic growth hotspots

### **5. Inventory Proxy Recommendations**

* Identified SKUs showing rapid QoQ growth
* Flagged items for possible **inventory top-up**

---

## ⚠️ Limitations

* **Inventory on-hand** data is not available → recommendations based on sales velocity only
* **Customer LTV** limited to time period of dataset
* **Marketing/channel attribution** requires additional fields
* Return/refund data not included

---

## 🚀 Suggested Next Steps

* Add inventory-on-hand & lead-time data to compute **reorder points**
* Integrate acquisition channels for **marketing ROI**
* Add returns/refunds to refine **net sales & margin**
* Deploy scheduled refresh + alerts for SKU stockouts and margin drops

---

## 📘 Repository Contents

```
|-- /PowerBI_Dashboard        # .pbix files and report pages
|-- /Data                     # Superstore dataset (if redistributable)
|-- /Documentation            # Insight summaries & business notes
|-- README.md                 # Project overview
```


Just tell me!
