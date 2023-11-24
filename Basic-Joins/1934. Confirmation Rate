with combo as (
    select user_id,
    sum(case when action = "confirmed" then 1 else 0 end) as totalconfirmed, 
    count(action) as totalaction 

    from confirmations
    group by user_id 
) 

select 
    s.user_id,
    round(ifnull(sum(totalconfirmed/totalaction),0),2) as confirmation_rate

    from signups s
    left join combo c
    on s.user_id = c.user_id 
    group by 1     
      
