# Data-Analysis-3-through-MySQL
Sales Insight Data Analysis Project through MySQL

Pre-requisite:- MySQL Workbench
Download db_dump.sql file to your local computer

Data Analysis Using SQL

1.Show all customer records

SELECT * 
FROM customers;

2.Show total number of customers

SELECT count(*) 
FROM sales.customers;

3.Show transactions for Chennai market (market code for chennai is Mark001

SELECT * 
FROM sales.transactions 
WHERE market_code='Mark001';

4.Show distinct product codes that were sold in chennai

SELECT distinct product_code 
FROM sales.transactions 
WHERE market_code='Mark001';

5.Show transactions where currency is US dollars

SELECT * 
FROM transactions 
WHERE currency="USD"

6.Show transactions in 2020 join by date table

SELECT *
FROM sales.transactions t
JOIN sales.date d
ON t.order_date = d.date
WHERE d.year="2020";

7.Show total revenue in year 2020,

SELECT sum(t.sales_amount)
FROM sales.transactions t
JOIN sales.date d
ON t.order_date = d.date
WHERE d.year="2020";

8.Show total revenue in year 2020 in Chennai

SELECT sum(t.sales_amount)
FROM sales.transactions t
JOIN sales.date d
ON t.order_date = d.date
WHERE d.year="2020" AND t.market_code="Mark001";





