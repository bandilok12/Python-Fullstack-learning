#### **What is data, field, record, database?**

**====================================================================**



**What is Data?**

\-------------

raw facts or figures without context.

example: 101,Ravi,50000,hyd



**What is the field?**

\------------------

smallest unit of data in a database(column/attribute)

example: EmpName, EmpId, EmpSalary, EmpAddress



**What is Record?**

\---------------

collection of related fields(row/tuple)

example :(111,ravi,60000,vjy)



**What is a database?**

\-------------------

organized collection of related records stored together.

example : an employee database containing all employee records.





#### **Client-server Architecture**

**===============================================**



**client** : the role of the client in client-server architecture is to send requests to the server. and to get a response from the server.



**Server** : server is software the role of the server in client-server arch is to take requests from clients.

if the request is a valid request then it will generate some response we can handover that response to the client. If the client request is not a valid request then it will raise the errors.



**protocol** : it has a set of rules and regulations. The role of the protocol in client-server arch is to send requests from client to server.





#### **SQL Identifiers**

**===========================**



SQL identifiers are names used to identify database objects such as.

Database names, Table names, Column names, view names, index names, constraints, triggers, stored procedures.



While we are declaring an identifier we have to follow some rules and regulations.

1\. the only allowed characters to declare identifiers a-z or A-Z or 0-9,\_,$

2\. must begin with a letter or underscore(\_).

3\. we can't declare identifiers with reserved keywords.

4\. spaces are not considered to declare identifiers.

5\. identifiers are case sensitive

6\. max length to declare identifiers are 15 characters.





#### **SQL Commands**

**======================**



SQL (Structured Query Language) commands are broadly classified into five main categories based on their functionality: DDL, DML, DQL, DCL, and TCL. 

Each category and every command within it is explained below with its purpose and usage.

Command

Description / Definition

**DDL**

Data Definition Language - defines and modifies the structure of database objects (tables, schemas, indexes).

**DML**

Data Manipulation Language - manages data stored within database objects (insert, update, delete).

**DQL**

Data Query Language - used to fetch/retrieve data from the database.

**DCL**

Data Control Language - manages permissions and access control on database objects.

**TCL**

Transaction Control Language - manages transactions to maintain data integrity.





**1. DDL - Data Definition Language**

**---------------------------------**

DDL commands are used to define, create, alter, and remove the structure of database objects such as tables, schemas, and indexes. Changes made by DDL commands are auto-committed and permanent.

Command

Description / Definition

**CREATE**

Creates a new database object such as a table, database, view, index, or schema. Example: CREATE TABLE Students (ID INT, Name VARCHAR(50));

**ALTER**

Modifies the structure of an existing database object, such as adding, deleting, or modifying columns in a table. Example: ALTER TABLE Students ADD Email VARCHAR(100);

**DROP**

Permanently deletes an existing database object (table, database, index, view) along with all its data and structure. This action cannot be rolled back in most databases.

**TRUNCATE**

Removes all rows/records from a table quickly while keeping the table structure intact for future use. Faster than DELETE as it does not log individual row deletions.

**RENAME**

Renames an existing database object, such as a table or column, to a new name without changing its structure or data.

**COMMENT**

Adds explanatory notes or comments to database objects (tables, columns) for documentation purposes; does not affect data or structure.



&#x20;

#### **Data Types**

**==================**



Data types in MySQL are essential for defining the kind of information each column in your table can store.



Categorical Overview

•   Numeric Data Types: Used for storing numerical values.

•   String Data Types: Used for storing text data.

•   Date and Time Data Types: Used for storing date and time information.



**Numeric Data Types**

**------------------**

•   TINY INT

•   SMALL INT

•   MEDIUM INT

•   INT / INTEGER

•   BIG INT

•   FLOAT

•   DOUBLE

•   DECIMAL (M,D)



**TINY INT**

•   Stores very small integers

•   Range:

1. Signed: -128 to 127
2. Unsigned: 0 to 255

&#x20;

&#x20; CREATE TABLE tinyint\_example (

&#x20;     age TINYINT

&#x20; );

&#x20; INSERT INTO tinyint\_example (age) VALUES (25);

&#x20;

**SMALL INT**

•   Stores small integers

•   Range:

1. Signed: -32,768 to 32,767
2. Unsigned: 0 to 65,535

&#x20;

&#x20; CREATE TABLE smallint\_example (

&#x20;     population SMALLINT

&#x20; );

&#x20; INSERT INTO smallint\_example (population) VALUES (15000);

&#x20;

**MEDIUM INT**

•   Stores medium sized integers

•   Range:

1. Signed: -83,88,608 to 83,88,607
2. Unsigned: 0 to 1,67,77,215

&#x20;

&#x20; CREATE TABLE mediumint\_example (

&#x20;     visitors MEDIUMINT

&#x20; );

&#x20; INSERT INTO mediumint\_example (visitors) VALUES (5000000);

&#x20;

**INT / INTEGER**

•   Stores standard integers

•   Range:

1. Signed: -2,14,74,83,648 to 2,14,74,83,647
2. Unsigned: 0 to 4,29,49,67,295

&#x20;

&#x20; CREATE TABLE int\_example (

&#x20;     product\_id INT

&#x20; );

&#x20; INSERT INTO int\_example (product\_id) VALUES (123456);

&#x20;

**BIG INT**

•   Stores large integers

•   Range:

1. Signed: -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807
2. Unsigned: 0 to 18,446,744,073,709,551,615

&#x20;

&#x20; CREATE TABLE bigint\_example (

&#x20;     account\_balance BIGINT

&#x20; );

&#x20; INSERT INTO bigint\_example (account\_balance) VALUES (5000000000);

&#x20;

**FLOAT**

•   Stores floating-point numbers with single precision.

•   Range: Approx -3.402823466E+38 to 3.402823466E+38

&#x20;

&#x20; CREATE TABLE float\_example (

&#x20;     temperature FLOAT

&#x20; );

&#x20; INSERT INTO float\_example (temperature) VALUES (36.5);

&#x20;

**DOUBLE**

•   Stores floating-point numbers with double precision.

•   Range: Approx -1.7976931348623157E+308 to 1.7976931348623157E+308

&#x20;

&#x20; CREATE TABLE double\_example (

&#x20;     distance DOUBLE

&#x20; );

&#x20; INSERT INTO double\_example (distance) VALUES (12345.6789);

&#x20;

**DECIMAL (M,D)**

•   Stores fixed-point numbers with exact precision, commonly used for financial data.

•   M is the maximum number of digits, and D is the number of digits after the decimal.

&#x20;

&#x20; CREATE TABLE decimal\_example (

&#x20;     price DECIMAL(10, 2)

&#x20; );

&#x20; INSERT INTO decimal\_example (price) VALUES (1999.99);

&#x20;

&#x20;

**String and Binary Data Types**

**----------------------------**

•   CHAR

•   VARCHAR

•   TEXT

•   TINY TEXT

•   MEDIUM TEXT

•   LONG TEXT

•   ENUM

•   SET



**CHAR**

•   Fixed-length string data type.

•   Ideal for storing strings that have a consistent length.

•   Pads the string with spaces to the specified length if the input is shorter.

&#x20;

&#x20; CREATE TABLE example (

&#x20;     code CHAR(5)

&#x20; );

&#x20; INSERT INTO example (code) VALUES ('AB'), ('ABCDE');

&#x20; -- Output: 'AB   ', 'ABCDE' (padded to 5 characters if shorter)

&#x20;

**VARCHAR**

•   Variable-length string data type.

•   More storage-efficient than CHAR for variable-length strings as it only uses as much space as needed.

•   Maximum length is 65,535 bytes, but keep in mind that UTF-8 characters may take up more than 1 byte each.

&#x20;

&#x20; CREATE TABLE example (

&#x20;     name VARCHAR(50)

&#x20; );

&#x20; INSERT INTO example (name) VALUES ('Alice'), ('Bob');

&#x20; -- Output: 'Alice', 'Bob'

&#x20;

**BINARY**

•   Fixed-length binary string.

•   Always stores exactly n bytes.

•   If the data is shorter than n, it is padded with \\0 (null bytes).

•   Similar to CHAR(n), but for binary data.

&#x20;

&#x20; CREATE TABLE test\_binary (

&#x20;     bin\_col BINARY(5)

&#x20; );

&#x20;  

&#x20; INSERT INTO test\_binary (bin\_col) VALUES ('abc');

&#x20; -- Stored as: 'abc\\0\\0'

&#x20;

**VARBINARY**

•   Variable-length binary string.

•   Stores up to n bytes.

•   Does not pad data; just stores it as-is.

&#x20;

&#x20; CREATE TABLE test\_varbinary (

&#x20;     varbin\_col VARBINARY(5)

&#x20; );

&#x20;  

&#x20; INSERT INTO test\_varbinary (varbin\_col) VALUES ('abc');

&#x20; -- Stored as: 'abc'

&#x20;

##### **CHAR vs VARCHAR**

**----------------------**

**Feature** -> CHAR(n),	VARCHAR(n)

1. **Storage Type** -> Fixed - length string,	Variable-length string
2. **Padding** -> Pads with spaces to length n,	No padding
3. **Storage Size** -> Always uses n bytes (plus 1 if needed),	Uses only actual string length (plus 1 or 2 bytes for length prefix)
4. **Performance** -> Slightly faster for fixed-length data,	More efficient for varying-length data
5. **Trailing Spaces** -> Trailing spaces are preserved/stored,	Trailing spaces are preserved but ignored in comparison
6. **Max Length** -> 255 characters,	65,535 bytes (depending on row size and character set)



##### **BINARY vs VARBINARY**

**-----------------------------**

**Feature** -> BINARY(n),	VARBINARY(n)

1. **Length** -> Fixed,	Variable
2. **Padding** -> Pads with \\0,	No padding
3. **Max length** -> Up to 255 bytes (or more in later versions),	Same
4. **Use case** -> Consistent-length binary data,	Varying-length binary data

Similar to CHAR(n), VARCHAR(n)





&#x20;

**TEXT Types, ENUM and SET**

**------------------------**



**TEXT**

•   Used for larger blocks of text, ideal for storing paragraphs or longer descriptions.

•   Can store up to 65,535 characters.

•   Cannot have a default value and is stored outside the table row, which may impact performance for frequently queried columns.

&#x20;

&#x20; CREATE TABLE example (

&#x20;     description TEXT

&#x20; );

&#x20; INSERT INTO example (description) VALUES ('This is a long description text.');

&#x20; -- Output: The full text is stored as-is.

&#x20;

**TINYTEXT, MEDIUMTEXT, LONGTEXT**

•   These are variants of the TEXT data type with different maximum storage capacities:

1. TINYTEXT: up to 255 characters.
2. MEDIUMTEXT: up to 16,777,215 characters.
3. LONGTEXT: up to 4,294,967,295 characters.

&#x20;

&#x20; CREATE TABLE example (

&#x20;     short\_text TINYTEXT,

&#x20;     medium\_text MEDIUMTEXT,

&#x20;     long\_text LONGTEXT

&#x20; );

&#x20; INSERT INTO example (short\_text, medium\_text, long\_text)

&#x20; VALUES ('Short text', 'This is a medium length text.', 'This is a very long text that can hold massive content.');

&#x20;

**ENUM**

•   Used for a predefined list of values.

•   Stores only one value chosen from the list.

•   Saves space as it internally maps each value to an integer.

&#x20;

&#x20; CREATE TABLE example (

&#x20;     status ENUM('active', 'inactive', 'pending')

&#x20; );

&#x20; INSERT INTO example (status) VALUES ('active'), ('inactive');

&#x20; -- Output: The status field accepts only one of the specified values.

&#x20;

**SET**

•   Used for a predefined list of values where multiple values can be stored.

•   Each value is stored as a bit in a set of bits, allowing for efficient storage.

&#x20;

&#x20; CREATE TABLE example (

&#x20;     permissions SET('read', 'write', 'execute')

&#x20; );

&#x20; INSERT INTO example (permissions) VALUES ('read,write'), ('write,execute');

&#x20; -- Output: The permissions field can store multiple values from the set.

&#x20;



&#x20;

**Date and Time**

**-------------**



**DATE**

•   In SQL, DATE is a data type that stores the date. It does not store time information.

•   The format of the date is, 'YYYY-MM-DD'. For instance, '2022-01-01'.

•   SQL provides several functions to handle and manipulate dates.

Create a table with DATE data type

•   In this example, the OrderDate column uses the DATE data type to store the date of the order.

&#x20;

&#x20; CREATE TABLE Orders (

&#x20;     OrderId int,

&#x20;     ProductName varchar(255),

&#x20;     OrderDate date

&#x20; );

&#x20;

Insert a date value into a table

•   This command inserts a new row into the Orders table with a date.

&#x20;

&#x20; INSERT INTO Orders (OrderId, ProductName, OrderDate)

&#x20; VALUES (1, 'Product 1', '2022-01-01');

&#x20;

Retrieve data with a specific date

•   This command retrieves all orders made on January 1, 2022.

&#x20;

&#x20; SELECT \* FROM Orders

&#x20; WHERE OrderDate = '2022-01-01';

&#x20;

**Date Functions**

•   In SQL, the Date-Time data type is used to work with dates and times.

•   SQL Server comes with numerous functions for processing dates and times.

•   Some of these include:

1. CURDATE()
2. DATE\_ADD()
3. DATE\_SUB()
4. DATEDIFF()



**CURRENT\_DATE()**

•   Returns the current date.

&#x20;

&#x20; SELECT CURDATE();

&#x20;

**DATEADD() \& DATESUB()**

•   Add or subtract a specified time interval from a date.

&#x20;

&#x20; SELECT DATE\_ADD('2024-01-09', INTERVAL 3 MONTHS)

&#x20; SELECT DATE\_SUB('2024-01-09', INTERVAL 3 MONTHS)

&#x20;

**DATEDIFF()**

•   Get the difference between two dates.

&#x20;

&#x20; SELECT DATEDIFF('2024-01-09', '2024-01-14')

&#x20;

**TIME**

•   In SQL, TIME data type is used to store time values in the database.

•   It allows you to store hours, minutes, and seconds.

•   The format of a TIME is 'HH:MI:SS'.

Syntax

&#x20;

&#x20; CREATE TABLE table\_name (

&#x20;     column\_name TIME

&#x20; );

&#x20;

Inserting Data

•   This command inserts a new row into the Orders table with a TIME.

Syntax

&#x20;

&#x20; INSERT INTO table\_name (column\_name) values ('17:34:20');

&#x20;

**Time Functions**

•   SQL provides several functions to work with the TIME data type. Some of them include:

1. CURTIME()
2. ADDTIME()
3. SUBTIME()



**CURTIME()**

•   Returns the current Time

&#x20;

&#x20; SELECT CURTIME();

&#x20;

**ADDTIME() \& SUBTIME()**

•   Add and Subtract time values

&#x20;

&#x20; SELECT ADDTIME('11:30:45', '15:30:45')

&#x20; SELECT SUBTIME('11:30:45', '15:30:45')

&#x20;

**TIMESTAMP**

•   SQL TIMESTAMP is a data type that allows you to store both date and time.

•   It is typically used to track updates and changes made to a record, providing a chronological time of happenings.

•   The format is as follows: 'YYYY-MM-DD HH:MI:SS'

Creating Table

Basic TIMESTAMP column:

&#x20;

&#x20; CREATE TABLE table\_name (

&#x20;     column1 TIMESTAMP,

&#x20;     column2 VARCHAR(100),

&#x20;     ...

&#x20; );

&#x20;

With a default value of the current timestamp:

&#x20;

&#x20; CREATE TABLE table\_name (

&#x20;     column1 TIMESTAMP DEFAULT CURRENT\_TIMESTAMP,

&#x20;     column2 VARCHAR(100),

&#x20;     ...

&#x20; );

&#x20;

**UPDATE CURRENT\_TIMESTAMP**

•   In MySQL, ON UPDATE CURRENT\_TIMESTAMP can be used to automatically update the TIMESTAMP field to the current date and time whenever there is any change in other fields of the row.

&#x20;

&#x20; CREATE TABLE table\_name (

&#x20;     column1 TIMESTAMP DEFAULT CURRENT\_TIMESTAMP ON UPDATE CURRENT\_TIMESTAMP,

&#x20;     column2 VARCHAR(100),

&#x20;     ...

&#x20; );

&#x20;



mysql> show databases;

+------------------------+

| Database               |

+------------------------+

| information\_schema     |

| jeevan\_raksha\_pharmacy |

| mysql                  |

| performance\_schema     |

| sys                    |

+------------------------+

5 rows in set (0.08 sec)



mysql> CREATE DATABASE PFS7;

Query OK, 1 row affected (0.06 sec)



mysql> SHOW DATABASES;

+------------------------+

| Database               |

+------------------------+

| information\_schema     |

| jeevan\_raksha\_pharmacy |

| mysql                  |

| performance\_schema     |

| pfs3                   |

| sys                    |

+------------------------+

6 rows in set (0.00 sec)



mysql> USE PFS7;

Database changed

mysql> CREATE TABLE EMPLOYEES(

&#x20;   -> EMPID CHAR(5),

&#x20;   -> FNAME VARCHAR(100),

&#x20;   -> LNAME VARCHAR(30),

&#x20;   -> AGE INT,

&#x20;   -> DOJ DATE,

&#x20;   -> ADDRESS TINYTEXT,

&#x20;   -> DEPT VARCHAR(20)

&#x20;   -> );

Query OK, 0 rows affected (0.27 sec)





