### Hard
Q.01  
* Show all of the patients grouped into weight groups.  
Show the total amount of patients in each weight group.  
Order the list by the weight group decending.  
  
For example, if they weight 100 to 109 they are placed in the 100 weight group, 110-119 = 110 weight group, etc.

---
```SQL
SELECT
  COUNT(patient_id) as patients_in_group,
  weight_group * 10
FROM(
    SELECT
      ROUND(weight / 10, 0) AS weight_group,
      patient_id
    FROM patients
  )
GROUP BY weight_group
ORDER BY weight_group DESC
;
```
