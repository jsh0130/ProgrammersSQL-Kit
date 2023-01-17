https://school.programmers.co.kr/learn/courses/30/lessons/59044


~~~
SELECT ai.name, ai.datetime
FROM animal_ins AS ai
LEFT JOIN animal_outs ao ON ai.animal_id = ao.animal_id
WHERE ao.animal_id IS NULL
ORDER BY datetime
LIMIT 3
~~~
