### Easy  
Q.13  
* Show the patient id and the total number of admissions for patient_id 579.

---
```SQL
SELECT
  patient_id,
  count(*) AS total_admissions
FROM admissions
WHERE patient_id = '579'
;
```
