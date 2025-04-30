### Medium
Q.01  
* Show first name, last name, and gender of patients whose gender is 'M'

---
```SQL
SELECT DISTINCT YEAR(birth_date) AS birth_Year
FROM patients
ORDER BY YEAR(birth_date)
;
```
