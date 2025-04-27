### Easy  
Q.10  
* Show all columns for patients who have one of the following patient_ids:   
1,45,534,879,1000

---
```SQL
SELECT *
FROM patients
WHERE
  patient_id IN ('1', '45', '534', '879', '1000')
;
```
