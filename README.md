# superstore-powerbi-analytics
A complete Power BI analytics project using the Superstore dataset, including data cleaning, DAX measures, dashboard design, sales insights, profitability analysis, customer behavior metrics, and documented business takeaways.

This project presents a full end-to-end Power BI analysis of the Sample Superstore dataset. It includes data cleaning, modeling, DAX measure creation, and visualization of key metrics such as sales trends, profitability, regional performance, customer segmentation, and repeat-buyer behavior. The repository contains dashboards, documentation, and insight summaries designed for business stakeholders and data teams.

Data sources & schema

Source file: Sample - Superstore (order-level).

Key fields: Order ID, Order Date, Customer ID, Sales, Profit, Discount, Quantity, Product ID, Category, Sub-Category, Region, State, City.

Assumptions: shipping cost not included unless present; discounts are applied at order-line level; each row = one product line.

Transformations

Normalized orders so each row is one product-line.

Created Date dimension and derived Year/Quarter/Month keys.

Computed Profit Margin per row.

Marked Repeat Customer based on distinct order counts per customer.

Removed or imputed rows where Sales or Order Date missing.

Measures & KPIs (definition)

Total Sales — sum of Sales.

Total Profit — sum of Profit.

Profit Margin % — Total Profit / Total Sales.

AOV — Average Order Value = Total Sales / distinct orders.

Repeat Purchase Rate — % of customers with >1 order.

YoY Sales % — growth vs same period previous year.

Analytical steps performed

Calculated baseline KPIs for most recent period and comparable prior period.

Identified top 10 SKUs by sales and by profit.

Segment analysis: sales and margin by Region, Category and Segment (Consumer/Corporate/Home Office).

Customer analysis: repeat vs new customers, AOV by customer cohort.

Product risk assessment: SKUs with high sales but low margin.

Inventory recommendations: SKUs with high share of QoQ growth concentrated in specific regions flagged for top-up.

Limitations

Inventory on-hand not part of dataset (unless provided). Inventory recommendations are proxy-based (sales velocity).

Customer LTV estimates will be limited to observed lifetime in dataset.

Channel attribution depends on presence of Channel or Campaign fields.

Suggested next steps

Add inventory-on-hand and lead time to compute explicit reorder points.

Enrich customer data with acquisition channel for marketing ROI.

Integrate returns / refunds data to refine net sales and margins.

Implement scheduled refresh and alerts for SKU stockouts and margin drops.
