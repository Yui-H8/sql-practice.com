### Medium
Q.19  
* Show first_name, last_name, and the total number of admissions attended for each doctor.
  
Every admission has been attended by a doctor.

---
```SQL
SELECT
  d.first_name,
  d.last_name,
  COUNT(doctor_id) as admissions_total
FROM admissions a
  JOIN doctors d ON a.attending_doctor_id = d.doctor_id
group by
  doctor_id,
  d.first_name,
  d.last_name
;
```
