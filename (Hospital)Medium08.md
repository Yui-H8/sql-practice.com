### Medium
Q.08  
* Show patient_id, diagnosis from admissions. Find patients admitted multiple times for the same diagnosis.

---
```SQL
SELECT
  patient_id,
  diagnosis
FROM admissions
group by patient_id, diagnosis
HAVING COUNT(diagnosis) > 1
;
```
