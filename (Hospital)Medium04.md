### Medium
Q.04  
* Show patient_id, first_name, last_name from patients whos diagnosis is 'Dementia'.   
* Primary diagnosis is stored in the admissions table.
---
```SQL
SELECT
  a.patient_id,
  first_name,
  last_name
FROM patients p
  JOIN admissions a ON p.patient_id = a.patient_id
WHERe a.diagnosis = 'Dementia'
;
```
