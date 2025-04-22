#### Medium  
* Q.02 Show the category_name and the average product unit price for each category rounded to 2 decimal places.
---
```SQL
SELECT
  category_name,
  ROUND(AVG(unit_price), 2) as average_unit_price
FROM categories c
  JOIN products p ON c.category_id = p.category_id
GROUP BY category_name;
```
