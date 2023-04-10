# Sales Data Analysis Dashboard

Problem statement:
A company that supplies computer hardware parts to different clients faces difficulty tracking their sales; also, sales are continuously declining for the company because data is not managed, and stakeholders are unable to track the sales as the market is changing dynamically; the problem is getting more complex. 

Data - 
The dataset can be downloaded from [here](https://github.com/codebasics/DataAnalysisProjects/tree/master/1_SalesInsights).
 It consists of six tables.
Product - containing product information. It has 280 rows. The columns available in the table are Product_code and Product_type.

Customers -  contains customers' information. It has 39 rows. The column available in the table is customer_name, customer_code, and customer_type.

Date - contains the exact date of sales; it has 1000 rows. The column available in the table is date, month, and year.

Market - contains the exact date of sales; it has 1000 rows. The columns available in the table are market_code, market_name, and zone.

Transactions - contains the exact date of sales; it has 1,48,395 rows. The columns available in the table are currency, customer_code, market_code, order_date, sales_amount, and sales_quantity.

With the help of SQL workbench, I converted all the given data into CSV so that I could use it on the Powerbi desktop. I imported the given data into the SQL workbench, where I made the dashboard and exported the data in CSV format. As shown in the figure below, in Microsoft Power BI, we will import the data from the feature of Get Data; there, I uploaded all the CSV files




<img src="https://github.com/sumedhakoranga/Sales_Data_Analysis_Dashboard/blob/main/images/Get%20data.png" alt="Get data.png">
Fig 1: To import the data in whatever format it is given


## Model View:
It is a Microsoft Power BI feature. With the help of this feature, I made a star schema, a star schema is a  multidimensional data model used to organize data in a database so that it is easy to understand and analyze. Star schema design is optimized for querying large data sets. Our fact table (transaction) is in the center of the logical diagram; it gives measurable, quantitative data about a business, and the small dimensional tables (customers, date, product, market) branch off to form the points of the star, which contains the related descriptive attributes.


<img src="https://github.com/sumedhakoranga/Sales_Data_Analysis_Dashboard/blob/main/images/model%20view.png" alt="mobile view.png">
Fig 2: We made the star schema considering transactions (Red color box) as the fact table and others in
Blue color as the dimension table.



## Data View:
Data view helps us inspect, explore, and understand data in our Power BI Desktop model.

1- Data view: As shown in Fig 3, select the icon to enter Data view.

2- Data Grid. This area (in Fig 3) shows the selected table and all columns and rows in it. 

3- Fields list. In Fig 3, select a table or column to view the data grid.

We are given the data of Customers, Date, Market, Product, and Transaction. 




<img src="https://github.com/sumedhakoranga/Sales_Data_Analysis_Dashboard/blob/main/images/tran.png" alt="tran.png">
Fig 3: Data Views, Data Grid, and Field list are shown.


## Transform data: 
After analyzing our data, we will finally start making our dashboard. Here, in the tool transform data, we can make changes to the given data.
Transform Data: It is a query editor. Here I changed the sales amount into INR currency since few were given in USD.
Removed sales quantity, whose value was given o or -1
Added conditional column names as num_sales_amount, in which currency was in INR.


<img src="https://github.com/sumedhakoranga/Sales_Data_Analysis_Dashboard/blob/main/images/Transform%20dataa.png" alt="Transform dataa.png">
Fig 4: To make changes in data, go to Home Tab and then select Transform Data

<img src="https://github.com/sumedhakoranga/Sales_Data_Analysis_Dashboard/blob/main/images/editor.png" alt="editor.png">
Fig 5: Changes in the table can be seen in Applied Steps as shown.


## Report View:
In Canvas, I dragged the total sales amount and calculated the total revenue of the company. To make it more understandable, I used the tool card and changed the data value into Million; the same is done with sales quantity.

Revenue by market: Added the data fields of market_ name and total sales amount in the y-axis and x-axis, respectively. To make it more interactive, I made the bar chart.

Sales qty by market: Added the data fields of market_ name and total sales quantity in the y-axis and x-axis, respectively. To make it more interactive, I made the bar chart.


<img src="https://github.com/sumedhakoranga/Sales_Data_Analysis_Dashboard/blob/main/images/report%20view.png" alt="report view.png">
Fig 6: Visualization of our dashboard


## Revenue by top 5  customers: 
We need filters on that particular visual to find the top N or bottom N.


<img src="https://github.com/sumedhakoranga/Sales_Data_Analysis_Dashboard/blob/main/images/topN.png" alt="topN.png">
Fig 7:  Filtering Top N 

 Similarly, we will visualize Revenue by top 5 markets, bottom five products, and top 5 products.


## Revenue Trend: 
To visualize trends, we will drop the data fields of cy_date and total sales amount in the x-axis and y-axis, respectively. Here cy_date is the hierarchical column, which stores the data of year, quarter, month, and day so that when we check the revenue trend, we can drill up or drill down the data according to our requirements.

<img src="https://github.com/sumedhakoranga/Sales_Data_Analysis_Dashboard/blob/main/images/revenue%20trend.png" alt="revenue trend.png">
Fig 8: Our revenue trend for the given data

















## Mobile view: 
I also made the mobile dashboard to check any changes in sales analysis. So that stakeholders can have an idea, even while traveling or at whatever time they want, they can track the sales by clicking on region, date, month, or customer.



<img src="https://github.com/sumedhakoranga/Sales_Data_Analysis_Dashboard/blob/main/images/mobile%20view.png" alt="mobile view.png">
Fig 9: Mobile View of our visualization








