# Sales Insights 

 Objective - I have taken a large data sample of a company name xyz and doing analysis on it to unlock sales Insights that are not visible before for sales team for decision support & automate them to reduced mannual time spent in data gathering.

and creating the dashboard using Tableau that shows the revnue yearly as well as monthly and the quantity of sales and most importantly to find the top 5 products as well as customers. These are the Objectives to make this project. 


Now, to make this project I have taken a large data sample gathered from the company and convert it into MySQL to do analysis on it. and the steps of MySQL is given below.

## Data analysis using MySQL - ##

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`

I have attachted the database file of MySQL.

Then the Tableau part comes here for ETL process and dashboard making.
By ETL process I have cleanned the data and remove the unnecessary things and convert in one unit so that it will be easy to understand. 
after that having all the corrected date I have imported it to make dashboard. For dashboard I have made individual sheet in this I put the data and create the visualized theme and after making all sheets which I needed to make the whole dashboard. 
I simpliy merged all sheets in one dashboard and locate it nicely for analysis and apply fillter to each other so that I can see the results of any Months or years quickly.

I have also attachted the dashboard picture and Tableau file below.

Tableau file atteached is password required file 
 username - root 
 password - AtoZ@786

<img width="1920" height="1080" alt="Project 2 Dashboard" src="https://github.com/user-attachments/assets/5e7ee824-b81f-4cd2-9f10-ac28f48f0973" />


