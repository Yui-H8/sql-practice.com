### Medium
Q.23  
* display the first name, last name and number of duplicate patients based on their first name and last name.
   
Ex: A patient with an identical name can be considered a duplicate.

---
```SQL
SELECT
  first_name,
  last_name,
  COUNT(patient_id) AS num_of_duplicate
FROM patients
group by
  first_name,
  last_name
HAVING num_of_duplicate > 1
;
```
