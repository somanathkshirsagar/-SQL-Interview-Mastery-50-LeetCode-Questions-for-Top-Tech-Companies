with cte as(
    select 
    distinct(customer_id),
    FIRST_VALUE(order_date=customer_pref_delivery_date) over(partition by customer_id order by order_date) ii
    from delivery
)

select round(avg(ii)*100,2) immediate_percentage
from cte

