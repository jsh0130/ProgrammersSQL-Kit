https://school.programmers.co.kr/learn/courses/30/lessons/131118


~~~
SELECT ri.rest_id, rest_name, food_type, favorites, address, ROUND(AVG(review_score),2) AS score
FROM rest_info AS ri
JOIN rest_review rv ON ri.rest_id = rv.rest_id
WHERE LEFT(address, 2) = '서울'
GROUP BY rest_id
ORDER BY score DESC, favorites DESC
~~~
