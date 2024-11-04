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

This structured approach aims to deliver a comprehensive understanding of sales performance,facilitating data-driven decision-making for future strategies



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

1. Excel

Purpose: Excel is great for initial data exploration and quick analysis. It allows for easy manipulation of data and visualization through pivot tables and charts.

2. SQL

Purpose: SQL is ideal for querying large datasets efficiently and performing complex analyses. It provides a robust framework for data manipulation and retrieval.

3. Power BI

Purpose: Power BI is designed for data visualization and business intelligence, allowing users to create interactive reports and dashboards. It makes it easier to communicate insights derived from data.

4.  Github

Purpose: Github is iseal for portfolio building and public showcasing of the work done.



**Data Cleaning and Preparation**

Data cleaning is a crucial step in the data analysis process that ensures data is accurate, consistent, and complete. Here are some steps you can take to clean data for analysis: 

![Screenshot (560)](https://github.com/user-attachments/assets/a2328b07-ed69-42d9-8f91-d17356486506)

Before cleaning

![Screenshot (562)](https://github.com/user-attachments/assets/debaaa07-d85d-4621-a2e9-95f0f9ea5a89)

After cleaning

**Remove duplicates**

Highlighted all data (Ctrl + A) and removed duplicates via Data tab > Remove Duplicates option. This step removed 40,079 duplicate values, leaving 9,921 unique records.

**Calculate revenue**

Added a new column to calculate revenue using the formula Quantity * Unit Price for each order.

Purpose:

Calculating revenue allows us to analyze total earnings per product, region, and period, which is essential for evaluating sales performance and profitability. 


**Instructions**

1. Excel:
   
o Perform an initial exploration of the sales data. Use pivot tables to summarize 
total sales by product, region, and month.

o Use Excel formulas to calculate metrics such as average sales per product and 
total revenue by region.

o Create any other interesting report


2. SQL:

Hint – You need to load the dataset into your SQL Server environment to write and 
validate your queries.

Write queries to extract key insights based on the following questions. 

o retrieve the total sales for each product category.

o find the number of sales transactions in each region.

o find the highest-selling product by total sales value.

o calculate total revenue per product.

o calculate monthly sales totals for the current year.

o find the top 5 customers by total purchase amount.

o calculate the percentage of total sales contributed by each region.

o identify products with no sales in the last quarter.


3. Power BI:

o Create a dashboard that visualizes the insights found in Excel and SQL.
 The dashboard should include a sales overview, top-performing products, and 
regional breakdowns





**Data Analysis**

Excel

1) Product	Sum of Revenue

Shoes	613380

Shirt	485600

Hat	316195

Gloves	296900

Jacket	208230

Socks	180785

Grand Total	**2101090**

![Screenshot (564)](https://github.com/user-attachments/assets/7abc7ce1-1a26-4f0e-ad2e-0b38f77050e1)


![image](https://github.com/user-attachments/assets/51cabbce-3751-4557-a1e5-10663666ee68)




Insight: 
Shoes and shirt are the best selling products for the period in review




2) **Sales by region**

   
South	927820

East	485925

North	387000

West	300345

Grand Total	 2,101,090.00 


![Screenshot (568)](https://github.com/user-attachments/assets/890f7479-d9ef-4cad-b974-cafc8b99a395)


Row Labels	Sum of Revenue
South	927820
East	485925
North	387000
West	300345
Grand Total	 2,101,090.00 




![Screenshot (570)](https://github.com/user-attachments/assets/174d9edf-9782-4125-b9da-2a779b9f0896)


**Revenue per month
**



![image](https://github.com/user-attachments/assets/05d8521a-23af-4c3f-8e14-7ac0186e03c6)


![Screenshot (573)](https://github.com/user-attachments/assets/6118d03b-7383-46eb-a0bf-4da1920419f1)


![Screenshot (576)](https://github.com/user-attachments/assets/6e84e220-9ca3-4f66-89fa-e49ddbce206a)



Insight : The business made most revenue in febuary and july, april,september and december brought in least revenue.

Considering these festive periods(april & december), the revenue ought to greatly increase during these months.

Close attention should be made to correct whatever affected the sales during these periods



**Use Excel formulas to calculate metrics

**


**Average Sales per Product:**
 =AVERAGEIF(range,criteria[average-range]) 


Copy and paste the product to column K, then remove duplicate in order to have our unique product list. Then use the formular =AVERAGEIF(C:C,N2,H:H) to calculate our average sales for each product. Where “C:C” rep our product column, “N2” rep the product we are working with, “H:H” rep our Sales Column.


![Screenshot (577)](https://github.com/user-attachments/assets/b362e814-eba4-4912-a039-c53d7ee2d359)



![Screenshot (581)](https://github.com/user-attachments/assets/b31a1c95-b6f6-4c29-bcd7-5b5856d14c82)




**Total Revenue by Region**

 =AVERAGEIF(range,criteria[average-range]) 

Copy and paste the Region to column K, then remove duplicate in order to have our unique Region list. Then use the formular =SUMIF(D:D,Table2[@Region],H:H) to calculate our sum of revenue for each region. Where “D:D” rep our Region column, “Table2[@Region” rep the region we are working with, “,H:H” rep our Revenue Column.


![Screenshot (582)](https://github.com/user-attachments/assets/ed20455a-b3ba-4bf1-97f5-a5857ad379ab)




![Screenshot (583)](https://github.com/user-attachments/assets/1b0d7f5b-7987-4731-9d2e-2c13b8ce9093)

























































































































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

each product.
 

 
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





