https://school.programmers.co.kr/learn/courses/30/lessons/157340



~~~
SELECT car_id,
        if(sum(if('2022-10-16' between start_date and end_date, 1, 0))>0, '대여중', '대여 가능') as availability
from car_rental_company_rental_history
group by car_id
order by car_id desc
~~~
