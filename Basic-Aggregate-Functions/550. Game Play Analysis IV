with cte as( 
  select player_id, min(event_date) as first_login 
  from activity 
  group by player_id
)

SELECT ROUND(COUNT(t2.player_id)/COUNT(t1.player_id),2) AS fraction
FROM cte t1 
LEFT JOIN Activity t2
ON t1.player_id = t2.player_id AND t1.first_login = t2.event_date - 1   
 
