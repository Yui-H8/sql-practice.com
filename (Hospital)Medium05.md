### Medium
Q.05  
* Display every patient's first_name.  
Order the list by the length of each name and then by alphabetically.
---
```SQL
SELECT first_name
FROM patients
ORDER BY
  LEN(first_name),
  first_name
;
```
