#### Medium  
* Q.03 Show the city, company_name, contact_name from the customers and suppliers table merged together.  
* Create a column which contains 'customers' or 'suppliers' depending on the table it came from.
---
```SQL
select
  City,
  company_name,
  contact_name,
  'customers' as relationship
from customers
union
select
  city,
  company_name,
  contact_name,
  'suppliers'
from suppliers;
```
