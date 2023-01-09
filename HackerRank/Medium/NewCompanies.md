https://www.hackerrank.com/challenges/the-company/problem?isFullScreen=true


~~~
SELECT c.company_code, c.founder, count(DISTINCT l.lead_manager_code), count(DISTINCT s.senior_manager_code), count(DISTINCT m.manager_code), count(DISTINCT e.employee_code)
FROM Company as c, Lead_Manager as l, Senior_Manager as s, Manager as m, Employee as e
WHERE c.company_code = l.company_code AND l.company_code = s.company_code AND s.company_code = m.company_code AND m.company_code = e.company_code
GROUP BY c.company_code, c.founder
ORDER BY c.company_code;
~~~
