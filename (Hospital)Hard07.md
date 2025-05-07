### Hard
Q.07  
* We are looking for a specific patient. Pull all columns for the patient who matches the following criteria:  
- First_name contains an 'r' after the first two letters.
- Identifies their gender as 'F'
- Born in February, May, or December
- Their weight would be between 60kg and 80kg
- Their patient_id is an odd number
- They are from the city 'Kingston'

---
```SQL
SELECT *
FROM patients
WHERE
  gender = 'F'
  and first_name like ('__r%')
  and (weight between 60 and 80)
  and month(birth_date) IN (2, 3, 12)
  and patient_id % 2 = 1
  and city ='Kingston'
;
```
