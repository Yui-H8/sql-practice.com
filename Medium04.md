#### Medium  
* Q.04 Show the total amount of orders for each year/month.
---
```SQL
SELECT
  YEAR(order_date) AS order_year,
  MONTH(order_date) AS order_month,
  COUNT(order_id) AS no_of_orders
FROM orders
GROUP BY
  YEAR(order_date),
  MONTH(order_date);
```
