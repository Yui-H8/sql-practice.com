### Medium
Q.25  
* Show patient_id, first_name, last_name from patients whose does not have any records in the admissions table.   
(Their patient_id does not exist in any admissions.patient_id rows.)
---
```SQL
SELECT
  p.patient_id,
  p.first_name,
  p.last_name
FROM patients p
WHERE NOT exists(
    SELECT *
    FROM admissions a
    WHERE p.patient_id = a.patient_id
  )
;
```
