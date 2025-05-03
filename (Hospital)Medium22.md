### Medium
Q.22  
* For every admission, display the patient's full name, their admission diagnosis, and their doctor's full name who diagnosed their problem.

```SQL
SELECT
  CONCAT(p.first_name, ' ', p.last_name) AS patient_name,
  diagnosis,
  CONCAT(d.first_name, ' ', d.last_name) AS doctor_name
FROM patients p
  JOIN admissions a ON p.patient_id = a.patient_id
  JOIN doctors d ON a.attending_doctor_id = d.doctor_id
;
```
