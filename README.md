# Brazilian Ecommerce Dashboard with Power BI
### The dataset was collected from Kaggle at: https://www.kaggle.com/olistbr/brazilian-ecommerce
## Preparation
### Brief introduction
I only downloaded relevant tables, which are the customer, order, order items, product and category name tables <br/>
The customer table contains customers'id and information about the customer's state and city <br/>
The order table contains order ids and various timestamps regarding order's processing (purchased, approved, delivered). This table is linked to the customer table with customer_id <br/>
The order_item contain item ids, price, product information and name of the seller <br/>
The remaining 2 tables give more details about the items' specification. <br/>
### Data transformation
After joining the above tables, I created new measures and used Power Query to add new columns according to ad hoc needs during the process <br/>
New measures include: No. of orders, No. of late orders (and percentage), average shipping time, ... <br/>
To calculate the number of late orders, I used actual deliver date and estimated to determine which order is late <br/>
For average shipping time, the difference between actual deliver date and purchased date was calculated using DATEDIFF function


