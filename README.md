## Introduction
### This report analyzes sales data using tools like Excel, SQL, and Power BI to uncover key trends and insights. The data contains fields such as Order ID, Customer ID, Products, Region, Order Date, Quantity, Unit Price, Total Sales, Order Year, and Year. The objective is to perform data cleaning, calculations, and visualizations to derive actionable conclusions about sales performance.
### Tools used:
- Excel: Data cleaning, initial exploration, and calculation of key metrics.
- Structured Query Language (SQL): Querying the dataset for deeper analysis and performing aggregations.
- Power BI: Visualizing the data and summarizing key findings through interactive reports and dashboards.
### Data Cleaning, Preparation, and Metrics (EXCEL)
- Removing Duplicates: The raw dataset has multiple entries which could have twisted the total sales. I used the excel feature 'Remove duplicates' to eliminate the repetitive rows and to extract the unique datas (i.e Order id's, Customer id's and products).;
- Pivot tables: In Excel, i used pivot tables to group sales by region, year, month and product category, allowing me to quickly spot which areas were underperforming.
- Formulas and Functions: During the analysis, Excel’s powerful functions were used extensively to calculate key sales metrics and derive actionable insights from the data. By leveraging these formulas, I was able to perform complex calculations quickly and efficiently.
  1. COUNT(): After removing duplicates to extract the unique datas, i used the COUNT function to count the number of cells with numeric values within a specified range. E.g Unique Order Id  (=COUNT(M2:M21))
  2. COUNTA(): After extracting the unique datas such as Unique customer Ids and products, i used the COUNTA function to count cells with variable characters (numbers and texts). E.g Unique customer Id (=COUNTA(S2:S7))
  3. COUNTIF(): To determine the number of times a particular product was sold, I utilized the COUNTIF() function. This helped identify high-selling products. (=COUNTIF(Table3[Product],"shirt")).
  4. AVERAGEIF(): To determine the average price per product, i used the AVERAGEIF() function. It helped to determine the average price of each particular product E.g (=AVERAGEIF(Table3[Product],"gloves",Table3[Total sales])).
  5. SUMIF(): To determine the total sales of a specific product, i used the SUMIF function. E.g (SUMIF(Table3[Product],"shirt",Table3[Total sales])).
  6. TEXT(): Using a TEXT() function in Excel, i was able to isolate the order month and year from the date data. E.g. (=TEXT(E2,"MMM")), (=TEXT(E3,"YYYY"))
  7. Adding calculated column: I added the calculated column below:
  - Total sales = Quantity * Unit price
### Data Organization and Filtering
The dataset was filtered by Region, Year, and Product to explore trends in different segments, making the data easier to analyze.

### SQL (Structured Query Language): Data Extraction and Querying.
### Metrics to Track:
- Total sales for each product  category
- Number of sales transaction in each Region
- Highest selling products by total sales value
- Total revenue per product
- Monthly sales total for the current year
 - Top 5 Customers by Total Purchase Amount
- Percentage pf total sales contributed by each Region
- Products with no sales in the last quarter
### Data Preparation and Sample structure
- order ID: Unique identifier for each Order
- Customer ID: Unique Identifier for each Customer
- Product: Product name
- Region: Sales Region
- OrderDate: Date of the Order
- Quantity: Number of Units sold
- Unit price: Price per unit
- Total sales: Total sales for the order (could be calculated as Quantity * UnitPrice).
- Year: The year the order was placed (extracted from OrderDate).
- Month: The month the order was placed (extracted from OrderDate).
### Queries for Sales Metrics
- Total sales for each product Category: The total sales metric gives an overview of overall performance across all orders.
  [Total sales Query.txt](https://github.com/user-attachments/files/17648735/Total.sales.Query.txt)

- Number of sales transaction in Each product
  [Sales transaction.txt](https://github.com/user-attachments/files/17648850/Sales.transaction.txt)

- Total Revenue per product
  [revenue per product.txt](https://github.com/user-attachments/files/17648938/revenue.per.product.txt)

- Top 5 Customers by total Purchase: Finding the top 5 products by sales is useful for focusing marketing and inventory efforts.
  [top 5 customers.txt](https://github.com/user-attachments/files/17648984/top.5.customers.txt)

- Percentage of Total sales contributed by each Region
  [total sales percentage.txt](https://github.com/user-attachments/files/17649002/total.sales.percentage.txt)

- Product with no sales in the last quarter
  [product with no sales.txt](https://github.com/user-attachments/files/17649038/product.with.no.sales.txt)

### Visual Analysis
[lita1 project.txt](https://github.com/user-attachments/files/17648503/lita1.project.txt)

## Power BI: Interactive Data Visualization
### Data Import and Transformation: 
Power BI helped me to import Data from multiple sources such as Excel sheets and SQL databases by connecting to these sources directly but for this report, data was imported from Excel sheets only. Once the data is imported, Power BI uses Power Query to clean, shape, and merge data as needed. Power Query has an easy-to-use interface to:
- Data Cleaning: This involves removing any unnecessary rows or columns, handling blank or missing values, and making sure each column has a consistent format.
- Data Transformation: I can perform tasks like renaming columns, splitting text, and formatting dates to make the data more usable.
- Data Merging: When data from different sources or tables need to be combined, Power query helps to join these tables on a common field.
### Importance of Data Transormation
 The importance of these is to have a single, organised dataset ready for analysis. This helps saves time, ensure data accuracy, and allows for a seamless transition to visualizing and analyzing the data within Power BI.
### Dashboards and Reports:
Creating dashboards and Reports is essential in Power BI because it helps to display key sales metrics in a clear and interactive way. Dashboards helps to see the overview of important information like total sales, revenue by region, etc. 
### Key Metrics setup
- Total sales: This shows the overall total sales
- Revenue by Region: This breaks down sales by different regions to see where the most revenue is coming from.
- Product performance: It displays the best selling products.
### Visualization Tools Used.
- Cards: Used to display single, large numbers like total sales or a total customers for quick reference.
- Donut Charts: Used for comparing things, like revenue from different products or sales in different regions.
- Clustered Bar chart: Ideal for showing values, measures for more than one item that shares the same category.
- Line Graphs: Ideal for showing trends over time, like monthly or yearly sales growth.
### Data Slicing and Filtering: 
This is an essential tool in Power BI that makes it easy for me to focus on some specific parts of my data without changing the entire dashboard. The Slicer tool helps to add filter controls on my dashboard. E.g Time slicer and Region slicer. Filter on the other hand helped to narrow down data. E.g Product category filter.
## Inference



