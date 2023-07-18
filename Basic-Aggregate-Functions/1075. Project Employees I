select project_id, round(sum(experience_years)/count(experience_years), 2) as average_years

from project p left join employee e on p.employee_id = e.employee_id

group by project_id
order by project_id
