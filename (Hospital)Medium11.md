### Medium
Q.11  
* Show all allergies ordered by popularity. Remove NULL values from query.
  
---
```SQL
SELECT
  allergies,
  COUNT(allergies) AS total_diagnosis
FROM patients
WHERE allergies IS NOT NULL
GROUP BY allergies
order by total_diagnosis DESC
;
```
