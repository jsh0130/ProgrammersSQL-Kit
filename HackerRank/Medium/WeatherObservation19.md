https://www.hackerrank.com/challenges/weather-observation-station-19/problem?isFullScreen=true



~~~
SELECT ROUND(SQRT(POW(MAX(lat_n)-MIN(lat_n),2)+POW(MAX(long_w)-MIN(long_w),2)),4)
FROM station
~~~
