# Retail-Demand-Inventory-Optimization

## Project Overview

Retail Demand & Inventory Optimization is a Power BI analytics project developed for Nova Retail Solutions to transform transactional order data into actionable insights for demand forecasting, product planning, and inventory allocation.

The project analyzes product demand, revenue contribution, demand patterns over time, and warehouse performance through three interactive dashboards: Product Performance, Demand Trends, and Warehouse Optimization.  

The analysis combines DAX, Power Query, time intelligence, KPI development, and interactive data visualization to help leadership understand what products to prioritize, when demand occurs, and where inventory should be positioned.  

## Problem Statement

Nova Retail Solutions needs better visibility into product demand, revenue performance, demand fluctuations, and warehouse activity to make effective operational decisions.  

Without a consolidated analytical view, it can be difficult to determine:  

- Which products and categories are driving demand and revenue  
- Which products are underperforming  
- How demand changes across months and seasons  
- When order activity reaches its peak  
- Which warehouses handle the greatest demand and revenue  
- Which warehouses specialize in particular categories  
- Which locations require greater inventory attention  
- Which products should receive increased production or replenishment priority  

The project addresses these challenges by converting raw order data into an interactive decision-support dashboard that connects product performance, demand patterns, and warehouse activity to actionable business decisions.  

## Business Questions Answered  
### Product Performance
- Which products have the highest demand? 
- Which products generate the most revenue?  
- Which categories generate the greatest demand and revenue?  
- Which products are top-performing or underperforming?  
- Which products should receive production or replenishment priority?  
### Demand Trends  
- How has demand changed over time?  
- Are there clear seasonal demand patterns?  
- Which months experience the highest demand?  
- Which weekdays experience the highest demand?  
- What time of day has the highest order activity?  
- Which products are most demanded at different times?  
### Warehouse Optimization  
- Which warehouses fulfill the highest demand?  
- Which warehouses generate the most revenue?  
- Are certain warehouses specialized in specific product categories?  
- Which warehouses or locations have the greatest demand concentration?  
- Which locations should receive more inventory focus?  
- Where should inventory be strategically allocated?  
## Overall Business Decision  

The analysis ultimately answers three core management questions:  

- What should we prioritize?  
- When should we prepare for demand?  
- Where should we allocate inventory?  

This enables Nova Retail Solutions to make more informed decisions around forecasting, production prioritization, replenishment, and warehouse inventory allocation.  

## Tools & Methodology  
### Tools Used  
**Power BI** — Dashboard development, interactive reporting, and visualization  
**Power Query** — Data cleaning, transformation, and preparation  
**DAX** — KPI development, ranking, performance classification, and time intelligence  
**Excel** — Initial data inspection and validation  
### Methodology  

The project followed a structured analytics workflow:  

**1. Data Preparation** 
Reviewed the dataset, validated data types, handled inconsistencies, and prepared date and time fields for analysis.

**2. Data Transformation**  
Created a dedicated Calendar table with Year, Quarter, Month, Weekday, and Year-Month attributes. The order time was also transformed into Hour and Time of Day categories.

**3. Data Modeling**  
A star schema was implemented in Power BI, with Fact_Table at the center and four supporting dimension tables: Dim_Product, Dim_Warehouse, Calendar, and Dim_Time.  

Fact_Table: Stores order transactions, demand, revenue, product, warehouse, date, and time information.  
Dim_Product: Supports product and category performance analysis.  
Dim_Warehouse: Enables warehouse and regional analysis using warehouse and ZIP information.  
Calendar: Supports monthly trends, seasonality, weekday analysis, and MoM time intelligence.  
Dim_Time: Enables analysis by hour and time of day.  

All dimension tables have 1: relationships* with the Fact_Table, to support accurate filtering and time-based analysis.    

**4. DAX Analysis**  
Developed measures for demand, revenue, product performance, warehouse performance, ranking, priority classification, and Month-over-Month (MoM) analysis.  

**5. Dashboard Development**  
Built three interactive dashboards:  

Product Performance  
Demand Trends  
Warehouse Optimization  

**6. Insight Generation**  
Translated analytical findings into recommendations for production, replenishment, demand forecasting, and inventory allocation.  

## Key Insights  

**Demand vs Revenue:** High-demand products were not always the highest-revenue products. TBOX recorded the highest demand (136.83M units), while VideoRight generated the highest revenue ($1.67M), highlighting the need to evaluate both volume and value when making production decisions.  

**Peak Demand Period:** October recorded the highest monthly demand, indicating a potential seasonal demand peak that should be considered when planning inventory and production capacity.  

**Peak Ordering Hour:** 10 PM recorded the highest order demand, indicating a strong concentration of activity during late hours and suggesting that fulfillment capacity should be aligned with peak ordering periods.  

**Weekday Demand:** Monday recorded the highest demand among weekdays, suggesting that inventory availability and warehouse capacity should be strengthened ahead of the start of the business week.  

**Warehouse Demand vs Revenue:** Cedar Park recorded the highest warehouse demand (1.25B units), while Berkeley generated the highest warehouse revenue ($12.05M). This indicates that the warehouse handling the greatest order volume is not necessarily the highest-value location, making both demand and revenue important for allocation decisions.  

**Warehouse Specialization:** Differences in demand across warehouse-category combinations reveal opportunities for strategic product positioning, allowing warehouses to focus inventory on categories with stronger local demand.  

**Demand Concentration:** The concentration of demand across specific products, periods, and warehouses suggests that inventory planning should be prioritized around high-demand combinations rather than distributed evenly across all products and locations.  

**Production Prioritization:** Products with high demand, strong revenue contribution, and positive demand trends represent the strongest candidates for increased production or replenishment, while consistently low-performing products should be reviewed for potential inventory reduction.  


Link to Power BI Report 

[Power BI ](https://app.powerbi.com/view?r=eyJrIjoiMTJhOTUwZDUtNGI4Yy00NmM1LTkzOTItMGQyYzA3MGVhZTZjIiwidCI6ImM0Njk0ZTkyLWUyYWQtNGJkOC1hZWE3LTA5MzYyOGU2YWU0ZSJ9
)
