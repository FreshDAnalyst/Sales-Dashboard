# Accessories Sales-Dashboard
![](https://github.com/FreshDAnalyst/Sales-Dashboard/blob/main/image_share_1704311652236.jpg)

## Introduction

In this project, you will dive into a large sales dataset to extract valuable insights. It will explore sales trends over time, identify the best-selling products, calculate revenue metrics such as total sales and profit margins, and create visualizations to present findings effectively. This project showcases my ability to manipulate and derive insights from large datasets, enabling me to make data-driven recommendations for optimizing sales strategies.

## Dataset

The dataset was downloaded from Meriskill google drive

## About the dataset

1. The dataset contains a single table in CSV format

2. The table contains columns like Order_id, Product, Quantity_ordered, Price_each, Order_date, Purchase_address, Month, Sales, City and hour

## The purpose of the Analysis

Analyze sales data to identify sales trends, top selling product and revenue metrics for business decision-making

## Tool used: Power BI

## Approach to Analysis

### 1. Extraction, Transformation and Loading (ETL)

· I checked through the dataset to check for errors

· I checked the data dictionary to fully understand the dataset

· I loaded the dataset into power BI

· I then loaded the data in Power Query Editor

### While in Power Query Editor…

I checked and changed the incorrect data types

I used the **SPLIT COLUMN** tool to split the **date** and **time** under the *order_date* column. Now having different column for **date** and **time**


![](https://github.com/FreshDAnalyst/Sales-Dashboard/blob/main/date%20before%20splitting.PNG)
                           *Date & Time Before Splitting*

![](https://github.com/FreshDAnalyst/Sales-Dashboard/blob/main/Date%20%26%20Time%20after%20splitting.PNG)
                           *Date & Time After Splitting*

I used the Order_date column to extract the **“Month Name”, “Day Name”** and **“quarter”** column to help for deeper analysis (drill-down).


![](https://github.com/FreshDAnalyst/Sales-Dashboard/blob/main/Month%20name%2C%20Day%20name%20creation.PNG)


I then click **“Close & Apply”** to exit Power Query Editor and save my Transformation.

## 1. Data Analysis Expression (DAX)

· I created my Measures table by clicking on “Enter Data” on the home ribbon

· I created a new measure **“Revenue”** using: Revenue = SUM (‘Sales Data’[Sales])

· I then created another measure **“Sales Qty”** using: Sales Qty = SUM (‘Sales Data’[Quantity Ordered])

· I created another measure **“Profit Margin”**. But first I need to create the “Total Cost” using: Total cost = SUM (‘Sales Data’[Price Each]). Now to get my “profit Margin” using: Profit Margin = (([Revenue]-[Total Cost])/[Revenue]) * 100


## DASHBOARD: 
I created an interactive and dynamic dashboard to help Meriskill understand business transaction and to drive more sales and work efficiently.


![](https://github.com/FreshDAnalyst/Sales-Dashboard/blob/main/dashboard%201.PNG)

![](https://github.com/FreshDAnalyst/Sales-Dashboard/blob/main/dashboard%202.PNG)


## INSIGHTS

This dashboard contains the KPIs (Revenue, Sales quantity and Profit margin)

· The data shows that the company has made $34,492k revenue and sold over 209k+ products and has a profit margin of 53.83%

· January has the lowest sales and sales is almost the same throughout the year until October, November and December when sales peaked

· San Francisco and Los Angeles have the highest market while sales is at the lowest at Austin and Portland

· Sales peaks on Tuesday and very low during the weekend

· Mac Book pro laptops and iPhone are the products that generate highest revenue

· AA batteries(4-pack) and USB — C Charging Cable are the most sold product

· Sales peak at 10am to 12pm and also 5pm to 8pm


## RECOMMENDATION

· Since January experience the lowest sale, the company should adjust its inventory management strategies for the month. Can also reduce the stock that are in lower demand. The company ca also continue its holiday sales promo to improve sales January sales too

· Since Tuesday is the day with most sales, the company should make marketing promotions for that day to boost the sales

· Given that the 10am to 12pm and also 5pm o 8pm are the peak hours for sales, the company should make more sales staff at those periods to welcome and attend to the numerous number of customers coming to purchase products

· With San francisco being the state with highest sales and revenue, the company should adopt the same marketing strategy on other states with low sales and revenue to also boost their sales

· Since Mac Book Pro laptops and Iphones are the top-performing product, the company should continue to prioritize and promote these products.

**Thank you for reading**
