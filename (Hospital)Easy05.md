### Easy  
Q.05  
* Update the patients table for the allergies column. If the patient's allergies is null then replace it with 'NKA'

---
```SQL
UPDATE patients
SET allergies = 'NKA'
WHERE allergies IS NULL
;
```
