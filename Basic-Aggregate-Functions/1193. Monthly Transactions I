select 
    date_format(trans_date, '%Y-%m') as month, 
    country, 
    count(trans_date) as trans_count,
    sum(case when state = "approved" then 1 else 0 end) as approved_count,
    sum(amount) as trans_total_amount,
    sum(if(state="approved",amount,0)) as approved_total_amount

from transactions 



group by 1,2