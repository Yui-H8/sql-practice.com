### Hard
Q.10  
* Sort the province names in ascending order in such a way that the province 'Ontario' is always on top.

---
```SQL
select province_name
from province_names
order by
  province_name = 'Ontario' desc,
  province_name
;
```
Answer2
```sql
select province_name
from province_names
order by
  (not province_name = 'Ontario'),
  province_name
;
```
Answer3
```sql
select province_name
from province_names
order by
  (case when province_name = 'Ontario' then 0 else 1 end),
  province_name
;
```
