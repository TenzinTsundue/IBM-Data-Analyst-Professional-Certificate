# WEEK 6
*Bonus Module: Advanced SQL for Data Engineering(Honors)*

*Views*
* Can include specified columns from multiple base tables and existing views
* Once created, can be queried like a table
* Only the definition of the view is stored, not the data
* The CREATE VIEW statement creates a view based on one or more tables or views

*Stored Procedures*
* A set of SQL statements stored and executed on the database server
* Reduction in network traffic
* CREATE PROCEDURE statement

*ACID Transactions*
* Transaction is indivisible unit of work consisting of one or more SQL statements
* In ACID transaction all the SQL statements must complete successfully, or none at all.
* A(Atomic): All the changes must be preformed successfully or not at all
* C(Consistent): Data must be in a consistent state before and after the transaction
* I(Isolated): No other process can change the data while the transaction is running
* D(Durable): The changes made by the transaction must persist
* BEGIN, COMMIT, ROLLBACK

*JOIN*
* Combines rows from two or more tables based on a relationship.
* Primary key: uniquely identifies each row in a table
* Foreign key: refers to a primary key of another table
* The tables being joined are related through Primary and Foreign keys

Types of Join
* Inner Join
* Outer Join
	* Left Outer Join
	* Right Outer Join
	* Full Outer Join

*Inner Join*
* Inner joins return only rows from joined tables that have a matching value in a common column
* Rows that do not have a matching value do not appear in the result

*Outer Join*
* Left Outer Join: All rows from the left table & any matching rows from the right table
* Right Outer Join: All rows from the right table & any matching rows from the left table
* Full Outer Join: All rows from both tables
