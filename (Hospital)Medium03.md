### Medium
Q.03  
* Show patient_id and first_name from patients where their first_name start and ends with 's' and is at least 6 characters long.

---
```SQL
SELECT
  patient_id,
  first_name
FROM patients
WHERe
  first_name LIKE 's%' AND first_name LIKE '%s'
  AND LEN(first_name) >= 6
;
```
