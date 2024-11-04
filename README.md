**Outline**

Project Summary
Project Objectives
Data Source
Dataset
Tools used
Data Cleaning and Preparation
Instructions
Data Analysis
Excel
SQL
Key Findings
Conclusion
Recommendation


**Project Summary: Sales Performance Analysis**

In this project, the goal is to analyze the sales performance of a retail store through a comprehensive exploration of sales data, using Excel, SQL, and Power BI to uncover key insights. The analysis focuses on identifying top-selling products, assessing regional performance, and analyzing monthly sales trends.


**Project Objectives**
To Utilize pivot tables to summarize total sales by product, region, and month, providing a clear overview of performance.

To Employ Excel formulas to derive key metrics such as average sales per product and total revenue by region, offering deeper insights into sales dynamics.

To Create additional reports to highlight interesting trends or anomalies in the sales data.

To Retrieve total sales for each product category.

To Count sales transactions per region to gauge activity levels.

To Identify the highest-selling product based on total sales value.

To Calculate total revenue per product to assess profitability.

To aggregate monthly sales totals for the current year to identify trends.

To determine the top 5 customers by total purchase amount to understand customer value.

To calculate the percentage of total sales contributed by each region for a comparative view.

To identify products with no sales in the last quarter to flag potential issues.

To develop an interactive Power BI dashboard that encapsulates the insights gained from both Excel and SQL analyses.

To identify sales overview to provide a snapshot of overall performance.

To identify top-performing products to highlight key drivers of revenue.

To identify regional breakdowns to analyze sales distribution and performance across different areas.

#This structured approach aims to deliver a comprehensive understanding of sales performance, facilitating data-driven decision-making for future strategies#



**Data Source**
The datasets of this project was provided by ladies in tech africa as an assignment for analytic purpose.

**Dataset**
The dataset used for this project contains the following fields:

OrderID: A unique identifier assigned to each order for tracking and reference.

Customer Id: A unique identifier for each customer, used to distinguish them within the database.

Product: The item or service being sold in the order.

Region: The geographic area where the order was placed or fulfilled.

OrderDate: The date when the order was placed by the customer.

Quantity: The number of units of the product ordered.

UnitPrice: The price per individual unit of the product.

Revenue: The total income generated from the order, calculated as Quantity × UnitPrice.


**Tools used**
















































































1. Excel Analysis
Initial Exploration:
Data Cleaning i.e
Remove duplicates and blanks
Sort


Pivot Tables:
 1) Pivot table to summarize total sales by product. 
Product in the Rows field and Sales Amount in the Values field.




2)Pivot table to summarize Sales by region. 
Region in Rows and Sales Amount in Values.



3) Pivot table to summarize monthly sales.
 Month in Rows and Sales Amount in Values.


##Calculating Metrics:##
Using excel formulas

Average Sales per Product:
 =AVERAGE(range_of_sales_amounts) where the range includes all sales for each product.
 

 
Total Revenue by Region:
Use a formula: =SUMIF(range_of_regions, region_name, range_of_sales) to get total revenue for each region.
Additional Reports:

Consider creating a report that shows the sales trend over time using a line chart, comparing total sales per month.
2. SQL Queries
Setup:

Load your sales dataset into SQL Server.
Key Queries:

Total Sales for Each Product Category:

sql
Copy code
SELECT ProductCategory, SUM(SalesAmount) AS TotalSales
FROM Sales
GROUP BY ProductCategory;
Number of Sales Transactions in Each Region:

sql
Copy code
SELECT Region, COUNT(TransactionID) AS NumberOfTransactions
FROM Sales
GROUP BY Region;
Highest-Selling Product by Total Sales Value:

sql
Copy code
SELECT TOP 1 Product, SUM(SalesAmount) AS TotalSales
FROM Sales
GROUP BY Product
ORDER BY TotalSales DESC;
Total Revenue per Product:

sql
Copy code
SELECT Product, SUM(SalesAmount) AS TotalRevenue
FROM Sales
GROUP BY Product;
Monthly Sales Totals for the Current Year:

sql
Copy code
SELECT MONTH(SaleDate) AS Month, SUM(SalesAmount) AS MonthlyTotal
FROM Sales
WHERE YEAR(SaleDate) = YEAR(GETDATE())
GROUP BY MONTH(SaleDate);
Top 5 Customers by Total Purchase Amount:

sql
Copy code
SELECT TOP 5 CustomerID, SUM(SalesAmount) AS TotalPurchase
FROM Sales
GROUP BY CustomerID
ORDER BY TotalPurchase DESC;
Percentage of Total Sales Contributed by Each Region:

sql
Copy code
SELECT Region, 
       SUM(SalesAmount) * 100.0 / (SELECT SUM(SalesAmount) FROM Sales) AS PercentageContribution
FROM Sales
GROUP BY Region;
Products with No Sales in the Last Quarter:

sql
Copy code
SELECT Product
FROM Products
WHERE ProductID NOT IN (
    SELECT ProductID
    FROM Sales
    WHERE SaleDate >= DATEADD(QUARTER, -1, GETDATE())
);
3. Power BI Dashboard
Creating the Dashboard:

Data Import:

Load your Excel summaries and SQL query results into Power BI.
Visualizations:

Create a sales overview card displaying total sales.
Use bar charts for top-performing products.
Implement a pie chart or a stacked bar chart for regional breakdowns.
Add line charts to show monthly sales trends.
Interactivity:

Use slicers for product categories and regions to allow users to filter the data dynamically.
Publishing:

Once your dashboard is ready, publish it to the Power BI service.
4. GitHub Repository
Creating the Repository:
Create a new repository on GitHub for this project.
Include the following:
A README.md file detailing your project, objectives, and how to use the dashboard.
Folder structure for your Excel files, SQL scripts, and Power BI files.
Any additional documentation or insights you gathered during the analysis.
Final Steps
Review all your findings and visualizations to ensure accuracy.
Prepare a presentation or report summarizing your insights for stakeholders.
Good luck with your project! If you need any specific help along the way, feel free to ask!




Column Titles
1. Excel Analysis
Initial Exploration:

Sales by Region:
Create a pivot table with "Region" in Rows and sum of "Revenue" in Values.
Monthly Sales:
Use "OrderDate" (grouped by month) in Rows and sum of "Revenue" in Values.
Calculating Metrics:

Average Sales per Product:

excel
Copy code
=AVERAGEIF(ProductRange, ProductName, RevenueRange)
Total Revenue by Region:

excel
Copy code
=SUMIF(RegionRange, RegionName, RevenueRange)
Additional Reports:

Create a line chart for monthly revenue trends or a bar chart for sales by customer.
2. SQL Queries
Make sure your SQL queries reflect the specific columns:

Total Sales for Each Product:

sql
Copy code
SELECT Product, SUM(Revenue) AS TotalSales
FROM Sales
GROUP BY Product;
Number of Sales Transactions in Each Region:

sql
Copy code
SELECT Region, COUNT(OrderID) AS NumberOfTransactions
FROM Sales
GROUP BY Region;
Highest-Selling Product by Total Sales Value:

sql
Copy code
SELECT TOP 1 Product, SUM(Revenue) AS TotalSales
FROM Sales
GROUP BY Product
ORDER BY TotalSales DESC;
Total Revenue per Product:

sql
Copy code
SELECT Product, SUM(Revenue) AS TotalRevenue
FROM Sales
GROUP BY Product;
Monthly Sales Totals for the Current Year:

sql
Copy code
SELECT MONTH(OrderDate) AS Month, SUM(Revenue) AS MonthlyTotal
FROM Sales
WHERE YEAR(OrderDate) = YEAR(GETDATE())
GROUP BY MONTH(OrderDate);
Top 5 Customers by Total Purchase Amount:

sql
Copy code
SELECT TOP 5 CustomerId, SUM(Revenue) AS TotalPurchase
FROM Sales
GROUP BY CustomerId
ORDER BY TotalPurchase DESC;
Percentage of Total Sales Contributed by Each Region:

sql
Copy code
SELECT Region, 
       SUM(Revenue) * 100.0 / (SELECT SUM(Revenue) FROM Sales) AS PercentageContribution
FROM Sales
GROUP BY Region;
Products with No Sales in the Last Quarter:

sql
Copy code
SELECT Product
FROM Sales
WHERE Product NOT IN (
    SELECT Product
    FROM Sales
    WHERE OrderDate >= DATEADD(QUARTER, -1, GETDATE())
);
3. Power BI Dashboard
Creating the Dashboard:

Data Import:

Import the Excel files and SQL query results into Power BI.
Visualizations:

Total Revenue: Card visualization for overall revenue.
Top Products: Bar chart showing total revenue by product.
Sales by Region: Pie chart or stacked bar chart for revenue by region.
Monthly Trends: Line chart for monthly sales totals.
Interactivity:

Add slicers for "Region" and "Product" to allow users to filter results.
4. GitHub Repository
Structure:
README.md for project overview.
Folders for:
Excel files.
SQL scripts.
Power BI files.





