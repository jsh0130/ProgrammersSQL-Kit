https://school.programmers.co.kr/learn/courses/30/lessons/144856



~~~
SELECT b.author_id, a.author_name, b.category, SUM(b.price * bs.sales) AS total_sales
FROM book AS b
LEFT JOIN author a ON b.author_id = a.author_id
LEFT JOIN book_sales bs ON b.book_id = bs.book_id
WHERE YEAR(bs.sales_date) = '2022' AND MONTH(bs.sales_date) = '1'
GROUP BY author_name, category
ORDER BY author_id, category DESC
~~~
