# WEEK 3
*Intermediate SQL*

Retrieving rows - using a *String Pattern*
* A predicate is an expression that evaluates to True, False , or Unknown
* Use the LIKE predicate with string patterns for the search <br>
`WHERE <columnname> LIKE <string pattern>`<br>
`WHERE fristname LIKE R%`<br>
> % wildcard character<br>
Retrieving rows - using a *Range*
```
select title, pages from Book
WHERE pages >= 290 AND pages <= 300
```
```
select title, pages from Book
WHERE pages between 290 and 300
```
Retrieving rows - using a *Set of Values*
```
select firstname, lastname, country
from Author
	WHERE country='AU' OR country='BR'
```
```
select firstname, lastname, country
from Author
	WHERE country IN ('AU', 'BR')
```

*Sorting Result Sets*
Using *ORDER BY clause*
```
select title from Book
	ORDER BY title
```
> By default the result set is sorted in ascending order, for descending order use DESC keyword
```
select title from Book
	ORDER By title DESC
```
Specifying Column Sequence Number 
Ascending order by Column 2 (number of pages)
```
select title, pages from Book
	ORDER BY 2
```

*Grouping Result Sets*
Eliminating Duplicates- *DISTINCT* clause
```
select distint(country)
	from Author
```
*GROUP BY* clause
```
select country, count(country)
	from Author GROUP BY country
```
```
select country, count(country)
	as Count from Author group by country
```

Restricting the Result Set - *HAVING* clause (work only with Group by clause)
```
select country, count(country)
	as Count from Author
	group by country
	having count(country) > 4
```
*Built-in Database Functions*
*Aggregate or Column Functions*
* Collection of values (e.g. entire column)
* Output; Single value
* Examples: SUM(), MIN(), MAX(), AVG(), etc.
*Scalar and String functions*
* Scalar: Perform operations on every input values
* Examples: ROUND(), LENGTH(), UCASE, LCASE

*Data and Time Built-in Functions*
Most databases contain special datatypes for dates and times.

*Sub-queries and Nested Selects*
Sub-query: A query inside another query
```
select COLUMN1 from TABLE
	where COLUMN2 = (select MAX (COLUMN2) from TABLE) 
```
```
select EMP_ID, SALARY,
	(select AVG(SALARY) from employees)
		AS AVG_SALARY
	from employees;
```

*Working with Multiple Tables*
Accessing Multiple Tables with Sub-queries
```
select * from employees
	where DEP_ID IN
	(select DEPT_ID_DEP from departments);
```
