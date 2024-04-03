# [Database Fundalmentals](../../README.md)
## 6. Databases (or Schemas), Tables and Views

- [Database Fundalmentals](#database-fundalmentals)
  - [6. Databases (or Schemas), Tables and Views](#6-databases-or-schemas-tables-and-views)
    - [6.1 Databases (or schemas) \[7\]](#61-databases-or-schemas-7)
      - [CREATE, USE and DROP](#create-use-and-drop)
    - [6.2 Tables \[8\]](#62-tables-8)
      - [CREATE, ALTER and DROP](#create-alter-and-drop)
    - [6.3 Views \[8\]](#63-views-8)
      - [CREATE](#create)


### 6.1 Databases (or schemas) [7]

Collection of tables that stores a specific set of structured data 

#### CREATE, USE and DROP

```sql
CREATE DATABASE database_name;
CREATE SCHEMA schema_name;

USE DATABASE database_name; // Set as default schema/database

DROP DATABASE database_name;
DROP SCHEMA schema_name;
```

### 6.2 Tables [8]

Is defined as a database object which is used to store data in a database. Tables stores data in a logically organized row-column format.

#### CREATE, ALTER and DROP

```sql
CREATE TABLE database_name . table_name (
	register_id INT NOT NULL AUTO_INCREMENT,
	property_1 VARCHAR(255) NULL,
	PRIMARY KEY ( register_id )
);

ALTER TABLE database_name . table_name 
DROP COLUMN column_name;

ALTER TABLE database_name . table_name
ADD COLUMN column_name <SPECIFICATIONS>;
// Specifications Ex: DATETIME NULL AFTER before_column_name;

DROP TABLE database_name . table_name
```

### 6.3 Views [8]

Is just like a virtual table that holds data from one or more than one table. A view includes a set of SQL queries for retrieving data from the database. Views are kept in memory, so there is no need to make the query again.

#### CREATE

```sql
CREATE OR REPLACE VIEW v_view_name AS 
	SELECT column_name1, column_name2 
	FROM table_name 
	WHERE column_name3 = 'example';
```
