# OPC Mountain Bike Acquisition Strategy

## Role
**SQL Data Analyst** – Outdoor Performance Center

## Timeline
**June 2024 – October 2024**

## Overview
As part of the Outdoor Performance Center (OPC) Data Science Team, I conducted a SQL-based analysis to evaluate the viability of acquiring Ord Cycles. The objective was to assess historical sales, warehouse efficiency, and top-performing mountain bike configurations to support leadership's acquisition decision.

## Tools & Technologies
- PostgreSQL
- SQL
- PowerPoint (for executive presentation)

## Key Contributions
- Queried and cleaned historical sales data (2010–2018)
- Identified monthly and yearly sales trends for mountain bikes
- Analyzed warehouse-level performance by total orders and revenue
- Highlighted top 10 best-selling mountain bike configurations
- Recommended strategic adjustments to product and warehouse operations

## Sample SQL Snippet
```sql
-- Monthly sales trends for mountain bikes
SELECT 
    EXTRACT(YEAR FROM ord_date) AS sale_year,
    EXTRACT(MONTH FROM ord_date) AS sale_month,
    SUM(order_tot) AS monthly_sales
FROM 
    orders
WHERE 
    prod_id IN (SELECT prod_id FROM products WHERE prod_cat_name = 'Mountain Bike')
GROUP BY 
    sale_year, sale_month
ORDER BY 
    sale_year, sale_month;
```

## Outcomes
Insights from this analysis were presented to OPC leadership and used to guide acquisition strategy and resource planning.

---
