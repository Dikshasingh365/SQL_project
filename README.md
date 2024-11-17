# SQL_project
-- QUestion- 1 What is the total amount each customer spent at the restaurant? --

select sum(m.price) as total_amount,s.customer_id
from dannys_diner.sales s 
INNER JOIN dannys_diner.menu m ON s.product_id=m.product_id
group by s.customer_id
order by total_amount desc;
