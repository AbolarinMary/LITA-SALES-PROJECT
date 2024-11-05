**Outline**
---

`
Project Summary
`

`
Project Objectives
`

`
Data Source
`

`
Dataset
`


`
Tools used
`


`
Data Cleaning and Preparation
`


`
Instructions
`

`
Data Analysis
`


Excel

SQL

PowerBI

`
Key Findings
`

`
Conclusion
`

`
Recommendation
`

### Project Summary: Sales Performance Analysis
---

In this project, the goal is to analyze the sales performance of a retail store through a comprehensive exploration of sales data, using Excel, SQL, and Power BI to uncover key insights. The analysis focuses on identifying top-selling products, assessing regional performance, and analyzing monthly sales trends.


### Project Objectives
---

- To Utilize pivot tables to summarize total sales by product, region, and month, providing a clear overview of performance.

. To Employ Excel formulas to derive key metrics such as average sales per product and total revenue by region, offering deeper insights into sales dynamics.

. To Create additional reports to highlight interesting trends or anomalies in the sales data.

. To Retrieve total sales for each product category.

. To Count sales transactions per region to gauge activity levels.

. To Identify the highest-selling product based on total sales value.

. To Calculate total revenue per product to assess profitability.

. To aggregate monthly sales totals for the current year to identify trends.

. To determine the top 5 customers by total purchase amount to understand customer value.

. To calculate the percentage of total sales contributed by each region for a comparative view.

. To identify products with no sales in the last quarter to flag potential issues.

. To develop an interactive Power BI dashboard that encapsulates the insights gained from both Excel and SQL analyses.

. To identify sales overview to provide a snapshot of overall performance.

. To identify top-performing products to highlight key drivers of revenue.

. To identify regional breakdowns to analyze sales distribution and performance across different areas.

This structured approach aims to deliver a comprehensive understanding of sales performance,facilitating data-driven decision-making for future strategies



### Data Source
---

The datasets of this project was provided by ladies in tech africa as an assignment for analytic purpose.


### Dataset
---

The dataset used for this project contains the following fields:

. OrderID: A unique identifier assigned to each order for tracking and reference.

. Customer Id: A unique identifier for each customer, used to distinguish them within the database.

. Product: The item or service being sold in the order.

. Region: The geographic area where the order was placed or fulfilled.

. OrderDate: The date when the order was placed by the customer.

. Quantity: The number of units of the product ordered.

. UnitPrice: The price per individual unit of the product.

. Revenue: The total income generated from the order, calculated as Quantity × UnitPrice.


### Tools used

1. Excel 

. Purpose: Excel is great for initial data exploration and quick analysis. 

. It allows for easy manipulation of data and visualization through pivot tables and charts.

2. SQL

. Purpose: SQL is ideal for querying large datasets efficiently and performing complex analyses. 

. It provides a robust framework for data manipulation and retrieval.

3. Power BI

. Purpose: Power BI is designed for data visualization and business intelligence, allowing users to create interactive reports and dashboards. It makes it easier to communicate insights derived from data.

4.  Github

. Purpose: Github is ideal for portfolio building and public showcasing of the work done.



### Data Cleaning and Preparation
---

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


![Screenshot (584)](https://github.com/user-attachments/assets/c6c3363c-2d6a-4f34-8140-92de9d6869dc)





![Screenshot (583)](https://github.com/user-attachments/assets/1b0d7f5b-7987-4731-9d2e-2c13b8ce9093)




**SQL
**

When loading my dataset I changed the unitsales and quantity column to “int” datatype

ADDED A COLUMN NAME SALES
Alter Table [dbo].[LITA Capstone Dataset SalesData]
add Sales int


SALES COLUMN WAS CALCULATED

```sql
(Update [dbo].[LITA Capstone Dataset SalesData]
Set Sales = quantity * unitprice)
```


**retrieve the total sales for each product category.**

```sql
Total Sales by Product
Select [Product], sum(Revenue) as Total_Revenue from [dbo].[Sales Data]
Group by [Product]
Order by Total_Revenue desc
```


![Screenshot (586)](https://github.com/user-attachments/assets/0b746675-fe54-4861-a4d9-0dbbae35600d)


Insight : -Hats and shoes makes most sales and should be considered for marketing and high stock provision.


**find the number of sales transactions in each region**

```sql
Sales Transactions by Region
Select Region, sum(Revenue) as Sales_Per_Product from [dbo].[Sales Data]
Group by Region
Order by Sales_Per_Product desc
```


![Screenshot (587)](https://github.com/user-attachments/assets/786004aa-533b-4462-88a2-bc03f3de92d8)







**Find the highest-selling product by total sales value**


```sql
select top 1 Product,
sum (sales) AS Total_sales
from [dbo].[LITA Capstone Dataset SalesData]
group by product
order by Total_sales desc
```
Insight: Shoe is the highest selling product with a total sales value of 613380


**calculate total revenue per product.**



![Screenshot (592)](https://github.com/user-attachments/assets/23254779-25d9-4a97-a6dd-f3ddd042ed16)



**calculate monthly sales totals for the current year**

```sql
Select Datefromparts(Year(OrderDate), Month(OrderDate), 1) as Sales_Month, Sum(Revenue) as Monthly_Total  
From [dbo].[Sales Data]
Where Year(OrderDate) = Year(GETDATE())
Group by Datefromparts(Year(OrderDate), Month(OrderDate), 1)
Order by Sales_Month;
```

**Find the top 5 customers by total purchase amount.**

```sql
select top 5 Customer_Id,
sum (Sales) as Total_sales
from [dbo].[LITA Capstone Dataset SalesData]
group by Customer_Id
order by Total_sales desc
```



![Screenshot (590)](https://github.com/user-attachments/assets/74faefae-ad5f-4f30-861f-4a3fdc37a5ea)



**calculate the percentage of total sales contributed by each region**

```sql
select Region,
sum (Sales) as Total_sales,
(sum (sales)*100/
(select sum (sales) from [dbo].[LITA Capstone Dataset SalesData])) as Sales_percentage
from [dbo].[LITA Capstone Dataset SalesData]
group by Region
order by Sales_percentage DESC
```



![Screenshot (589)](https://github.com/user-attachments/assets/e8eb6cea-5c51-4492-9154-7eca3b40c8c3)



Identify products with no sales in the last quarter

```sql
SELECT DISTINCT Product 
FROM [dbo].[LITA Capstone Dataset SalesData]
WHERE Product NOT IN 
(SELECT Product
FROM [dbo].[LITA Capstone Dataset SalesData]
WHERE OrderDate >= DATEADD(QUARTER, -1, GETDATE()))
```


**Key Findings**

Highest Selling Product: Shoes generated the highest revenue, totaling 613,380 units sold.

Revenue by Region: The South region was the top-performing region, generating 927,820 in revenue, followed by East and North regions.

Sales Trends by Month: Sales peaked in February with a revenue of 546,300, while the lowest sales occurred in September and October, indicating a seasonal sales dip.

The analysis reveals a few key insights:

**Product Performance**: Shoes are the most selling item, representing a high sales value across all regions. However,jacket and socks needs  improved marketing 

Regional Sales: The South region shows a significantly higher revenue contribution, which could indicate a strong customer preference or effective marketing strategies within this region.



**Recommendation**


Enhance Marketing for Top-Performing Products Focus on marketing campaigns that promote the top-selling product categories, especially Shoes. Highlighting their popularity could increase brand trust and encourage further purchases.

Product Diversification and Bundling Opportunities To boost revenue from low-performing items like Socks and Jackets, consider creating product bundles or seasonal discounts. This could attract budget-conscious customers and increase average sales per customer.

Targeted Regional Campaigns With the South region demonstrating the highest revenue, additional promotional efforts in East and West could help balance sales distribution. A focus on localized marketing strategies may appeal to unique preferences in each region.

Address Seasonal Sales Fluctuations To combat the dip in sales observed in September and October, consider introducing seasonal promotions or limited-time offers during these months to stimulate demand.

Customer Segmentation and Retention With a large unique customer base, implementing customer segmentation could allow for more tailored marketing. Sending targeted offers based on past purchases can help drive repeat sa














































