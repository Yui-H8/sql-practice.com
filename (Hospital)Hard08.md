### Hard
Q.08  
* Show the percent of patients that have 'M' as their gender. Round the answer to the nearest hundreth number and in percent form.

---
```SQL
SELECT
  round(100 * avg(gender = 'M'), 2) || '%' AS percent_of_male_patients
FROM
  patients
;
```
Answer2
```SQL
SELECT 
   CONCAT(ROUND(SUM(gender='M') / CAST(COUNT(*) AS float), 4) * 100, '%')
FROM patients;
```
