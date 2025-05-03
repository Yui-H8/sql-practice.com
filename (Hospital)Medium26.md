### Medium
Q.26  
* Display a single row with max_visits, min_visits, average_visits where the maximum, minimum and average number of admissions per day is calculated. Average is rounded to 2 decimal places.

---
```SQL
SELECT
  MAX(patient_count) as max_visits,
  MIN(patient_count) as min_visits,
  ROUND(avg(patient_count), 2) as average_visits
FROM (
    SELECT
      COUNT(patient_id) as patient_count
    FROM admissions
    group by admission_date
  )
;
```
