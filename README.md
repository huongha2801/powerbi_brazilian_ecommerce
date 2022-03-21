# Brazilian Ecommerce Dashboard with Power BI
### The dataset was collected from Kaggle at: https://www.kaggle.com/olistbr/brazilian-ecommerce
## Preparation
### Brief introduction
I only downloaded relevant tables, which are the *customer*, *order*, *order items*, *product* and *category name* tables <br/>
The customer table contains customers' id and information about the customer's state and city <br/>
The order table contains order ids and various timestamps regarding order's processing (purchased, approved, delivered). This table is linked to the customer table with customer_id <br/>
The order_item contain item ids, price, product information and name of the seller <br/>
The remaining 2 tables give more details about the items' specification. <br/>
### Data transformation
After joining the above tables, I created new measures and used Power Query to add new columns according to ad hoc needs during the process <br/>
New measures include: No. of orders, No. of late orders (and percentage), average shipping time, ... <br/>
To calculate the number of late orders, I used actual deliver date and estimated time of delivery to determine which order is late <br/>
For average shipping time, the difference between actual deliver date and purchased date was calculated using DATEDIFF function <br/>
Further more, throughout the process, there was much need for the date and time columns to be transformed into formats suitable for PowerBI presentation, hence I did make much use of the Editor.

## How to use it?
The slicers allow the end-user to choose their state and city of interest, as well as the period to focus on. <br/>
For the <strong>Orders and Late orders</strong> timeseries, the reader can also drill down to such levels as days and weeks.

## What insights can be drawn?
From the most comprehensive level, it can be seen that: <br/>
* Top 5 states with the highest number of orders: Sao Paulo, Rio de Janeiro, Minas Gerais, Rio Grande do Sul & Paraná
* The capacity to deliver orders quickly improved since Janulary 2017 the period after which saw the total number of orders soaring while that of late orders remain low.
* During the two-year period, there were as many as 7000 orders delivered late Brazil-wide, this calls for better operation from the Supply side.
* Most orders (note, to be differentiated with app use, where shoppers browse for products) took place between 10 a.m and 23 p.m.

Making use of the slicers, the reader can gain more insights into the pattern of e-commerce inside each state/city in particular. <br/>
  



