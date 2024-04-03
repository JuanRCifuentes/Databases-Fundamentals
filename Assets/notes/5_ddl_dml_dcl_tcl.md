# [Database Fundalmentals](../../README.md)
## 5. DDL, DML, DCL and TCL (and Referencial Integrity) [6]

- [Database Fundalmentals](#database-fundalmentals)
  - [5. DDL, DML, DCL and TCL (and Referencial Integrity) \[6\]](#5-ddl-dml-dcl-and-tcl-and-referencial-integrity-6)
    - [5.1 DDL (Data Definition Language)](#51-ddl-data-definition-language)
    - [5.2 DML (Data Manipulation Language)](#52-dml-data-manipulation-language)
    - [5.3 DCL (Data Control Language)](#53-dcl-data-control-language)
    - [5.4 TCL (Transaction Control Language)](#54-tcl-transaction-control-language)
    - [5.5 Referencial Integrity](#55-referencial-integrity)

### 5.1 DDL (Data Definition Language)

This language allows us to create and modify a database structure. Examples in section 6.

- CREATE: Create schemas (databases), tables, columns and registers.
- ALTER: Modify schemas (databases), tables, columns and registers.
- DROP: Basically delete (WARNING !!)... schemas (databases), tables, columns and registers.
- TRUNCATE: Delete every register within a table.
- COMMENT: Add comments to the data dictionary.
- RENAME: Rename objects.

### 5.2 DML (Data Manipulation Language)

It's not about the database structure but about the database content. It's a language used to store, modify, retrieve, delete and update data in a database

- SELECT: Retrieve data from a database

    ```sql
    SELECT column_name FROM table_name
    ```
- INSERT: Insert data into a database

    ```sql
    INSERT 
    INTO table_name (name_column1, name_column2)
    VALUES (value_column1, value_column2);
    ```
- UPDATE: Updates existing data within a database

    ```sql
    -- Change one register
    UPDATE table_name
    SET name_column1 = value_column1, name_column2 = value_column2
    WHERE register_id = register_value;
    
    -- Change all registers with a value in a column
    UPDATE table_name
    SET name_column = new_value_column
    WHERE name_column2 = value_column
    ```
- DELETE: Deletes all records from a database table

    ```sql
    DELETE FROM table_name
    WHERE regisetr_id = register_id_value
    ```
- MERGE
- CALL
- EXPLAIN PLAN
- LOCK TABLE

### 5.3 DCL (Data Control Language)

This is a language mostly concerned with rights, permissions and other controls of the database.

- GRANT: Allow users access privileges to the database
- REVOKE: Withdraw users privileges given by using the GRANT command

### 5.4 TCL (Transaction Control Language)

Deals with a transaction within a database

- COMMIT
- ROLLBACK
- SAVEPOINT
- SET TRANSACTION

### 5.5 Referencial Integrity

[What is Referential Integrity?](https://database.guide/what-is-referential-integrity/)