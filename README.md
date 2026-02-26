# Sql-project
create database Payment;
use payment;
create table Payment (
customer_id int primary key,
 customer varchar(50),
 mode varchar(50),
 city varchar(50)
 );
insert into payment 
value
(101, 'olivia', 'Netbanking', 'Portland');
insert into payment 
value
(102, 'olivia', 'Netbanking', 'Portland');
insert into payment 
value
(103, 'Denial', 'Marketing', 'london');
insert into payment (customer_id, customer, mode, city)
value 
(104, 'Maya', 'Credit card', 'Denver'),
(105, 'Liam', 'Networking','New Orleans'),
(106, 'sophia', 'Credit card', 'Minneapolis'),
(107, 'Caleb', 'Networking', 'Boston'),
(108, 'Ava patel', 'Credit card', 'Boston'),
(109, 'Lucas Carter', 'Networking', 'Miami'),
(110, 'Jackson Brooks', 'Networking', 'Miami');
select * from Payment;
select mode, count(customer_id)
from payment
group by mode
order by mode;
select customer_id
from payment
where mode ='networking';
update payment 
set mode = 'netbanking'
where customer_id in (105, 107, 109,110);
select * from Payment;
select customer_id
from payment
where mode = 'marketing';
update payment
set mode = 'debit card'
where customer_id in (103);
select * from Payment;
select mode, count(city)
from payment
group by mode
order by mode asc;
select mode, count(city)
from payment
group by mode
Having count(city) > 2
order by mode asc;
select * from Payment;




