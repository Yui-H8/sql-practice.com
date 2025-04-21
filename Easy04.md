#### Easy  
* Q.04 Show the city, company_name, contact_name of all customers from cities which contains the letter 'L' in the city name, sorted by contact_name
---
```SQL
SELECT
  city,
  company_name,
  contact_name
FROM customers
WHERE
  city LIKE 'L%'
  OR city LIKE '%L%'
  OR city LIKE '%L'
ORDER BY contact_name;
```
