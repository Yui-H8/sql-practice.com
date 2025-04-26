### Easy  
Q.03
* Show first name of patients that start with the letter 'C'

---
```SQL
SELECT first_name
FROM patients
WHERE first_name LIKE "C%"
;
```
