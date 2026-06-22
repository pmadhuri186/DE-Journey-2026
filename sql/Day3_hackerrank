--Problem: Binary tree nodes
--Source: HackerRank
--Concepts: Case when, subquery

select n,case when p is null then 'Root' when n in (select distinct p from bst) and p is not null then 'Inner' else 'Leaf'
end as typ
from bst
order by n;

--Problem: New Companies
--Source: HackerRank
--Concepts: Joins, group by
select c.company_code,founder,count(distinct lm.lead_manager_code),count(distinct sm.senior_manager_code),count(distinct m.manager_code),count(distinct e.employee_code) from company c
join lead_manager lm on lm.company_code=c.company_code
join senior_manager sm on sm.company_code=c.company_code
join manager m on m.company_code=c.company_code
join employee e on e.company_code=c.company_code
group by c.company_code,founder
order by c.company_code;
