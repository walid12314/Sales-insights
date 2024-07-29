# Sales-insights


**Data Analysis Using SQL**


1. Show all customer records

SELECT 
    *
FROM
    customers;

2. Show total number of customers

SELECT 
    count(*)
FROM
    customers;

3. Show transactions for Chennai market (market code for chennai is Mark001

SELECT 
    *
FROM
    sales.transactions
WHERE
    market_code = 'Mark001';

4. Show distrinct product codes that were sold in chennai

SELECT 
    distinct(product_code)
FROM
    transactions
WHERE
    market_code = 'Mark001';

5. Show transactions where currency is US dollars
   SELECT 
    *
FROM
    transactions
WHERE
    currency = 'USD';

6.Show transactions in 2020 join by date table

SELECT 
    *
FROM
    transactions
        INNER JOIN
    date ON transactions.order_date = date.date
WHERE
    year = '2020';

7. Show total revenue in year 2020,

SELECT 
    SUM(transactions.sales_amount)
FROM
    transactions
        INNER JOIN
    date ON transactions.order_date = date.date
WHERE
    year = '2020';

8.Show total revenue in year 2020, January Month,

SELECT 
    SUM(transactions.sales_amount)
FROM
    transactions
        INNER JOIN
    date ON transactions.order_date = date.date
WHERE
    year = '2020' AND month_name = 'January'
        AND currency = 'INR ;
9. Show total revenue in year 2020 in Chennai

SELECT 
    SUM(transactions.sales_amount)
FROM
    transactions
        INNER JOIN
    date ON transactions.order_date = date.date
WHERE
    year = '2020' AND market_code = 'Mark001'
        
;




    
