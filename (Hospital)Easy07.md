### Easy  
Q.07  
* Show first name, last name, and the full province name of each patient.   
Example: 'Ontario' instead of 'ON'

---
```SQL
SELECT
  first_name,
  last_name,
  n.province_name
FROM patients p
  JOIN province_names n ON p.province_id = n.province_id
;
```
