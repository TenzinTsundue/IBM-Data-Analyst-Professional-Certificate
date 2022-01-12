# Week 1

*Getting Started with SQL*

* *SQL (Structured Query Language)*:  is a programming language designed for managing data in a relational database
* *Databases* : is an organized collection of structured information, or data, typically stored electronically in a computer system.
* *Relational database* is a collection of data items with pre-defined relationships between them.
	* Data stored in tabular form - columns and rows

*SELECT* Statement : Is a Data Manipulation Language(DML) statement used to read and modify data
`Select * from <tablename>`
`SELECT book_id,title from Book`

*WHERE* Clause: to restricts the result set
`select * from <tablename> WHERE predicate`
`SELECT book_id,title from Book WHERE book_id='B1'`

*COUNT, DISTINCT, LIMIT*
*COUNT()* : a built in function that retrieves the number of rows matching the query criteria.
`select COUNT(*) from tablename`
Rows in the MEDALS table where Country is Canada:
`select COUNT(COUNTRY) from MEDELS where COUNTRY='CANADA'`

*DISTINCT* is used to remove duplicate values from a result set.
`select DISTINCT columnname from tablename`
List  the unique countries that received GOLD medals:
`select DISTINCT COUNTRY from MEDALS where MEDALTYPE = 'GOLD'`

*LIMIT* is used for restricting the number of rows retrieved from the database.
`select * from tablename LIMIT 10`
Retrieve 5 rows in the MEDALS table for a particular year:
`select * from MEDALS where YEAR = 2018 LIMIT 5`

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
