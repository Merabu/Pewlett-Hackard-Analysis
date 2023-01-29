# Pewlett-Hackard-Analysis
## Overview of the analysis:
Bobby and I was tasked by his manager to determine the number of retiring employees per tittle, and identify employees who are to participate in mentorship program and then write a report summarize the analysis and help the Bobby’s manager to silver tsunami as many current employees reach retirement age.
	Deliverable 1: The Number of Retiring Employees by Title
	Deliverable 2: The Employees Eligible for the Mentorship Program
	Deliverable 3: A written report on the employee database analysis.

## Process
The first thing i had to do is use the data in csv formata to create six individual table. I achieved by first examining the data and getting an understanding of the data. We used the ERD concept to create a visual map to show the relationship as we assign primary and foreign keys.This process flashed light in my queries which saved my time

![EmployeeDB png](https://user-images.githubusercontent.com/115379848/215355325-566d2477-21c5-4aa8-b7a5-469168e3f73c.png)




## Results
### Total expected retirees: 
There are 72458 employee expected to be at retirement age.

35.76% of the total expected retirement population are Seniors engineers

Followed by senior staff with 34.4% which means the company may face more diffculty in replacing these position as both position need lots of exprience.

![retiring titles](https://user-images.githubusercontent.com/115379848/215355179-b630adb6-dec7-437c-99d6-508c19f02c2c.png)

### Employees Eligible to Participate in Mentorship Program
![image](https://user-images.githubusercontent.com/115379848/215360220-e9340f17-197d-4695-9b6b-f14ca514b538.png)

Over 1940 employess will be selected to take part of the memetorship program wich is expected to train employees 

## additional Queries to assist the management.
### Additional Table
--create a new table table joining currect employees and retiring employees.group by titles
SELECT DB1.TITLE, COUNT(DB1.TITLE) AS CUR_EMP , COUNT(DB2.TITLE) AS RET_EMP
INTO EXTRA_QUERY
FROM BONUS_DB2 DB1
LEFT JOIN UNIQUE_TITLES DB2 ON (DB1.EMP_NO = DB2.EMP_NO)
GROUP BY DB1.TITLE
SELECT * FROM EXTRA_QUERY;


### Additinal  Query
