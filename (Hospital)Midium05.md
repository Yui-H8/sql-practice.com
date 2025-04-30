### Medium
Q.05  
* Show the total amount of male patients and the total amount of female patients in the patients table.  
Display the two results in the same row.

---
```SQL
SELECT (
    select COUNT(*)
    FROM patients
    WHERE gender = 'M'
  ) AS male_count, (
    select COUNT(*)
    FROM patients
    WHERE gender = 'F'
  ) AS female_count
;
```
Shorter
```sql
SELECT 
  SUM(Gender = 'M') as male_count, 
  SUM(Gender = 'F') AS female_count
FROM patients
```
