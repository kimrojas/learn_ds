## Module 1
- SQL language for relational database (used to query data from database)
- database: repository of data with querying functionality
- data stored as tables (rows and columns)
- table is a collection of related things
- relationships can exists between tables
- dbms (database management  system): tools to manage data (rdms for relational)
- rdbms examples: MySQL, Oracle database, IBM db2

basic commands
- create table
- insert
- select
- update
- delete

What is sql, data, database, relational database, rdbms, 5 basic sql commands

### `select` statement

goal

- retrieve data from relational database
- define the use of a predicate
- identify the syntax of the `SELECT` statement using the `WHERE` clause
- list comparison operators supported by RDMS

**How to use SELECT**

`select * from Book` for all attributes

`select book_id, title, edition, year from Book` for selected attributes (subset of the columns)

**Restrict the results set**

- predicate: a conditonal statement leading to True, False, Unknown and is used for the WHERE

`select book_id, title from Book WHERE book_id='B1"`

- there are other comparison operators (<, >, etc)

**Hands-on select statements**

`SELECT * FROM FilmLocations;`

![alt text](image1-1.png)

`SELECT Title, ReleaseYear, Locations, ProductionCompany, Director FROM FilmLocations WHERE ReleaseYear>=2000;`

![alt text](image1-2.png)

### COUNT, DISTINCT, LIMIT

**COUNT**

- `select COUNT(*) from tablename`

**DISTINCT**

- `select DISTINCT columnname from tablename`

**LIMIT**

- restrict the number of rows retreived from the database
- `select * from tablename LIMIT 10`
- `select * from MEDALS where YEAR = 2018 LIMIT 5

**Hands-on select statement**

`SELECT COUNT(DISTINCT ProductionCompany) FROM FilmLocations WHERE ReleaseYear >= 2015 LIMIT 5`

![alt text](image1-3.png)

`SELECT COUNT(DISTINCT ProductionCompany) FROM FilmLocations WHERE ReleaseYear >= 2015;`

![alt text](image1-4.png)
 

### INSERT statement

```sql
INSERT INTO AUTHOR
    (AUTHOR_ID, LASTNAME, FIRSTNAME, EMAIL, CITY, COUNTRY)
VALUES ('A1', 'Chong', 'Raul', 'rfc@ibm.com', 'Toronto', 'CA')
```

**multiple insert**

```sql
INSERT INTO AUTHOR
    (AUTHOR_ID, LASTNAME, FIRSTNAME, EMAIL, CITY, COUNTRY)
VALUES ('A1', 'Chong', 'Raul', 'rfc@ibm.com', 'Toronto', 'CA')
VALUES ('A1', 'Smith', 'Smith', 'ra@ibm.com', 'Toronto', 'CA')
```

### UPDATE and DELETE statement

**UPDATE**

```sql
UPDATE AUTHOR SET LASTNAME='KATTA' FIRSTNAME='LAKSHMI' WHERE AUTHOR_ID='A2'
```

**DELETE**

```sql
DELETE FROM AUTHOR 
  WHERE AUTHOR_ID='A2'
```

```sql
DELETE FROM AUTHOR 
  WHERE AUTHOR_ID IN ('A1', 'A2')
```




**Hands-on INSERT, UPDATE, DELETE statements**

`SELECT * From Instructor;`

![alt text](image1-5.png)

```sql
INSERT INTO Instructor 
    (ins_id, lastname, firstname, city, country)
VALUES (4, 'Kurt', 'Rojas', 'Vancouver', 'CA')
```

![alt text](image1-6.png)


```sql
update Instructor set lastname='Roxas' where ins_id=4
```

![alt text](image1-7.png)


```sql
delete from Instructor where ins_id=4
```

![alt text](image1-8.png)

### Summary

- Data manipulation language (DML) statements read and modify data 
- The search condition of the WHERE clause uses a predicate to refine the search
- The SQL retrieves specific data from the database
- INSERT, UPDATE, and DELETE statements are DML statements for adding/modifying tables


![alt text](image1-9.png)

