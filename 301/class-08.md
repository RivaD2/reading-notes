# A Quick Intro to SQL 
![SQL](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTQU44Ntv-EdtPTsURwsAdFKgpHPmu-t4KFxQ&usqp=CAU)
**What is SQL and why use it? Let's get started!**

## What is SQL?
* Structured Query Language, or SQL, is a standard programming language for **relational databases**
* What is a relational database you might ask?

>It is a common misconception that the word relational implies relationship between the tables. A relation is a mathematical term that is roughly equivalent to a table itself. When used
in conjunction with the word database, we mean to say that this particular system arranges data in a tabular fashion.
>
* Almost all database management systems you’ll come across will have a SQL implementation
* What is a DBMS? A **Database Management System (DBMS)** is a collection of programs which enables its users to access database, manipulate data, reporting and representation of data. It also helps to control access to the database.
* Using SQL, you can query, update, and reorganize data, as well as create and modify the schema (structure) of a database system and control access to its data.
* It is a language for interacting with databases and it consists of commands that allow us to carry out operations with a [database](https://www.guru99.com/introduction-to-database-sql.html).


**Let's picture a spreadsheet...We know that spreadsheets like  Excel can compile a lot of data but SQL is intended to compile and manage data in much greater volumes. SQL databases can handle millions, or even billions, of cells of data.**

---------

## Why use SQL?
* Allows users to access data in the relational database management systems.
* Allows users to describe the data.
* Allows users to define the data in a database and manipulate that data.
* Allows to embed within other languages using SQL modules, libraries & pre-compilers.
* Allows users to create and drop databases and tables.
* Allows users to create view, stored procedure, functions in a database.
* Allows users to set permissions on tables, procedures and views.

-----

## Practicing commands on a relational database 
1. **Use Ingres:** Ingres comes in a free and open source edition, it’s available on most major platforms and it’s a full-fledged
enterprise class database with many features.
1. **Use SQL-Lite:** SQLite is an in-process library that implements a self-contained, serverless, zero-configuration, transactional SQL database engine. The code for SQLite is in the public domain and is thus free for use for any purpose, commercial or private. 
 * SQLite is an embedded SQL database engine. Unlike most other SQL databases, SQLite does not have a separate server process. SQLite reads and writes directly to ordinary disk files.

 ------

## SQL in Action
### When you are executing an SQL command for any RDBMS, the system determines the best way to carry out your request and SQL engine figures out how to interpret the task.

**There are various components included in this process and these components are:

1. Query Dispatcher
1. Optimization Engines
1. Classic Query Engine
1. SQL Query Engine, etc.
1. A classic query engine handles all the non-SQL queries, but a SQL query engine won't handle logical files.

## SQL commands:

1. **Data Definition Language:**
* CREATE - Creates a new table, a view of a table, or other object in the database.
  * The command `createdb` is used to create a database which will serve as a holding envelope for your tables.
* INSERT- ```INSERT INTO <Table Name>
 VALUES ('Value1', 'Value2', ...);```
* ALTER -Modifies an existing database object, such as a table.
* DROP -Deletes an entire table, a view of a table or other objects in the database.


2. **Data Manipulation Language:**
* SELECT- Retrieves certain records from one or more tables.
* INSERT- Creates a record.
* UPDATE- Modifies records.
* DELETE- Deletes records.

3. **Data Control Language**
* GRANT -Gives a privilege to user.
* REVOKE -Takes back privileges granted from user.
----

## Writing a Query
* A query is a way to check the results of our previous operations in which we created a table and inserted rows of data into it. 
* To write a query, we would use a Data Query Language (DQL) command called SELECT.
* A query is simply a SQL statement that allows you to retrieve a useful subset of data contained within your database. 
* For example, fetching operation with `SELECT` falls under the query category.
* Most of our day-to-day operations in a SQL environment would involve queries, because we would create the database structure once (modifying it only on a need basis) and inserting rows only
when new data is available
 
 **To Learn more about SQL, click below to visit the articles I used to reference the info above. You will find they go into much more detail on how to get started using SQL.**

 1. [A Primer On SQL: 3rd Edition](https://openlibra.com/en/book/download/a-primer-on-sql-3rd-edition)
 1. [Tutorials Point: Learn SQL](https://www.tutorialspoint.com/sql/sql-overview.htm)
 1. [Guru 99: What is a Database: What is SQL?](https://www.guru99.com/introduction-to-database-sql.html)
 1. [SQLite.Org](https://www.sqlite.org/about.html)
