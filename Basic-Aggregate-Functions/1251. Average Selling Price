select p.product_id, round(sum(units*price)/sum(units),2) as average_price


from prices p
join unitssold u 
    on p.product_id = u.product_id
    and purchase_date between start_date and end_date

group by u.product_id