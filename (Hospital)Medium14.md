### Medium
Q.14  
* Show the province_id(s), sum of height; where the total sum of its patient's height is greater than or equal to 7,000.
---
```SQL
SELECT
  province_id,
  sum(height) AS sum_height
FROM patients
group by province_id
having sum_height >= 7000
;
```
