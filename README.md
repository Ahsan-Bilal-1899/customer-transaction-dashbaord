# Customer Transaction Dashboard
![Model]([Paste_link_here](https://github.com/Ahsan-Bilal-1899/customer-transaction-dashbaord/blob/7bcb6b1e9f211a3554acaef34f5529fa33cbf958/Dashboard%20Capture.png
))

## Dashboard Preview

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b6000e67-04d0-4af9-b190-245446b216c4/6ed1623b-dbab-425e-9806-a8847ef1a031/image.png)

## About the Dataset

The dataset is in the form of an Excel spreadsheet and it contains records about transactions made by 510 distinct customers to fulfill payment. The data dictionary below shows the column names, descriptions and associated datatype.

| Column Name | Column Description | Data Type |
| --- | --- | --- |
| Cust ID | Short for customer ID, acts as a unique identifier number for each customer. | String |
| Region | Region where customer lives. | String |
| Payment | Payment made via Credit or PayPal | String |
| Source | Source by which customer paid, either Email or Web. | String |
| Amount | The dollar amount paid for each transaction. | Number (decimal) |
| Product | Form of the product, either online or a physical book. | String |
| Time of Day | Time at which the transaction occurred, 24 hour clock (hh: mm).    | Datetime |
| ** Hour  | Hour at which the transaction occurred (0-22). | Datetime |

** Hour is a calculated field that was not present in the original dataset.

![*DATEPART()* function in Tableau allows extracting the hour from a record.](https://prod-files-secure.s3.us-west-2.amazonaws.com/b6000e67-04d0-4af9-b190-245446b216c4/d98cc3b9-7169-45d2-9640-e4fcc531c327/image.png)

*DATEPART()* function in Tableau allows extracting the hour from a record.

## Dashboard Elements

The dashboard was designed in Tableau, which is popular in the analytics and business intelligence sphere. The dashboard is designed to fit in a typical browser screen for a PC or Laptop. It comprises of several visuals and other components such as filters and search bar for interactivity purposes.

### KPI Card 1 - Total Dollar Amount of Transactions

The total sum paid by all customers in their transactions was close to 200,000 US dollars.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b6000e67-04d0-4af9-b190-245446b216c4/9ce9fa8a-003e-456b-b8d4-0907cf2cdbd3/image.png)

### KPI Card 2 - Total Transactions Made

The sum of the transaction amount was distributed over 510 transactions made by each different customer.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b6000e67-04d0-4af9-b190-245446b216c4/5f1dccb1-e0b1-44dd-bcfa-5d45a768b6c3/image.png)

### KPI Card 3 - Median Amount of Transactions

The final KPI card shows the median value for the amount paid by customers. The distribution of the amount varies a lot from one customer to another. Hence, the median is a better measure of central tendency in this case.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b6000e67-04d0-4af9-b190-245446b216c4/6ec84f7c-fe6d-4e89-b658-178495287e14/image.png)

### Stacked Bar Chart - Customers grouped by Payment Type and Source

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b6000e67-04d0-4af9-b190-245446b216c4/a8654480-936e-4120-87c0-fcf0f1c29bcf/image.png)

### Bar Chart - Product Type grouped by Average Transaction Amount

The bar graph below compares the average transaction amount for the two different types of product - a physical book or its online format. 

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b6000e67-04d0-4af9-b190-245446b216c4/4474575e-b774-4983-a63c-6188a336f711/image.png)

### Line Chart - Count of transactions by Hour of Day

The line chart shows how the number of transactions varied throughout the course of a day. 

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b6000e67-04d0-4af9-b190-245446b216c4/2cf68019-761d-4be5-89fd-4f2da3731d48/image.png)

### Filter 1 - Filter by Region

The first filter of the dashboard was implemented on all of the worksheets/visuals shown above. It is a dropdown menu that allows end users to get isolated views of the metrics based on the region where the customers live *(North, South, East and West)*. Since the dropdown menu allows multiple selection, users can also filter by multiple regions at the same time.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b6000e67-04d0-4af9-b190-245446b216c4/13fb049e-719b-45d0-966c-636efda5cf44/image.png)

### Filter 2 - Filter by Customer ID

The second filter of the dashboard allows end users to get a more detailed and specific look on each individual customer. This filter is also a dropdown menu but only allows single selection to preserve dashboard layout and spacing. Once a customer ID is selected, a table appears showing the customer’s payment type, product and the amount they paid in the transaction. 

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/b6000e67-04d0-4af9-b190-245446b216c4/d0361be0-12bc-44d3-b600-4eeb16833ae0/image.png)
