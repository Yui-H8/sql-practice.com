#### Hard  
* Q.02 Show how much money the company lost due to giving discounts each year, 
* order the years from most recent to least recent. Round to 2 decimal places
```SQL
SELECT
  YEAR(order_date) AS 'order_year',
  ROUND(
    (SUM((unit_price * quantity) * discount)),2) AS 'discount_amount'
FROM order_details od
  JOIN orders o ON od.order_id = o.order_id
  JOIN products p ON od.product_id = p.product_id
GROUP BY YEAR(order_date)
ORDER BY YEAR(order_date) DESC;
```
