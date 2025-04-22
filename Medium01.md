#### Medium  
* Q.01 Show the ProductName, CompanyName, CategoryName from the products, suppliers, and categories table
---
```SQL
SELECT
  product_name,
  company_name,
  category_name
FROM categories c
  JOIN products p ON c.category_id = p.category_id
  JOIN suppliers s ON p.supplier_id = s.supplier_id;
```
