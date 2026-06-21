Query 1: Find the first two highest salary employee in each dept
select name,rn
from
(
  select name,row_number() over(partition by dept order by salary desc) as rn from empn 
) as ranked_emp
where rn in (1,2);
O/p: 
Query 2: 
