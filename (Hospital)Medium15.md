### Medium
Q.15  
* Show the difference between the largest weight and smallest weight for patients with the last name 'Maroni'

---
```SQL
SELECT
  max(weight) - min(weight) AS weight_data
FROM patients
WHEre last_name = 'Maroni'
;
```
