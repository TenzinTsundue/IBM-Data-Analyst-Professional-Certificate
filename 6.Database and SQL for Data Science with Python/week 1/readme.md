# Week 1

*Getting Started with SQL*

* *SQL (Structured Query Language)*:  is a programming language designed for managing data in a relational database
* *Databases* : is an organized collection of structured information, or data, typically stored electronically in a computer system.
* *Relational database* is a collection of data items with pre-defined relationships between them.
	* Data stored in tabular form - columns and rows

*SELECT* Statement : Is a Data Manipulation Language(DML) statement used to read and modify data<br>
`Select * from <tablename>`<br>
`SELECT book_id,title from Book`<br>

*WHERE* Clause: to restricts the result set<br>
`select * from <tablename> WHERE predicate`<br>
`SELECT book_id,title from Book WHERE book_id='B1'`<br>

*COUNT, DISTINCT, LIMIT*
*COUNT()* : a built in function that retrieves the number of rows matching the query criteria.
`select COUNT(*) from tablename`
Rows in the MEDALS table where Country is Canada:<br>
`select COUNT(COUNTRY) from MEDELS where COUNTRY='CANADA'`<br>

*DISTINCT* is used to remove duplicate values from a result set.<br>
`select DISTINCT columnname from tablename`<br>
List  the unique countries that received GOLD medals:<br>
`select DISTINCT COUNTRY from MEDALS where MEDALTYPE = 'GOLD'`<br>

*LIMIT* is used for restricting the number of rows retrieved from the database.<br>
`select * from tablename LIMIT 10`<br>
Retrieve 5 rows in the MEDALS table for a particular year:<br>
`select * from MEDALS where YEAR = 2018 LIMIT 5`<br>

*INSERT* Statement: Is a DML statement
Used to add new rows to a table
```
INSETT INTO [TableName]
	<([ColumnName],...)>
VALUES([Values],..)
```

*UPDATE & DELETE STATEMENT*
UPDATE Statement : Altering rows of a table. Is also a DML statement
```
UPDATE [TableName]
SET [[ColumnName]=[Value]]
<WHERE[Condition]>
``` 
DELETE Statement: Remove 1 or more rows from the table
```
DELETE FROM [TableName]
<WHERE[Condition]>
```
```
DELETE FROM AUTHOR
WHERE AUTHOR_ID IN('A2','A3')
```
