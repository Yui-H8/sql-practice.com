### Medium
Q.21  
* Display the total amount of patients for each province. Order by descending.
  
---
```SQL
SELECT
  province_name,
  COUNT(patient_id) as patient_count
FROM patients p
  JOIN province_names n ON p.province_id = n.province_id
GROUP BY province_name
ORDER BY patient_count DESC
;
```
