### Easy  
Q.14  
* Based on the cities that our patients live in, show unique cities that are in province_id 'NS'.

---
```SQL
SELECT DISTINCT city
FROM patients
WHERE province_id = 'NS'
;
```
