### Hard
Q.02  
* Show patient_id, weight, height, isObese from the patients table.  
Display isObese as a boolean 0 or 1.  
Obese is defined as weight(kg)/(height(m)2) >= 30.  
weight is in units kg.  
height is in units cm.  

---
```SQL
SELECT patient_id, weight, height, 
  (CASE 
      WHEN weight/(POWER(height/100.0,2)) >= 30 THEN
          1
      ELSE
          0
      END) AS isObese
FROM patients;
-- If you divide an int by an int you will get an int. Dividing an int by a float will return a float.
-- That's why you have to divide by 100.0 and not 100.
-- Use CAST(variable_name AS FLOAT) function if you are dividing by two variables.
;
```
Answer 2
```SQL
SELECT
  patient_id,
  weight,
  height,
  weight / power(CAST(height AS float) / 100, 2) >= 30 AS obese
FROM patients
;
```
