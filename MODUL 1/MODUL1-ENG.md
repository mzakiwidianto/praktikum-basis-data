# **MODULE 1**
###### Table of Content
- [**MODULE 1**](#module-1)
          - [Table of Content](#table-of-content)
  - [**Introduction to Databases***](#pengantar-database)
    - [***Database***](#database)
    - [**DBMS**](#dbms-database-management-system)
    - [**SQL**](#sql)
    - [**Data Types in MySQL**](#data-types-in-mysql)
  - [***Data Definition Language* (DDL)**](#data-definition-language-ddl)
  - [**DDL Statements in MySQL**](#statement-ddl-pada-database-mysql)
  - [***MySQL Constraints***](#mysql-constraint)
  - [***Referential Integrity Constraint***](#referential-integrity-constraint)

---
## **Pengantar *Database***
- ### ***Database***
    <div align='justify'>
    &nbsp;&nbsp;&nbsp;A database is a collection of data organized into tables that are interrelated or stand-alone and stored together on a medium. Databases can be used by one or more application programs optimally, and the data is stored without depending on the programs that will use it.
    </div>

- ### DBMS (*Database Management System*)
    <div align='justify'>
    &nbsp;&nbsp;&nbsp;DBMS is a software or system designed to process a database and perform operations on the data requested by its users. The main purpose of using a DBMS is to avoid chaos when processing large amounts of data.
    <br>
    <br>
    Examples of DBMS include:
    <br><ul><li>MySQL</li>
    <li>Microsoft Access</li> 
    <li>Airtable</li> 
    <li>Oracle</li> 
    <li>SQL Server</li>
    </div>

- ### SQL
    <div align='justify'>
    &nbsp;&nbsp;&nbsp;SQL (<i>Structured Query Language</i>) is an ANSI (<i>American National Standard Institute</i>) standard computer language for accessing and manipulating data in relational databases.
    <br>
    <br>
    The SQL functions include:
    <br>
    <b><ul><li>Running a <i>query</i> in a <i>database</i></b></li>
    SQL is used to execute queries or commands to retrieve specific data from a relational database.
    <br>
    <br>
    <b><li>Inserting data into a <i>database</i></b></li>
    SQL is also used to insert new data into a relational database. New data can be inserted into a table using the INSERT command. 
    <br>
    <br>
    <b><li>Changing data in the <i>database</i></b></li>
    SQL allows users to change data in a relational database by using the UPDATE command. This command allows users to change existing values in a table column.
    <br>
    <br>
    <b><li>Deleting data in the <i>database</i></b></li>
    SQL also allows users to delete data in a relational database by using the DELETE command. This command allows users to delete one or more rows of data from a table.</ul>
    <br>
    <p align="center">
    <img src="img/1.webp" width="350">
    <br>
    <i>SQL Command Types</i>
    </p>

    SQL uses commands that can be grouped into 4 :
    <br>
    <b><ul><li>DDL (<i>Data Definition Language</i>)</b></li>
    DDL is used to define or manage database objects such as tables, columns, indexes, and procedures.
    <br>
    <br>
    <b><li>DML (<i>Data Manipulation Language</i>)</b></li>
    DML is used to manipulate data in the database such as adding, changing, and deleting data.
    <br>
    <br>
    <b><li>DCL (<i>Data Control Language</i>)</b></li>
    DCL is used to set user access rights to the database such as giving permission to read or write to certain tables.
    <br>
    <br>
    <b><li>TCL (<i>Transaction Control Language</i>)</b></li>
    TCL is used to manage database transactions such as COMMIT (confirming transactions) and ROLLBACK (canceling transactions).</ul>
    </div>
- ### Data Types in MySQL
    <div align='justify'>
    &nbsp;&nbsp;&nbsp;A data type is a form of data modeling that is declared when creating a table. This data type will affect any data that will be entered into a table. The data to be entered must match the declared data type. The various data types in MySQL can be seen as follows:
    </div>
    <br>
    
    | Tipe Data        | Deskripsi    |
    | :------------- |:-------------|
    | `Char (size)`      | Defines a String of length _size_ characters. If _size_ is not included then the character length is 1. |
    | `Varchar (size)`    | Defines a String whose length is arbitrary. The maximum character length is 4000.|
    | `Int (size)` | Used to store positive and negative integer data. |
    | `Time`     | Used to store time values in hour, minute, and second formats within the time range 00:00:00 to 23:59:59.  |
    | `Date` | Defines a date. Dates that can be stored between January 1, 4712 BC and December 31, 9999 AD.|
    | `Decimal (size, d)`      | A data type for storing decimal numbers with a certain precision. The _size_ parameter specifies the number of digits that can be stored, while the d parameter specifies the number of digits placed after the decimal point.|
    | `Double` | A data type for storing fractional numbers with high precision. This data type can store numbers with a larger number of digits than the FLOAT data type.|
    | `Float`      | A data type for storing fractional numbers with lower precision than the DOUBLE data type.|
    | `Boolean/Tinyint(1)` | A data type used to store boolean or logical (true/false) values. This data type is a variant of the Tinyint data type with a length of 1.|
    | `Text`      | A data type used to store text of very large length. It can store text up to 65,535 characters long.|
    | `Blob` | A data type used to store binary data of very large length. This data type can store binary data up to 65,535 bytes long. |

    ___
## ***Data Definition Language* (DDL)**
<div align='justify'>
&nbsp;&nbsp;&nbsp;DDL or Data Definition Language is an SQL (<i>Structure Query Language</i>) programming language that has commands to create and modify the structure of an object in a database that is mainly in the form of a schema. These objects can be tables, indexes, views, and triggers. The main functions of DDL are as follows: 
</div>

- **_CREATE_**
    <div align='justify'>
    &nbsp;&nbsp;&nbsp;The <i>CREATE</i> command is used to create a new object, either a database, a table, an index, or a stored procedure. The syntax of the <i>CREATE</i> command can vary depending on the object being created, but is generally as follows :
    <br>
    <br>
    </div>

    ```sql
	CREATE TABLE student (
		id INT PRIMARY KEY,
		name VARCHAR(50),
		major VARCHAR(50),
		date_birth DATE,
	);
    ```

- **_ALTER_**
    <div align='justify'>
    &nbsp;&nbsp;&nbsp;The <i>ALTER</i> command is used to change or modify the structure of an existing table in the database, by adding, deleting or changing the data type of a column in the table, changing the table name, adding and deleting indexes, or determining the Primary Key or Foreign Key. The <i>ALTER</i> command syntax can vary depending on the object you want to modify. However, it generally has the following structure:
    <br>
    <br>
    </div>

    ```sql
    ALTER TABLE student 
    ADD COLUMN adress VARCHAR(50); 
    ```
- **_DROP_**
    <div align='justify'>
    &nbsp;&nbsp;&nbsp;The <i>DROP</i> command is used to delete or remove objects in the database. The <i>DROP</i> command cannot be undone, so objects that have been deleted cannot be restored. The syntax for the <i>DROP</i> command is generally as follows :
    <br>
    <br>
    </div>

    ```sql
    DROP TABLE student;
    ```
---
## **DDL Statements in MySQL <i>Database</i>**
- ### ***Database* Creation**
    - #### **CREATE DATABASE**
        <div align='justify'>
        Used to create a database in the MySQL server.
        <br>
        Command:
        </div>
        <br>

        ```sql
        CREATE DATABASE database_name;
        ```
        Example : 
        <p align="center">
        <img src="img/2.png" width="550">
        </p>

    - #### **SHOW DATABASE**
        <div align='justify'>
        Used to view the entire database that has been created. <br>Command:
        </div>
        <br>

        ```sql
        SHOW DATABASES;
        ```
        Example : 
        <p align="center">
        <img src="img/3.png" width="350">
        </p>


    - #### **USE DATABASE**
        <div align='justify'>
        Used to access the database that has been created. This command is needed when we will use the database.
        <br>
        Command:
        </div>
        <br>

        ```sql
        USE database_name;
        ```

    - #### **CREATE TABLE**
        <div align='justify'>
        Used to create tables in a database.
        <br>
        Command :
        </div>
        <br>

        ```sql
        CREATE TABLE table_name (
        column_name1 data_type null / not null primary key / not,
        column_name2 data_type null / not null
        );
        ```
        Example : 
        <p align="center">
        <img src="img/4.png" width="550">
        </p>


    - #### **SHOW TABLE**
        <div align='justify'>
        Used to view all tables that have been created      previously. (With the condition: Already in the database that has the table)
        <br>
        Command :
        </div>
        <br>

        ```sql
        SHOW TABLES;
        ```
        Example : 
        <p align="center">
        <img src="img/5.png" width="450">
        </p>


    - #### **DESC TABLE**
        <div align='justify'>
        DESC stands for DESCRIBE. DESC is used to describe the structure of a table.
        <br>
        Command: 
        </div>
        <br>

        ```sql
        DESC table_name;
        ```
        Contoh : 
        <p align="center">
        <img src="img/6.png" width="400">
        </p>

        
    - #### **FOREIGN KEY**
        <div align='justify'>
        A foreign key is a field in one table that refers to a primary key in another table. The table that has the foreign key is called the child table, while the table that has the primary key is called the parent table or the referenced table. Foreign Key means that values in one table can correlate with other tables using the same id. Foreign Key or FK is a referential integrity in the database.
        <br>
        Command:
        </div>
        <br>

        ```sql
        CREATE TABLE table_name (
            column_name1 data_type null / not null primary key / not,
            column_name2 data_type null / not null,
            CONSTRAINT fk_column
            FOREIGN KEY (column1, column2, …)
            REFERENCES parent_table_name (parent_column)
        );
        ```
        Example : 
        <p align="center">
        <img src="img/7.png" width="650">
        <img src="img/8.png" width="450">
        </p>
<!-- Checkpoint -->
- ### **ALTER TABLE**
    - #### **ADD COLUMN**
        <div align='justify'>
        Add Column is used to create columns in a table.
        <br>
        Command :
        </div>
        <br>

        ```sql
        ALTER TABLE table_name ADD column_name data_type;
        ```
        Example : 
        <p align="center">
        <img src="img/9.png" width="500">
        </p>
        
    - #### **ADD MULTIPLE COLUMN**
        <div align='justify'>
        Add Multiple Column is used to add multiple columns to a table. 
        <br>
        Command :
        </div>
        <br>

        ```sql
        ALTER TABLE table_name 
        ADD column_name1 data_type, 
        ADD column_name2 data_type;
        ```
        Example : 
        <p align="center">
        <img src="img/10.png" width="500">
        </p>

    - #### **ADD FOREIGN KEY**
        <div align='justify'>
        Add Foreign Key is used to add a foreign key to a table.
        <br>
        Command :
        </div>
        <br>

        ```sql
        ALTER TABLE table_name
        ADD CONSTRAINT fk_column
        FOREIGN KEY (column1, column2, …)
        REFERENCES parent_table_name (parent_column)
        ;
        ```
        Example : 
        <p align="center">
        <img src="img/11.png" width="500">
        </p>


    - #### **MODIFY COLUMN**
        <div align='justify'>
        Modify Column is used to change the data type of a column in a table.
        <br>
        Command :
        </div>
        <br>

        ```sql
        ALTER TABLE table_name
        MODIFY column_name data_type;   
        ```
        Contoh : 
        <p align="center">
        <img src="img/12.png" width="500">
        </p>


    - #### **MODIFY MULTIPLE COLUMN**
        <div align='justify'>
        Modify Multiple Column is used to change the data type of several columns in a table.
        <br>
        Command: 
        </div>
        <br>

        ```sql
        ALTER TABLE table_name
        MODIFY column_name1 data_type
        MODIFY column_name2 data_type;
        ```
        Example : 
        <p align="center">
        <img src="img/13.png" width="550">
        </p>

    - #### **RENAME COLUMN**
        <div align='justify'>
        Rename Column is used to rename a column in a table.
        <br>
        Command :
        </div>
        <br>

        ```sql
        ALTER TABLE table_name
        RENAME COLUMN column_name
        TO new_column_name; 
        ```
        Contoh : 
        <p align="center">
        <img src="img/14.png" width="500">
        </p>

    - #### **RENAME TABLE**
        <div align='justify'>
        Rename Table is used to rename a table.
        <br>
        Command :
        </div>
        <br>

        ```sql
        ALTER TABLE table_name
        RENAME TO new_table_name;
        ```
        Example :
        <p align="center">
        <img src="img/15.png" width="500">
        </p>

- ### **DROP**
    - #### **DROP COLUMN**
        <div align='justify'>
        Drop Column is used to delete columns in a table.
        <br>
        Command :
        </div>
        <br>

        ```sql
        ALTER TABLE table_name
        DROP COLUMN column_name;
        ```
        Example : 
        <p align="center">
        <img src="img/16.png" width="500">
        </p>

    - #### **DROP FOREIGN KEY**
        <div align='justify'>
        Drop Foreign Key is used to delete a foreign key in a table with the command :
        </div>
        <br>

        ```sql
        ALTER TABLE table_name
        DROP FOREIGN KEY fk_column;
        ```
        Example : 
        <p align="center">
        <img src="img/17.png" width="500">
        <img src="img/18.png" width="500">
        </p>

    - #### **DROP TABLE**
        <div align='justify'>
        Drop Table is used to delete a table in an SQL query.
        <br>
        Command:
        </div>
        <br>

        ```sql
        DROP TABLE table_name;
        ```
        Example : 
        <p align="center">
        <img src="img/19.png" width="500">
        </p>

    - #### **DROP DATABASE**
        <div align='justify'>
        Drop database is used to delete a database that has been created.
        <br>
        Command:
        </div>
        <br>

        ```sql
        DROP DATABASE database_name;
        ```
        Contoh : 
        <p align="center">
        <img src="img/20.png" width="500">
        </p>

---
## ***MySQL Constraint***
<div align='justify'>
&nbsp;&nbsp;&nbsp;<b><i>MySQL Constraint</i></b> are used to define rules that limit what values or data can be stored in columns within MySQL database tables. These constraints are used to limit the type of data that can be included in a table. MySQL Constraints are declared when creating a table.</div> <br>

BHere are some <b>constraints</b> that are often used in MySQL tables:
<!-- Checkpoint 2 -->
1.  #### **NOT NULL**
    <div align='justify'>
    In MySQL, the NOT NULL constraint allows to specify that a column cannot contain NULL values. MySQL NOT NULL can be used when CREATE and ALTER tables.
    </div>

2.  #### **UNIQUE**
    <div align='justify'>
    The UNIQUE constraint in MySQL ensures that each value in a column is unique or cannot be a duplicate. With this constraint, unwanted data duplication is prevented. In addition, the UNIQUE constraint serves to ensure the integrity of data.
    </div>
    
3.  #### **PRIMARY KEY**
    <div align='justify'>
    PRIMARY KEY is a constraint that enforces a table to accept unique data for a particular column. PRIMARY KEY identifies each row in the table by creating a unique index and can help to access the table faster.  
    </div>
    
4.  #### **FOREIGN KEY**
    <div align='justify'>
    FOREIGN KEY in MySQL is used to create a link between two tables with one specific column from both tables. The column specified in one table must be a PRIMARY KEY and referenced by a column of another table known as a FOREIGN KEY.
    </div>
    
5.  #### **CHECK**
    <div align='justify'>
    CHECK is a constraint that controls the values in the corresponding column.The CHECK constraint determines whether or not the value is valid from a logical expression.
    </div>
    
6.  #### **DEFAULT**
    <div align='justify'>
    In a MySQL table, every column must contain a value (including NULLs). When inserting data into a table, if no value is assigned to the column, then the column will get the value set as DEFAULT.
    </div>
    
7.  #### **INDEX**
    <div align='justify'>
    The INDEX constraint is used to index one or more columns in a table. INDEX speeds up searching and sorting data in a table. Indexes can be created on columns that have high cardinality, meaning there are many unique values in the column.
    </div>
    
8.  #### **AUTO INCREMENT**
    <div align='justify'>
    AUTO INCREMENT constraint is used to create a column whose value is automatically incremented when a new row is inserted into the table. Usually, AUTO INCREMENT is used on Primary Key columns to generate unique values and increment automatically.
    </div>
    
9.  #### **ON DELETE dan ON UPDATE**
    <div align='justify'>
    ON DELETE and ON UPDATE constraints are used to specify the action to be taken on a row in a table that has a reference to a row in another table when that row is deleted or updated. There are four actions that can be performed, namely RESTRICT, CASCADE, SET NULL, and NO ACTION.
    </div>
    
10. #### **UNIQUE INDEX**
    <div align='justify'>
    The UNIQUE INDEX constraint is used to restrict unique values to one or more columns in a table. UNIQUE INDEX ensures that no two rows have the same value in that column.
    </div>
    
11. #### **NOT NULL WITH DEFAULT**
    <div align='justify'>
    The NOT NULL WITH DEFAULT constraint is used to restrict non-null values in a column and provide a default value when a value is not provided when inserting new data into the table.
    </div>
    
12. #### **VIRTUAL**
    <div align='justify'>
    VIRTUAL constraint is used to create a virtual column that results from an expression or calculation on another column in the table. The virtual column is not stored in the table but is generated when the column is displayed.
    </div>

<div align='justify'>
&nbsp;&nbsp;&nbsp;All of the above constraint types can be used when creating or modifying table structures in MySQL. Proper use of constraints can improve the integrity of the data in the table and ensure that the data entered into the table is always valid and accurate.</div>

---
## ***Referential Integrity Constraint***
<div align='justify'>
&nbsp;&nbsp;&nbsp;Referential Integrity Constraint is a database rule that aims to ensure that the relationship between two tables remains consistent. This constraint ensures that every value in a column used as a foreign key in a table must match the value in the primary key column in the corresponding table. There are two kinds of tables: child tables and parent tables. Referential integrity rules are usually used when there is a data modification process such as insert, update, and delete.</div><br>

Here are some of the rules in the Referential Integrity Constraint:

1. #### Update Rule
    This rule applies during the modification process in the parent table :

    - CASCADE 	: An update of a data row is followed by an update of the data row in the child table to which it is linked.

    - RESTRICT 	: Prevents the data update process if there is a data row in the child table that is correlated.  

    - IGNORE 	: Ignore the reference. Can update the data in the parent, but not the related data in the child table.

2. #### Delete Rule
    This rule applies to the modification process in the parent table.

    - CASCADE	: Deletes all rows of data in the resolved child table. 

    - RESTRICT 	: Prevents deletion if there are related rows in the child table. 

    - IGNORE 	: Ignore the reference. May delete data, and has no effect on the child table.

3. #### Insert Rule
    This rule applies to the process of adding data in the parent table. 

    - RESTRICT 	: Do not add data to the child table, if the value inserted in the related column does not exist in the parent table. 

    - IGNORE 	: Ignore the reference. You can add data to the child, even if the value entered in the related column does not exist in the parent table.

    