https://school.programmers.co.kr/learn/courses/30/lessons/59413



~~~
WITH RECURSIVE time AS (
    SELECT 0 AS hour
    UNION ALL
    SELECT hour+1 FROM time WHERE hour<23
)
SELECT t.hour AS hour, count(a.animal_id>0) AS count
FROM time AS t
LEFT JOIN (
            SELECT *, HOUR(datetime) AS hour
            FROM animal_outs
) a
            ON t.hour = a.hour
GROUP BY t.hour
ORDER BY t.hour
~~~

NEW - WITH과 RECURSIVE의 활용
