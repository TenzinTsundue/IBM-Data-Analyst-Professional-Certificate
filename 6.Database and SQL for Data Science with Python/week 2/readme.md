# WEEK 2
*Introduction to Relational Databases and Tables*
Relational Database concepts
Entity-Relationship Model
* Used as a tool to design relational databases

A *primary key* is a key in a relational database that is unique for each record.
*Foreign key* is a column or a set of columns in a table whose values correspond to the values of the primary key in another table

Types of SQL statements(DDL vs. DML)
* DDL(Data Definition Language) statements:
	* Define, change, or drop data
* Common DDL:
	* CREATE
	* ALTER
	* TRUNCATE
	* DROP

* DML(Data Manipulation Language) statements:
	* Read and modify data
	* CRUD operations(Create, Read, Update and Delete rows)
* Common DML:
	* INSERT
	* SELECT
	* UPDATE
	* DELETE

*CREATE TABLE Statement*
Create table statement includes definition of attributes(columns):
	* Names of columns
	* Datatypes of columns
	* Constraints (e.g. Primary Key)
```
CREATE TABLE table_name
(
 column_name_1 datatype optional_parameters,
 column_name_2 datatype,
 ...
 column_name_n datatype
)
```  
```
CREATE TABLE author(
	auther_id char(2) PRIMARY KEY NOT NULL,
	last_name varchar(15) NOT NULL,
	first_name varchar(15) NOT NULL,
	email VARCHAR(40),
	city VARCHAR(15),
	country CHAR(2)
)
```

*ALTER, DROP, and TRUNCATE Tables*

*ALTER*
* Add or remove columns
* Modify the data type of columns
* Add or remove keys
* Add  or remove constraints
```
ALTER TABLE <table_name>
	ADD COLUMN <column_name_1> datatype
	...
	ADD COLUMN <column_name_n> datatype;
```
```
ALTER TABLE <table_name>
	ALTER COLUMN <columns_name> SET DATA TYPE
<datatype>;
```

*DELETE*: 
```
ALTER TABLE author
	DROP COLUMN telephone_number;
```
```
DROP TABLE <table_name>;
```

*TRUNCATE*: Removes all rows from a table, but the table structure and its columns, constraints, indexes, and so on remain.
```
TRUNCATE TABLE <table_name>
	IMMEDIATE;
```
