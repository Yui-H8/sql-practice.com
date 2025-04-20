#### Easy  
* Q.03 Show all the even numbered Order_id from the orders table
---
```SQL
SELECT order_id
FROM orders
WHERE order_id % 2 = 0;
```
