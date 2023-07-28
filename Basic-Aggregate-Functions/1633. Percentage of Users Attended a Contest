with tt as (
    select count(*) as totalusers
    from users
)



select contest_id, round((count(user_id)/totalusers)*100,2) as percentage   
 

from tt u join register r

group by contest_id
order by percentage desc, contest_id
