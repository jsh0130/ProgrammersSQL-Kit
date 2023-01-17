https://school.programmers.co.kr/learn/courses/30/lessons/59042



~~~
SELECT ao.animal_id, ao.name
FROM animal_ins AS ai
RIGHT JOIN animal_outs ao ON ai.animal_id = ao.animal_id
WHERE ai.animal_id IS NULL
ORDER BY animal_id
~~~
