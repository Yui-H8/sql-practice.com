### Medium
Q.17  
* Show all columns for patient_id 542's most recent admission_date.

---
```SQL
SELECT *
FROM admissions
WHERE patient_id = 542
order by admission_date DESC
LIMIT 1
;
```
