https://school.programmers.co.kr/learn/courses/30/lessons/59409


~~~
SELECT animal_id, name, IF(sex_upon_intake REGEXP 'Neutered|Spayed','O','X') AS 중성화
FROM animal_ins
ORDER BY animal_id
~~~
