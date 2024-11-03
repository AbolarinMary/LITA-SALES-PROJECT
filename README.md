# LITA-SALES-PROJECT
Summary:
The goal of this project is to analyze the sales performance of a retail store, uncovering insights on top-selling products, regional performance, and monthly sales trends. An interactive Power BI dashboard will be created to visualize these findings.

Instructions:
1. Excel Analysis:
a. Initial Exploration:

Import the sales data into Excel.
Create Pivot Tables to summarize:
Total sales by product
Total sales by region
Total sales by month
b. Metrics Calculation:

Use Excel formulas to calculate:
Average sales per product:
excel
Copy code
=AVERAGE(sales_range)
Total revenue by region:
excel
Copy code
=SUMIF(region_range, region_name, sales_range)
c. Additional Reports:

Consider creating a report showing sales trends over time using line charts.
Analyze sales by customer demographics, if available.
2. SQL Queries:
Load the dataset into SQL Server, then execute the following queries:

a. Total Sales by Product Category:

```sql
SELECT ProductCategory, SUM(SalesAmount) AS TotalSales
FROM SalesData
GROUP BY ProductCategory
```

b. Number of Sales Transactions by Region:

sql
Copy code
SELECT Region, COUNT(TransactionID) AS NumberOfTransactions
FROM SalesData
GROUP BY Region;
c. Highest-Selling Product:

sql
Copy code
SELECT TOP 1 ProductName, SUM(SalesAmount) AS TotalSales
FROM SalesData
GROUP BY ProductName
ORDER BY TotalSales DESC;
d. Total Revenue per Product:

sql
Copy code
SELECT ProductName, SUM(SalesAmount) AS TotalRevenue
FROM SalesData
GROUP BY ProductName;
e. Monthly Sales Totals for the Current Year:

sql
Copy code
SELECT MONTH(SaleDate) AS Month, SUM(SalesAmount) AS TotalSales
FROM SalesData
WHERE YEAR(SaleDate) = YEAR(GETDATE())
GROUP BY MONTH(SaleDate);
f. Top 5 Customers by Purchase Amount:

sql
Copy code
SELECT CustomerName, SUM(SalesAmount) AS TotalPurchase
FROM SalesData
GROUP BY CustomerName
ORDER BY TotalPurchase DESC
LIMIT 5;
g. Percentage of Total Sales by Region:

sql
Copy code
SELECT Region, 
       SUM(SalesAmount) * 100.0 / (SELECT SUM(SalesAmount) FROM SalesData) AS SalesPercentage
FROM SalesData
GROUP BY Region;
h. Products with No Sales in the Last Quarter:

sql
Copy code
SELECT ProductName
FROM Products
WHERE ProductName NOT IN (
    SELECT ProductName 
    FROM SalesData
    WHERE SaleDate >= DATEADD(QUARTER, -1, GETDATE()
);
3. Power BI Dashboard:
a. Create the Dashboard:

Import the summarized data from Excel and the results from SQL queries into Power BI.
Visualizations to include:
Sales Overview: Total sales figures and growth indicators.
Top-Performing Products: A bar chart displaying the highest-selling products.
Regional Breakdown: A map or pie chart showing sales distribution across regions.
Monthly Trends: A line chart illustrating sales trends over the months.
b. Interactivity:

Use slicers for users to filter by product category, region, or time period.
Ensure that all visuals update dynamically based on the selections made.
Repository:
Maintain a folder structure for organized storage of:
Raw data files
Excel files with Pivot Tables and reports
SQL scripts
Power BI files (.pbix)
Conclusion:
This project will provide valuable insights into sales performance, enabling the retail store to make data-driven decisions for future strategies. The interactive Power BI dashboard will serve as a comprehensive tool for ongoing performance monitoring.



By messaging ChatGPT, you agree to our Terms and have read our Privacy Policy.
Don't share sensitive info. Chats may be reviewed and used to train our models. Learn more


ChatGPT can make mistakes. Check important info.
?
