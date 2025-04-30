### Easy  
Q.16 
* Write a query to find list of patients first_name, last_name, and allergies where allergies are not null and are from the city of 'Hamilton'

---
```SQL
SELECT
  first_name,
  last_name,
  allergies
FROM patients
WHERE allergies IS NOT NULL AND city IS 'Hamilton'
;
```
