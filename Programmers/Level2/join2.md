https://school.programmers.co.kr/learn/courses/30/lessons/131533


~~~
SELECT product_code, SUM(price * sales_amount) AS sales
FROM product AS p
JOIN offline_sale o ON p.product_id = o.product_id
GROUP BY product_code
ORDER BY sales DESC, product_code
~~~
