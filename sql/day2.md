Query 1: Find the first two highest salary employee in each dept
select name,rn
from
(
  select name,row_number() over(partition by dept order by salary desc) as rn from empn 
) as ranked_emp
where rn in (1,2);
O/p: https://github.com/pmadhuri186/DE-Journey-2026/blob/main/sql/screenshots/Day02_query1_output.jpg
Query 2: 
