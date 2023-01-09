https://school.programmers.co.kr/learn/courses/30/lessons/144854


~~~
SELECT b.book_id, a.author_name, DATE_FORMAT(published_date,'%Y-%m-%d') AS published_date
FROM book AS b
LEFT JOIN author a ON b.author_id = a.author_id
WHERE b.category = '경제'
ORDER BY published_date
~~~
