# BMW Car Sales Analysis | Revenue,Trends and Insights
Excel + SQL + Power BI Project | Retail Sales Data | From Raw Data to Business Insights

## Table Of Content
 * [Project Overview](#project-overview)
 * [Tools & Technologies](#tools--technologies)
 * [Data Cleaning Process](#data-cleaning-process)
 * [Exploratory Analysis](#exploratory-analysis)
 * [Power BI Dashboard](#power-bi-dashboard)
 * [Key Insights](#key-insights)
 * [Recommendations](#recommendations)

### Project Overview
This project analyzes BMW car sales data to uncover trends in revenue, product performance, world sales, and profitability.
Using SQL for data exploration, Excel for transformation, and Power BI for visualization, the project turns raw transaction records into actionable business insights.

## Tools & Technologies
* SQL (PostgreSQL / MySQL / SQLite).
* Excel.
* Power BI.
* Jupyter Notebook or DBeaver for SQL querying.

## Data Cleaning Process
* Converted Date to proper datetime format
* Removed missing or invalid values
* Created new calculated fields:
* New Table for, Total = Unit Price * Quantity Sold
* Revenue = Sum (Total)
* Avg Price = Revenue / Quantity Sold

### Exploratory Analysis

1. #### 📊 Monthly Revenue Trend Analysis

##### This SQL query helps analyze **monthly revenue trends** by aggregating total sales revenue for each month. It's useful for identifying seasonality, growth patterns, and key revenue-driving periods.

##### 🔍 Query:

```sql
SELECT 
    DATE_TRUNC('month', Date) AS Month,
    SUM(Units_Sold * Unit_Price) AS Total_Revenue
FROM stock_sales
GROUP BY Month
ORDER BY Month;
sql
SELECT 
    DATE_TRUNC('month', Date) AS Month,
    SUM(Units_Sold * Unit_Price) AS Total_Revenue
FROM stock_sales
GROUP BY Month
ORDER BY Month;
```
2. #### Top 5 Products by Total Sales

##### This SQL query identifies the **top 5 best-selling products** by total revenue. It helps stakeholders quickly see which products drive the most sales and should be prioritized in marketing, inventory, or sales strategies.

##### 🔍 Query:

```sql
SELECT 
    Product_Name,
    SUM(Total_Sales) AS Revenue
FROM stock_sales
GROUP BY Product_Name
ORDER BY Revenue DESC
LIMIT 5;
```

3. #### 🌍 Revenue by Region

##### This SQL query breaks down **total revenue by region**, allowing you to compare sales performance across different geographical areas. It's useful for regional strategy, resource allocation, and identifying high-performing or underperforming markets.

##### 🔍 Query:

```sql
SELECT 
    Region,
    SUM(Total_Sales) AS Revenue
FROM stock_sales
GROUP BY Region
ORDER BY Revenue DESC;
```

### Power BI Dashboard

#### The dashboard utilizes the following Power BI visualizations to provide insights into sales data:

- **Line Chart**:  
  Displays the monthly revenue trend over time.

- **Clustered Bar Chart**:  
  Shows the top 5 products by total sales revenue.

- **Map Visual (Filled Map or Shape Map)**:  
  Visualizes revenue distribution across different regions.

- **Card Visuals**:  
  Highlight key metrics such as Total Revenue, Total Units Sold, and Average Profit Margin.

- **Slicer**:  
  Allows filtering data by date range, product category, or region for dynamic analysis.

- **Table or Matrix**:  
  Detailed view of sales data by product, region, and month.

---

> 💡 These visuals collectively help in understanding trends, regional performance, and product-level insights.

<img width="1920" height="1039" alt="2025-10-08 (4)" src="https://github.com/user-attachments/assets/84126336-34b4-422f-8fac-1d8cf9418341" />
<img width="1920" height="1022" alt="2025-10-08 (5)" src="https://github.com/user-attachments/assets/4b64f7b3-8e19-4c44-9db2-9334045377af" />

### Key Insights 
---
1. **Top Selling Models:**
   * The BMW Z4 is the top-selling model with a total of **666 units sold**, followed by the BMW 8 Series (641 units) and BMW M4 (620 units).

2. **Revenue Trends:**
   * Total revenue for the BMW Z4 model reached **R51.58M**. It shows a steady increase in sales year-over-year, peaking in 2022 with **R14.04M** in revenue from 176 units sold.
   * The overall revenue for 2023 is showing a solid growth trajectory with a **20.3%** increase compared to the previous year, reaching **R0.05bn**.
   * 
3. **Geographic Sales Distribution:**
   * Sales are concentrated in countries like **Spain**, **South Africa**, and **China**. Spain has sold 39 units, South Africa 15, and China 25.
   * **Thailand** contributes 3 sales, marking a smaller but consistent presence in this market.

4. **Sales by Channel:**
   * Online sales contributed **2.64M** in revenue (21% of total sales), Wholesale was at **0.76M** (4%), and **Dealerships** made up **31%**, equating to **1.41M** in sales.

5. **Sales Trends by Year:**
   * The dashboard indicates an even distribution of sales across years from 2019 to 2022. The **BMW Z4** performed well in all years with noticeable growth in 2022 and 2023.

6. **Most Expensive Models:**
   * The **BMW 8 Series** is noted as one of the most expensive models, with an average price of **R75.6K**.

7. **Sales Revenue by Month:**
   * Monthly data visualizations indicate periodic spikes in sales, with noticeable patterns showing high activity during specific months (Jan, Mar, Jun, Sep, Nov, Dec), aligning with typical automotive sales cycles.

8. **Year-over-Year Sales Growth:**
   * The overall sales growth is robust, especially in 2023, where sales and revenue are showing a marked increase from previous years.

9. **Revenue Distribution (PY):**
   * A comparison of **Revenue** and **Previous Year (PY) Revenue** indicates steady progress, with the current year showing an upward trend in revenue generation.

These insights provide a snapshot of the performance of BMW car models, helping identify key growth areas, trends, and strategies for sales optimization.

### Recommendations:
---
1. **Capitalize on the Success of the BMW Z4:**
   * Since the **BMW Z4** is the top-selling model, BMW should focus on maintaining its market dominance by introducing limited editions, targeted marketing campaigns, and enhancing the customer experience. Special promotions or upgrades for returning customers could further boost sales.

2. **Increase Online Sales and Digital Presence:**
   * With **21% of sales** coming from online channels, there’s an opportunity to expand the digital sales experience. Enhancing the online platform with more customization options, virtual vehicle tours, and exclusive online-only offers could help attract a broader audience and increase revenue from this channel.

3. **Expand Sales in Underperforming Regions:**
   * Focus on markets like **Thailand** and **Morocco**, where sales are relatively low. Tailor marketing strategies and introduce region-specific promotions to capture a larger share of these markets, potentially through localized advertising or targeted discounts.

4. **Focus on High-Margin, Premium Models:**
   * Models like the **BMW 8 Series** and **BMW M4** are more expensive and could offer higher profit margins. BMW should emphasize these models in their advertising campaigns, highlighting luxury features, exclusivity, and performance to attract affluent buyers.

5. **Leverage Seasonal Trends and Sales Cycles:**
   * Sales trends indicate peaks during certain months, such as **January, March, June, September, and December**. BMW should plan targeted promotions and campaigns around these months, offering time-sensitive discounts or exclusive packages to maximize sales during these high-activity periods.







  
