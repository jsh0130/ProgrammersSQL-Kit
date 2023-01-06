https://www.hackerrank.com/challenges/the-pads/problem?isFullScreen=true

'''
SELECT CONCAT(NAME,'(',LEFT(OCCUPATION,1),')')
FROM OCCUPATIONS ORDER BY NAME;

SELECT CONCAT('There are a total of ',COUNT(name),' ',lower(occupation),'s.')
FROM occupations GROUP BY occupation ORDER BY count(name), occupation;
'''
