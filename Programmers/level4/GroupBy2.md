https://school.programmers.co.kr/learn/courses/30/lessons/131532


"""
SELECT YEAR(sales_date) as year, MONTH(sales_date) as month, ui.gender, count(distinct os.user_id) as users
FROM online_sale os
LEFT JOIN user_info ui ON os.user_id = ui.user_id
WHERE ui.gender IS NOT NULL
GROUP BY year, month, gender
ORDER BY year, month, gender
"""
