### Hard
Q.01  
* Show first name, last name, and gender of patients whose gender is 'M'

---
```SQL
SELECT
  first_name,
  last_name,
  gender
FROM patients
WHERE gender = "M"
;
```
