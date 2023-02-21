https://school.programmers.co.kr/learn/courses/30/lessons/131124



~~~
SELECT mp.member_name, rr.review_text, DATE_FORMAT(rr.review_date,'%Y-%m-%d') AS review_date
FROM rest_review rr LEFT JOIN member_profile mp ON rr.member_id = mp.member_id,
    (SELECT member_id, COUNT(*) AS cnt
    FROM rest_review
    GROUP BY member_id
    HAVING cnt = (SELECT MAX(cnt) FROM (SELECT count(*) AS cnt FROM rest_review GROUP BY member_id) tb1)
     ) tb2
WHERE tb2.member_id = rr.member_id
ORDER BY review_date, rr.review_text
~~~
