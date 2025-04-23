#### Hard  
* Q.01 Show the employee's first_name and last_name, a "num_orders" column with a count of the orders taken,
* and a column called "Shipped" that displays "On Time" if the order shipped_date is less or equal to the required_date,
* "Late" if the order shipped late, "Not Shipped" if shipped_date is null.
* Order by employee last_name, then by first_name, and then descending by number of orders.
---
```SQL
SELECT
  first_name,
  last_name,
  COUNT(order_id) AS num_orders,
  CASE
    WHEN shipped_date <= required_date THEN 'On Time'
    WHEN shipped_date > required_date THEN 'Late'
    ELSE 'Not Shipped'
  END AS Shipped
FROM employees e
  JOIN orders o ON e.employee_id = o.employee_id
group by
  last_name,
  first_name,
  Shipped
ORDER BY
  last_name,
  first_name,
  num_orders DESC;
```
