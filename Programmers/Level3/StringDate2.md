https://school.programmers.co.kr/learn/courses/30/lessons/59411



~~~
SELECT ao.animal_id, ao.name
FROM animal_outs AS ao
LEFT JOIN animal_ins ai ON ao.animal_id = ai.animal_id
WHERE ai.datetime IS NOT NULL
ORDER BY DATEDIFF(ai.datetime,ao.datetime)
LIMIT 2
~~~
