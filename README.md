# Ecommerce-Sales-Analysis

### Project Overview
This project analyzes Ecommerce sales data from 01/12/2010 to 09/12/2011 for a UK-based and registered non-store online retail.
The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.

### Data Sources
The analysis is based on a “Ecommerce.csv dataset” containing sales data from 01/12/2010 to 09/12/2011.
{https://www.kaggle.com/datasets/carrie1/ecommerce-data/data}

### Tool Used
- Excel: Data Cleaning
- SQL Server: Data Analysis
- Power BI: Data Visualization.

### Data Cleaning/Pre-processing
Data cleaning and pre-processing were carried out at the initial stage to ensure data quality, and the following tasks were performed;
- Data loading and inspection 
- Fixing the un-standardized date format
- Handling duplicates and foreign characters(used find and replace)
- Data cleaning and formatting

### Exploratory Data Analysis (EDA)
The EDA process involves analyzing the Ecommerce dataset to understand the distribution of variables, identify patterns and trends, detect potential issues, and answer key questions:
1.  What is the sales trend over time?
2.  Which stock code account for the product with the highest revenue? Top 6?
3.  Total sales for each product(stockcode).
4.  Which country has the highest number of customers?
5.  Which products are selling the most in terms of quantity?
6.  Average order size(quantity) per invoice?
7.  Which country has the highest sales revenue? Top 10?
8.  What is the distribution of sales across different countries?
9.  Which invoice date has the highest sales volume?
10. Are there any pattern in invoice date(More sales on certain days)?

### Data Analysis
Data analysis was done in SQL Server.
~~~sql
---What is the sales trend over time?

SELECT YEAR(InvoiceDate) AS Year,
FORMAT(InvoiceDate, 'MMM') AS Month, SUM(Quantity * UnitPrice) AS TotalSales
FROM Ecommerce
GROUP BY YEAR(InvoiceDate), MONTH(InvoiceDate), FORMAT(InvoiceDate, 'MMM')
ORDER BY TotalSales DESC;
~~~

### Results/Findings
### Recommendations
### Limitations


