# Retail-Demand-Inventory-Optimization  

## Table of Contents
- [Project Overview](https://github.com/Emjay-19/Retail-Demand-Inventory-Optimization/blob/main/README.md#project-overview)
- [Problem Statement](https://github.com/Emjay-19/Climate-Impact-on-Agricultural-Productivity/blob/main/README.md#problem-statement)
- [Data Source](https://github.com/Emjay-19/Climate-Impact-on-Agricultural-Productivity/blob/main/README.md#data-source)
- [Tools and Methodologies](https://github.com/Emjay-19/Climate-Impact-on-Agricultural-Productivity/blob/main/README.md#tools-and-methodologies)
- [Business Questions](https://github.com/Emjay-19/Climate-Impact-on-Agricultural-Productivity/blob/main/README.md#business-questions)
- [Exploratory Data Analysis (EDA)](https://github.com/Emjay-19/Climate-Impact-on-Agricultural-Productivity/blob/main/README.md#exploratory-data-analysis-eda)
- [Key Insights](https://github.com/Emjay-19/Climate-Impact-on-Agricultural-Productivity/blob/main/README.md#key-insights)
- [Summary of Findings](https://github.com/Emjay-19/Climate-Impact-on-Agricultural-Productivity/blob/main/README.md#summary-of-findings)
- [Recommendations](https://github.com/Emjay-19/Climate-Impact-on-Agricultural-Productivity/blob/main/README.md#recommendations)
- [Limitations](https://github.com/Emjay-19/Climate-Impact-on-Agricultural-Productivity/blob/main/README.md#limitations)
- [Conclusion](https://github.com/Emjay-19/Climate-Impact-on-Agricultural-Productivity/blob/main/README.md#conclusion)



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
- Which warehouses require greater inventory attention  
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
- Which warehouses have the greatest demand concentration?  
- Which warehouses should receive more inventory focus?  
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

<img width="551" height="311" alt="Screenshot 2026-08-24 195401" src="https://github.com/user-attachments/assets/d08ea0d4-30ca-442d-880d-099ea993783a" />


<img width="630" height="338" alt="Screenshot 2026-08-24 182814" src="https://github.com/user-attachments/assets/d1cf4ddc-3ae7-4a72-9864-a8139f4bdbe6" />

<img width="627" height="338" alt="Screenshot 2026-08-24 182902" src="https://github.com/user-attachments/assets/23a4193a-ae72-4ee1-b3d7-a76e997e3d81" />

<img width="629" height="338" alt="Screenshot 2026-08-24 182940" src="https://github.com/user-attachments/assets/d6245027-0308-4704-85dc-10a7821e9e9b" />




## Key Insights  

**Demand vs Revenue:** High-demand products were not always the highest-revenue products. TBOX recorded the highest demand (136.83M units), while VideoRight generated the highest revenue ($1.67M), highlighting the need to evaluate both volume and value when making production decisions.  

**Peak Demand Period:** October recorded the highest monthly demand, indicating a potential seasonal demand peak that should be considered when planning inventory and production capacity.  

**Peak Ordering Hour:** 10 PM recorded the highest order demand, indicating a strong concentration of activity during late hours and suggesting that fulfillment capacity should be aligned with peak ordering periods.  

**Weekday Demand:** Monday recorded the highest demand among weekdays, suggesting that inventory availability and warehouse capacity should be strengthened ahead of the start of the business week.  

**Warehouse Demand vs Revenue:** Cedar Park recorded the highest warehouse demand (1.25B units), while Berkeley generated the highest warehouse revenue ($12.05M). This indicates that the warehouse handling the greatest order volume is not necessarily the highest-value location, making both demand and revenue important for allocation decisions.  

**Warehouse Specialization:** Differences in demand across warehouse-category combinations reveal opportunities for strategic product positioning, allowing warehouses to focus inventory on categories with stronger local demand.  

**Demand Concentration:** The concentration of demand across specific products, periods, and warehouses suggests that inventory planning should be prioritized around high-demand combinations rather than distributed evenly across all products and locations.  

**Production Prioritization:** Products with high demand, strong revenue contribution, and positive demand trends represent the strongest candidates for increased production or replenishment, while consistently low-performing products should be reviewed for potential inventory reduction.  

## Recommendations
**1. Prioritize High-Demand Products**  

Products with consistently high demand should receive greater production and replenishment priority to minimize potential supply gaps.  

**2. Balance Demand and Revenue**  

Production decisions should consider both demand volume and revenue contribution. High-volume products and high-value products may require different strategies.  

**3. Strengthen Demand Forecasting**  

Use the observed monthly trends, seasonal patterns, and MoM changes as inputs into future demand forecasting models.  

**4. Prepare for Peak Periods**  

The concentration of demand around specific weekdays and hours should guide warehouse staffing, fulfillment capacity, and inventory availability.  

**5. Optimize Warehouse Allocation**  

Warehouses experiencing consistently high demand should be evaluated for increased inventory capacity and operational resources.  

**6. Leverage Warehouse Specialization**  

Warehouse-category demand patterns can be used to strategically position products where they are most frequently demanded.  

**7. Prioritize High-Opportunity Locations**  

Regions and warehouse-product combinations with high demand and strong revenue contribution should receive greater inventory focus.  

**. Enhance Future Analysis**  

Future iterations should incorporate inventory levels, supplier lead times, purchase orders, stockouts, carrying costs, and replenishment cycles to develop a more comprehensive inventory optimization solution.  

## Limitations  
- The dataset covers only two years, limiting the ability to identify long-term trends and recurring seasonal patterns over multiple years.  
- The analysis is based on order demand, not actual inventory levels. Therefore, stockouts, inventory on hand, safety stock, and inventory turnover cannot be directly measured.  
- Weekend demand analysis is not applicable because orders do not occur on weekends.  
- The dataset does not provide sufficient information to calculate traditional inventory optimization metrics such as reorder points, lead times, economic order quantity (EOQ), or stockout rates.  
- Regional analysis is limited to the available ZIP Code/region information.  
- Historical demand patterns do not guarantee future demand and should be complemented with additional forecasting models.  

## Conclusion  

The Retail Demand & Inventory Optimization project demonstrates how transactional retail data can be transformed into actionable business intelligence using Power BI.  

The three dashboards provide a connected view of:  

**Product Performance → Demand Trends → Warehouse Optimization**  

The analysis helps Nova Retail Solutions understand what products to prioritize, when demand occurs, and where inventory should be allocated.  

By combining demand, revenue, time, product, and warehouse analysis, the dashboard provides a practical foundation for improving demand forecasting, production planning, replenishment decisions, and inventory allocation.  

Ultimately, the project moves beyond simply reporting historical performance and provides leadership with a data-driven framework for making better operational decisions.  

## Link to Power BI Report  

[Power BI ](https://app.powerbi.com/view?r=eyJrIjoiMTJhOTUwZDUtNGI4Yy00NmM1LTkzOTItMGQyYzA3MGVhZTZjIiwidCI6ImM0Njk0ZTkyLWUyYWQtNGJkOC1hZWE3LTA5MzYyOGU2YWU0ZSJ9
)
