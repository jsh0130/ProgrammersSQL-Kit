https://school.programmers.co.kr/learn/courses/30/lessons/131123


~~~
SELECT food_type, rest_id, rest_name, favorites
FROM (
    SELECT food_type, rest_id, rest_name, favorites, RANK() OVER (PARTITION BY food_type ORDER BY favorites DESC) AS r
    FROM rest_info
    ) AS a
WHERE r = 1
ORDER BY food_type DESC


/*
SELECT food_type, rest_id, rest_name, favorites
FROM (SELECT *
      FROM rest_info
      ORDER BY favorites DESC
      limit 99999 #limit을 걸어야만 결과가 나오는 이유?
     ) A
GROUP BY food_type
ORDER BY food_type DESC
*/
~~~
