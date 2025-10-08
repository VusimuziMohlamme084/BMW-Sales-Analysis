# BMW Car Sales Analysis | Revenue,Trends and Insights
Excel + SQL + Power BI Project | Retail Sales Data | From Raw Data to Business Insights

### Project Overview
This project analyzes BMW car sales data to uncover trends in revenue, product performance, world sales, and profitability.
Using SQL for data exploration, Excel for transformation, and Power BI for visualization, the project turns raw transaction records into actionable business insights.

## Tools and Technologies
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

### 📊 Power BI Visuals Used

The dashboard utilizes the following Power BI visualizations to provide insights into sales data:

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








  
