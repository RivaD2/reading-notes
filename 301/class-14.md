# DATABASE NORMALIZATION
**Database normalization is a process used to organize a database into tables and columns.  The main idea with this is that a table should be about a specific topic and only supporting topics included**

##What Is A Database Table?
* A relational database is made up of several components.
* The table is most significant of components.
* The database table is where all the data in a database is stored, and without tables, there would not be much use for relational databases.
* Tables should really serve only one purpose
* You can eliminate or reduce anomalies by separating data into different tables. This puts the data into tables serving a single purpose.

## Reasons behind Database Normalization
**There are three main reasons to normalize a database:**

1. To minimize duplicate data
2. To minimize or avoid data modification issues
3. To simplify queries

## Types of Modification Anomalies
**There are three modification anomalies that can occur:**
1. Insert Anomaly: In order to create the record, we need provide a primary key. We can not record facts until we know information for the entire row.
2. Update Anomaly: As we change information, if we don’t update all rows, then inconsistencies appear.
3. Deletion Anomaly: Deletion of a row causes removal of more than one set of facts.

## The Three Different Types of Database Normalization
**There are three common forms of database normalization: 1st, 2nd, and 3rd normal form. They are also abbreviated as 1NF, 2NF, and 3NF respectively.**

1. [First Normal Form](https://www.essentialsql.com/get-ready-to-learn-sql-8-database-first-normal-form-explained-in-simple-english/) – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.
2. [Second Normal Form](https://www.essentialsql.com/get-ready-to-learn-sql-10-database-second-normal-form-explained-in-simple-english/) – The table is in first normal form and all the columns depend on the table’s primary key.
3. [Third Normal Form](https://www.essentialsql.com/get-ready-to-learn-sql-11-database-third-normal-form-explained-in-simple-english/) – the table is in second normal form and all of its columns are not transitively dependent on the primary key

**Just remember that the above forms are progressive so they add upon one another. To reach the second normal form, all criteria must have been met for the first form. Sound confusing?**

### If you would like to learn more, please visit the sites below that I used to reference the material above:
* [Database Normalization Explained in Plain English](https://www.essentialsql.com/get-ready-to-learn-sql-11-database-third-normal-form-explained-in-simple-english/)
* [What is a Database Table from essentialSQL.com](https://www.essentialsql.com/what-is-a-database-table/)
