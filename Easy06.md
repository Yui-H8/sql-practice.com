#### Easy  
* Q.06 Show the first_name, last_name. hire_date of the most recently hired employee.
---
```SQL
SELECT
  first_name,
  last_name,
  MAX(hire_date) AS hire_date
FROM employees;
```
