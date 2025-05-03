### Medium
Q.20  
* For each doctor, display their id, full name, and the first and last admission date they attended.

---
```SQL
SELECT
  d.doctor_id,
  CONCAT(d.first_name, ' ', d.last_name) AS full_name,
  MIN(admission_date) AS first_admission_date,
  MAX(admission_date) AS last_admission_date
FROM admissions a
  JOIN doctors d ON a.attending_doctor_id = d.doctor_id
group by
  doctor_id,
  full_name
;
```
