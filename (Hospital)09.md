### Easy  
Q.09  
* Show the first_name, last_name, and height of the patient with the greatest height.

---
```SQL
SELECT
  first_name,
  last_name,
  MAX(height)
FROM patients
;
```
*May not be supported in every sql language.*

More correct answer:
```SQL
SELECT
  first_name,
  last_name,
  height
FROM patients
WHERE height = (
    SELECT max(height)
    FROM patients
  )
;
```
