### Hard
Q.09  
* For each day display the total amount of admissions on that day. Display the amount changed from the previous date.

---
```SQL
select
  admission_date,
  COUNT(admission_date) as admission_day,
  (COUNT(admission_date)) - (
      LAG(COUNT(admission_date)) OVER (
        ORDER BY
          admission_date
      )) AS admission_count_change
    FROM admissions
    GROUP BY admission_date
;
```
