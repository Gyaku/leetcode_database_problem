Source : https://leetcode.com/problems/group-sold-products-by-the-date/<br>
Author : gyaku<br>
Time   : 2023-3-26<br>

##解题思路
## 考察的是SQL中相关字符串函数

###GROUP_CONCAT() 函数

group_concat([DISTINCT] 要连接的字段 [Order BY ASC/DESC 排序字段] [Separator '分隔符'])

Separator 缺省','

##sql
select sell_date,<br>
count(distinct product) as num_sold, <br>
group_concat(distinct product <br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; order by product <br>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; separator ',' ) as products<br>
from Activities <br>
group by sell_date<br>
order by sell_date<br>

###ps
_GROUP(str1,str2,…)_ 

可以将多个字符串拼接在一起

_GROUP_WS(separator,str1,str2,…)_ 

代表 CONCAT With Separator ，是 _CONCAT()_ 的特殊形式。
第一个参数是其它参数的分隔符。分隔符的位置放在要连接的两个字符串之间