# Customer Transaction Dashboard
![Model]([Paste_link_here](https://github.com/Ahsan-Bilal-1899/customer-transaction-dashbaord/blob/7bcb6b1e9f211a3554acaef34f5529fa33cbf958/Dashboard%20Capture.png
))

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
*DATEPART()* function in Tableau allows extracting the hour from a record.

## Dashboard Elements

The dashboard was designed in Tableau, which is popular in the analytics and business intelligence sphere. The dashboard is designed to fit in a typical browser screen for a PC or Laptop. It comprises of several visuals and other components such as filters and search bar for interactivity purposes.

### KPI Card 1 - Total Dollar Amount of Transactions

The total sum paid by all customers in their transactions was close to 200,000 US dollars.

### KPI Card 2 - Total Transactions Made

The sum of the transaction amount was distributed over 510 transactions made by each different customer.

### KPI Card 3 - Median Amount of Transactions

The final KPI card shows the median value for the amount paid by customers. The distribution of the amount varies a lot from one customer to another. Hence, the median is a better measure of central tendency in this case.

### Stacked Bar Chart - Customers grouped by Payment Type and Source

### Bar Chart - Product Type grouped by Average Transaction Amount

The bar graph below compares the average transaction amount for the two different types of product - a physical book or its online format. 

### Line Chart - Count of transactions by Hour of Day

The line chart shows how the number of transactions varied throughout the course of a day. 

### Filter 1 - Filter by Region

The first filter of the dashboard was implemented on all of the worksheets/visuals shown above. It is a dropdown menu that allows end users to get isolated views of the metrics based on the region where the customers live *(North, South, East and West)*. Since the dropdown menu allows multiple selection, users can also filter by multiple regions at the same time.

### Filter 2 - Filter by Customer ID

The second filter of the dashboard allows end users to get a more detailed and specific look on each individual customer. This filter is also a dropdown menu but only allows single selection to preserve dashboard layout and spacing. Once a customer ID is selected, a table appears showing the customer’s payment type, product and the amount they paid in the transaction. 
