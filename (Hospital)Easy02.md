### Easy  
* Q.02 Show first name and last name of patients who does not have allergies. (null)

---
```SQL
SELECT
  first_name,
  last_name
FROM patients
WHERE allergies IS NULL;
;
```
