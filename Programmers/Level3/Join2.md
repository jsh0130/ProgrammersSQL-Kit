https://school.programmers.co.kr/learn/courses/30/lessons/59043



~~~
SELECT ai.animal_id, ai.name
FROM animal_ins AS ai
JOIN animal_outs ao ON ai.animal_id = ao.animal_id
WHERE ai.datetime > ao.datetime
ORDER BY ai.datetime
~~~
