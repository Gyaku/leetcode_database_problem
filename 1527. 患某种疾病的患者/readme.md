Source : https://leetcode.com/problems/second-highest-salary/<br>
Author : gyaku<br>
Time   : 2023-3-26<br>

##解题思路一
###模糊查询

##sql
select patient_id, patient_name, conditions
from Patients
where conditions like 'DIAB1%' or conditions like '% DIAB1%'


##解题思路二
###正则表达式
REGEXP
SELECT * FROM PATIENTS
WHERE CONDITIONS REGEXP '^DIAB1|\\sDIAB1'

