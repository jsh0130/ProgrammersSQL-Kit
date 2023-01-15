https://school.programmers.co.kr/learn/courses/30/lessons/151139



~~~
SELECT b.category, SUM(bs.sales) AS total_sales
FROM book AS b
JOIN book_sales AS bs ON b.book_id = bs.book_id
WHERE sales_date LIKE '2022-01%'
GROUP BY b.category
ORDER BY b.category
~~~
