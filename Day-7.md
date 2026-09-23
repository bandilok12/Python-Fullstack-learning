

**What is an operator ?**

\----------------

operator is a symbol that performs a specific task.



syntax

\-------

operand  operator  operand

a         +           b





**MySQL Operators and Their Usage**

**===============================**



**What are Operators?**

Operators are special symbols or keywords used in MySQL to perform operations on data. They help in calculations, comparing values, filtering records, combining conditions, manipulating strings, and performing bitwise operations.



**Types of Operators**

1. Arithmetic Operators
2. Comparison Operators
3. Assignment Operators
4. Logical Operators
5. String Operators
6. Bitwise Operators
7. NULL Operators
8. Special Operators



1\. Arithmetic Operators

Definition

Arithmetic operators are used to perform mathematical calculations on numeric values.

Operator

Description

Example

Result

\+

Addition

10 + 5

15

\-

Subtraction

10 - 5

5

\*

Multiplication

10 \* 5

50

/

Division

10 / 5

2

%

Modulus (Remainder)

10 % 3

1







STEP 1: Create Table

CREATE TABLE Products (

&#x20;id INT,

&#x20;name VARCHAR(100),

&#x20;price DECIMAL(10,2),

&#x20;qty INT

&#x20;);



STEP 2: Insert Records

INSERT INTO Products VALUES

&#x20;(1, 'Pen', 10.00, 100),

&#x20;(2, 'Notebook', 25.00, 50),

&#x20;(3, 'Pencil', 5.00, 200),

&#x20;(4, 'Eraser', 3.00, 300),

&#x20;(5, 'Marker', 15.00, 80),

&#x20;(6, 'Scale', 20.00, 150),

&#x20;(7, 'Sharpener', 8.00, 120),

&#x20;(8, 'Geometry Box', 120.00, 40),

&#x20;(9, 'Sketch Pen', 60.00, 75),

&#x20;(10, 'Crayons', 90.00, 55);



SELECT Queries

Q1. Calculate the price after adding 12% GST.

SELECT name, price, price + (price \* 0.12) AS price\_with\_tax

&#x20;FROM Products;



Q2. Calculate the discounted price after reducing ₹5.

SELECT name, price, price - 5 AS discounted\_price

&#x20;FROM Products;



Q3. Find the total inventory value of each product.

SELECT name, price, qty, price \* qty AS total\_inventory\_value

&#x20;FROM Products;



Q4. Calculate the cost of purchasing 10 units.

SELECT name, price, price \* 10 AS price\_for\_10\_units

&#x20;FROM Products;



Q5. Display products whose quantity is not divisible by 50.

SELECT \*

&#x20;FROM Products

&#x20;WHERE qty % 50 <> 0;



Q6. Add ₹20 to the price of every product.

SELECT name, price, price + 20 AS increased\_price

&#x20;FROM Products;



Q7. Display half of each product's quantity.

SELECT name, qty, qty / 2 AS half\_quantity

&#x20;FROM Products;



Q8. Display double the quantity of every product.

SELECT name, qty, qty \* 2 AS double\_quantity

&#x20;FROM Products;



Q9. Find the remaining quantity after selling 10 units.

SELECT name, qty, qty - 10 AS remaining\_quantity

&#x20;FROM Products;



Q10. Divide the price equally among 5 people.

SELECT name, price, price / 5 AS share\_price

&#x20;FROM Products;



Q11. Display products whose price is an even number.

SELECT \*

&#x20;FROM Products

&#x20;WHERE price % 2 = 0;



Q12. Display products whose quantity is divisible by 5.

SELECT \*

&#x20;FROM Products

&#x20;WHERE qty % 5 = 0;



Q13. Calculate the price after giving a 10% discount.

SELECT name, price, price - (price \* 0.10) AS discounted\_price

&#x20;FROM Products;



Q14. Calculate the price after adding ₹15 and then 18% GST.

SELECT name, price, (price + 15) \* 1.18 AS final\_price

&#x20;FROM Products;



Q15. Display the remaining quantity after selling half the stock.

SELECT name, qty, qty - (qty / 2) AS remaining\_stock

&#x20;FROM Products;



UPDATE Queries

Q1. Add 2 units to every product.

UPDATE Products

&#x20;SET qty = qty + 2;



Q2. Reduce the price of every product by ₹5.

UPDATE Products

&#x20;SET price = price - 5;



Q3. Double the quantity of Eraser.

UPDATE Products

&#x20;SET qty = qty \* 2

&#x20;WHERE name = 'Eraser';



Q4. Reduce the quantity of Marker to half.

UPDATE Products

&#x20;SET qty = qty / 2

&#x20;WHERE name = 'Marker';



Q5. Increase the price of Notebook by ₹20.

UPDATE Products

&#x20;SET price = price + 20

&#x20;WHERE name = 'Notebook';



Q6. Increase the quantity of Pen by 50.

UPDATE Products

&#x20;SET qty = qty + 50

&#x20;WHERE name = 'Pen';



Q7. Reduce the quantity of Pencils by 25.

UPDATE Products

&#x20;SET qty = qty - 25

&#x20;WHERE name = 'Pencil';



Q8. Increase the price of Scale by 10%.

UPDATE Products

&#x20;SET price = price + (price \* 0.10)

&#x20;WHERE name = 'Scale';



Q9. Double the quantity of Sharpener.

UPDATE Products

&#x20;SET qty = qty \* 2

&#x20;WHERE name = 'Sharpener';



Q10. Reduce the price of Crayons by ₹15.

UPDATE Products

&#x20;SET price = price - 15

&#x20;WHERE name = 'Crayons';



DELETE Queries

Q1. Delete products whose quantity is less than 100.

DELETE FROM Products

&#x20;WHERE qty < 100;



Q2. Delete products whose price is less than ₹10.

DELETE FROM Products

&#x20;WHERE price < 10;



Q3. Delete the Marker record.

DELETE FROM Products

&#x20;WHERE name = 'Marker';



Q4. Delete products whose quantity is greater than 300.

DELETE FROM Products

&#x20;WHERE qty > 300;



Q5. Delete products whose price is greater than ₹100.

DELETE FROM Products

&#x20;WHERE price > 100;

This is plain text without any



Comparison Operators in MySQL

What are Comparison Operators?

Comparison Operators are used to compare two values or expressions. They return TRUE (1) or FALSE (0) based on whether the comparison condition is satisfied.

These operators are mainly used with the WHERE clause to filter records.



Types of Comparison Operators

Operator

Description

Example

=

Equal to

salary = 50000

!= or <>

Not Equal to

department != 'HR'

>

Greater Than

salary > 50000

<

Less Than

age < 25

>=

Greater Than or Equal To

age >= 18

<=

Less Than or Equal To

salary <= 40000



Note: In MySQL, both != and <> represent Not Equal To.





STEP 1: Create Table

CREATE TABLE StudentScores (

&#x20;id INT,

&#x20;name VARCHAR(100),

&#x20;subject VARCHAR(50),

&#x20;marks INT

&#x20;);



STEP 2: Insert Records

INSERT INTO StudentScores VALUES

&#x20;(1, 'Alice', 'Math', 95),

&#x20;(2, 'Bob', 'Math', 76),

&#x20;(3, 'Charlie', 'Math', 59),

&#x20;(4, 'Diana', 'Math', 88),

&#x20;(5, 'Eve', 'Math', 40),

&#x20;(6, 'Frank', 'Math', 95),

&#x20;(7, 'Grace', 'Science', 67),

&#x20;(8, 'Henry', 'Science', 82),

&#x20;(9, 'Ivy', 'English', 91),

&#x20;(10, 'Jack', 'English', 55),

&#x20;(11, 'Kevin', 'Math', 73),

&#x20;(12, 'Lily', 'Science', 48),

&#x20;(13, 'Mia', 'English', 100),

&#x20;(14, 'Noah', 'Math', 64),

&#x20;(15, 'Olivia', 'Science', 79);



SELECT Queries

Q1. Display students who scored more than 80.

SELECT \*

&#x20;FROM StudentScores

&#x20;WHERE marks > 80;



Q2. Display students who scored 60 or more.

SELECT \*

&#x20;FROM StudentScores

&#x20;WHERE marks >= 60;



Q3. Display students who scored less than 50.

SELECT \*

&#x20;FROM StudentScores

&#x20;WHERE marks < 50;



Q4. Display students who scored exactly 95.

SELECT \*

&#x20;FROM StudentScores

&#x20;WHERE marks = 95;



Q5. Display students who did not score 95.

SELECT \*

&#x20;FROM StudentScores

&#x20;WHERE marks != 95;



Q6. Display students who scored 60 or less.

SELECT \*

&#x20;FROM StudentScores

&#x20;WHERE marks <= 60;



Q7. Display students who scored more than 70.

SELECT \*

&#x20;FROM StudentScores

&#x20;WHERE marks > 70;



Q8. Display students who scored less than or equal to 75.

SELECT \*

&#x20;FROM StudentScores

&#x20;WHERE marks <= 75;



Q9. Display students who scored exactly 100.

SELECT \*

&#x20;FROM StudentScores

&#x20;WHERE marks = 100;



Q10. Display students who did not score 40.

SELECT \*

&#x20;FROM StudentScores

&#x20;WHERE marks <> 40;



Q11. Display students who scored more than or equal to 90.

SELECT \*

&#x20;FROM StudentScores

&#x20;WHERE marks >= 90;



Q12. Display students who scored less than 65.

SELECT \*

&#x20;FROM StudentScores

&#x20;WHERE marks < 65;



UPDATE Queries

Q1. Increase marks by 10 for students scoring below 50.

UPDATE StudentScores

&#x20;SET marks = marks + 10

&#x20;WHERE marks < 50;



Q2. Increase marks by 5 for students scoring 60 or below.

UPDATE StudentScores

&#x20;SET marks = marks + 5

&#x20;WHERE marks <= 60;



Q3. Add 2 bonus marks to students scoring above 90.

UPDATE StudentScores

&#x20;SET marks = marks + 2

&#x20;WHERE marks > 90;



Q4. Add 3 bonus marks to students scoring 80 or more.

UPDATE StudentScores

&#x20;SET marks = marks + 3

&#x20;WHERE marks >= 80;



Q5. Reduce 1 mark for students who did not score exactly 95.

UPDATE StudentScores

&#x20;SET marks = marks - 1

&#x20;WHERE marks != 95;



Q6. Set marks to 100 for students who scored exactly 95.

UPDATE StudentScores

&#x20;SET marks = 100

&#x20;WHERE marks = 95;



Q7. Increase marks by 15 for students scoring below 60.

UPDATE StudentScores

&#x20;SET marks = marks + 15

&#x20;WHERE marks < 60;



Q8. Add 5 marks for students scoring above 75.

UPDATE StudentScores

&#x20;SET marks = marks + 5

&#x20;WHERE marks > 75;



Q9. Reduce 3 marks for students scoring above 95.

UPDATE StudentScores

&#x20;SET marks = marks - 3

&#x20;WHERE marks > 95;



Q10. Set marks to 75 for students scoring below 50.

UPDATE StudentScores

&#x20;SET marks = 75

&#x20;WHERE marks < 50;



Q11. Increase marks by 8 for students scoring exactly 64.

UPDATE StudentScores

&#x20;SET marks = marks + 8

&#x20;WHERE marks = 64;



Q12. Reduce 5 marks for students scoring 100.

UPDATE StudentScores

&#x20;SET marks = marks - 5

&#x20;WHERE marks = 100;



DELETE Queries

Q1. Delete students who scored below 50.

DELETE FROM StudentScores

&#x20;WHERE marks < 50;



Q2. Delete students who scored 60 or below.

DELETE FROM StudentScores

&#x20;WHERE marks <= 60;



Q3. Delete students who scored above 90.

DELETE FROM StudentScores

&#x20;WHERE marks > 90;



Q4. Delete students who scored 80 or more.

DELETE FROM StudentScores

&#x20;WHERE marks >= 80;



Q5. Delete students whose marks are not equal to 95.

DELETE FROM StudentScores

&#x20;WHERE marks != 95;



Q6. Delete students who scored exactly 76.

DELETE FROM StudentScores

&#x20;WHERE marks = 76;



Q7. Delete students who scored exactly 100.

DELETE FROM StudentScores

&#x20;WHERE marks = 100;



Q8. Delete students who scored less than 65.

DELETE FROM StudentScores

&#x20;WHERE marks < 65;



Q9. Delete students who scored greater than or equal to 90.

DELETE FROM StudentScores

&#x20;WHERE marks >= 90;



Q10. Delete students who scored exactly 73.

DELETE FROM StudentScores

&#x20;WHERE marks = 73;



Q11. Delete students who scored exactly 48.

DELETE FROM StudentScores

&#x20;WHERE marks = 48;



Q12. Delete students who scored between 70 and 80 (using comparison operators).

DELETE FROM StudentScores

&#x20;WHERE marks >= 70 AND marks <= 80;



Logical Operators in MySQL

What are Logical Operators?

Logical Operators are used to combine multiple conditions in a SQL query. They help filter data based on one or more conditions and are commonly used with the WHERE clause.

Types of Logical Operators

AND – Returns records only if all conditions are TRUE.

OR – Returns records if at least one condition is TRUE.

NOT – Reverses the result of a condition (TRUE becomes FALSE and vice versa).



STEP 1: Create Table

STEP 1: Create Table

CREATE TABLE Employees (

&#x20;id INT,

&#x20;name VARCHAR(100),

&#x20;department VARCHAR(100),

&#x20;salary INT,

&#x20;isactive BOOLEAN

&#x20;);



STEP 2: Insert Records

INSERT INTO Employees VALUES

&#x20;(1, 'Rahul Sharma', 'IT', 50000, TRUE),

&#x20;(2, 'Priya Reddy', 'HR', 30000, TRUE),

&#x20;(3, 'Amit Kumar', 'Finance', 45000, FALSE),

&#x20;(4, 'Sneha Patel', 'IT', 35000, TRUE),

&#x20;(5, 'Vikram Singh', 'Finance', 28000, TRUE),

&#x20;(6, 'Anjali Mehta', 'HR', 32000, FALSE),

&#x20;(7, 'Kiran Rao', 'IT', 60000, TRUE),

&#x20;(8, 'Pooja Verma', 'Marketing', 27000, TRUE),

&#x20;(9, 'Ramesh Naidu', 'Sales', 38000, TRUE),

&#x20;(10, 'Deepika Joshi', 'Finance', 52000, TRUE),

&#x20;(11, 'Suresh Babu', 'Marketing', 29000, FALSE),

&#x20;(12, 'Neha Kapoor', 'HR', 41000, TRUE),

&#x20;(13, 'Arjun Reddy', 'IT', 55000, FALSE),

&#x20;(14, 'Lakshmi Devi', 'Sales', 33000, TRUE),

&#x20;(15, 'Nikhil Jain', 'IT', 47000, TRUE);



SELECT Queries

Q1. Display IT department employees whose salary is greater than 40000.

SELECT \*

&#x20;FROM Employees

&#x20;WHERE department = 'IT' AND salary > 40000;



Q2. Display employees who belong to the HR department or whose salary is less than 35000.

SELECT \*

&#x20;FROM Employees

&#x20;WHERE department = 'HR' OR salary < 35000;



Q3. Display employees who are not in the HR department.

SELECT \*

&#x20;FROM Employees

&#x20;WHERE department != 'HR';



Q4. Display employees whose department is Finance or whose salary is greater than 30000 and are active.

SELECT \*

&#x20;FROM Employees

&#x20;WHERE department = 'Finance'

&#x20;OR (salary > 30000 AND isactive = TRUE);



Q5. Display active IT employees.

SELECT \*

&#x20;FROM Employees

&#x20;WHERE department = 'IT' AND isactive = TRUE;



Q6. Display inactive employees or employees earning less than 30000.

SELECT \*

&#x20;FROM Employees

&#x20;WHERE isactive = FALSE OR salary < 30000;



Q7. Display Marketing employees with salary greater than 25000.

SELECT \*

&#x20;FROM Employees

&#x20;WHERE department = 'Marketing' AND salary > 25000;



Q8. Display employees who are not in the Finance department.

SELECT \*

&#x20;FROM Employees

&#x20;WHERE department != 'Finance';



Q9. Display active employees earning more than 50000.

SELECT \*

&#x20;FROM Employees

&#x20;WHERE salary > 50000 AND isactive = TRUE;



Q10. Display employees from Sales or HR departments.

SELECT \*

&#x20;FROM Employees

&#x20;WHERE department = 'Sales' OR department = 'HR';



Q11. Display employees who are inactive and belong to the IT department.

SELECT \*

&#x20;FROM Employees

&#x20;WHERE department = 'IT' AND isactive = FALSE;



Q12. Display employees whose salary is less than 40000 and are active.

SELECT \*

&#x20;FROM Employees

&#x20;WHERE salary < 40000 AND isactive = TRUE;



UPDATE Queries

Q1. Increase salary by 2000 for active IT employees earning less than 60000.

UPDATE Employees

&#x20;SET salary = salary + 2000

&#x20;WHERE department = 'IT'

&#x20;AND isactive = TRUE

&#x20;AND salary < 60000;



Q2. Reduce salary by 10% for Finance department employees or inactive employees.

UPDATE Employees

&#x20;SET salary = salary - (salary \* 0.10)

&#x20;WHERE department = 'Finance'

&#x20;OR isactive = FALSE;



Q3. Make all non-IT employees inactive.

UPDATE Employees

&#x20;SET isactive = FALSE

&#x20;WHERE department != 'IT';



Q4. Increase salary by 3000 for active HR employees.

UPDATE Employees

&#x20;SET salary = salary + 3000

&#x20;WHERE department = 'HR'

&#x20;AND isactive = TRUE;



Q5. Increase salary by 5000 for Sales employees earning less than 40000.

UPDATE Employees

&#x20;SET salary = salary + 5000

&#x20;WHERE department = 'Sales'

&#x20;AND salary < 40000;



Q6. Activate all inactive Marketing employees.

UPDATE Employees

&#x20;SET isactive = TRUE

&#x20;WHERE department = 'Marketing'

&#x20;AND isactive = FALSE;



Q7. Reduce salary by 2000 for inactive employees.

UPDATE Employees

&#x20;SET salary = salary - 2000

&#x20;WHERE isactive = FALSE;



Q8. Increase salary by 15% for active employees earning more than 50000.

UPDATE Employees

&#x20;SET salary = salary + (salary \* 0.15)

&#x20;WHERE salary > 50000

&#x20;AND isactive = TRUE;



Q9. Make all Finance employees active.

UPDATE Employees

&#x20;SET isactive = TRUE

&#x20;WHERE department = 'Finance';



Q10. Increase salary by 1000 for IT or Sales employees.

UPDATE Employees

&#x20;SET salary = salary + 1000

&#x20;WHERE department = 'IT'

&#x20;OR department = 'Sales';



DELETE Queries

Q1. Delete inactive employees from the HR department.

DELETE FROM Employees

&#x20;WHERE department = 'HR'

&#x20;AND isactive = FALSE;



Q2. Delete employees from Finance or employees earning less than 35000.

DELETE FROM Employees

&#x20;WHERE department = 'Finance'

&#x20;OR salary < 35000;



Q3. Delete employees who are not in the IT department.

DELETE FROM Employees

&#x20;WHERE department != 'IT';



Q4. Delete inactive employees.

DELETE FROM Employees

&#x20;WHERE isactive = FALSE;



Q5. Delete Marketing employees with salary less than 30000.

DELETE FROM Employees

&#x20;WHERE department = 'Marketing'

&#x20;AND salary < 30000;



Q6. Delete Sales employees or inactive employees.

DELETE FROM Employees

&#x20;WHERE department = 'Sales'

&#x20;OR isactive = FALSE;



Q7. Delete active employees earning more than 55000.

DELETE FROM Employees

&#x20;WHERE isactive = TRUE

&#x20;AND salary > 55000;



Q8. Delete employees who are not in the IT or HR departments.

DELETE FROM Employees

&#x20;WHERE department != 'IT'

&#x20;AND department != 'HR';



Q9. Delete employees whose salary is below 30000 and are inactive.

DELETE FROM Employees

&#x20;WHERE salary < 30000

&#x20;AND isactive = FALSE;



Q10. Delete employees from the Marketing department or whose salary is greater than 50000.

DELETE FROM Employees

&#x20;WHERE department = 'Marketing'

&#x20;OR salary > 50000;

NULL Operator

What are NULL Operators?

NULL Operators are used to check whether a column contains a NULL value (missing or unknown data).

Note: NULL is not the same as 0 (zero) or an empty string (''). It represents the absence of a value.

MySQL provides two NULL operators:

IS NULL – Checks whether a column contains a NULL value.

IS NOT NULL – Checks whether a column contains a non-NULL value.



STEP 1: Create Table

CREATE TABLE Projects (

&#x20;id INT,

&#x20;name VARCHAR(100),

&#x20;assignedto VARCHAR(100),

&#x20;start DATE,

&#x20;end DATE

&#x20;);



STEP 2: Insert Records

INSERT INTO Projects VALUES

&#x20;(1, 'Website Revamp', 'Alice', '2024-01-15', '2024-03-01'),

&#x20;(2, 'Mobile App', 'Bob', '2024-02-01', NULL),

&#x20;(3, 'Data Migration', NULL, NULL, NULL),

&#x20;(4, 'SEO Optimization', 'Eve', '2024-03-10', '2024-04-20'),

&#x20;(5, 'Cloud Migration', NULL, '2024-03-15', NULL),

&#x20;(6, 'ERP Development', 'John', '2024-04-01', NULL),

&#x20;(7, 'CRM Upgrade', NULL, NULL, NULL),

&#x20;(8, 'Inventory System', 'David', '2024-05-10', '2024-06-25'),

&#x20;(9, 'Online Portal', 'Sophia', '2024-06-15', NULL),

&#x20;(10, 'Security Audit', NULL, '2024-07-01', NULL),

&#x20;(11, 'AI Chatbot', 'James', NULL, NULL),

&#x20;(12, 'Payroll System', 'Emma', '2024-08-01', '2024-09-10'),

&#x20;(13, 'Hospital Management', NULL, NULL, NULL),

&#x20;(14, 'Student Portal', 'Michael', '2024-09-05', NULL),

&#x20;(15, 'Banking Application', NULL, '2024-10-01', NULL);



SELECT Queries

Q1. Display all projects that are not assigned to anyone.

SELECT \*

&#x20;FROM Projects

&#x20;WHERE assignedto IS NULL;



Q2. Display projects that have not started yet.

SELECT \*

&#x20;FROM Projects

&#x20;WHERE start IS NULL;



Q3. Display all completed projects.

SELECT \*

&#x20;FROM Projects

&#x20;WHERE end IS NOT NULL;



Q4. Display all projects with an assigned employee.

SELECT \*

&#x20;FROM Projects

&#x20;WHERE assignedto IS NOT NULL;



Q5. Display projects that have not yet been completed.

SELECT \*

&#x20;FROM Projects

&#x20;WHERE end IS NULL;



Q6. Display projects that have both a start date and an end date.

SELECT \*

&#x20;FROM Projects

&#x20;WHERE start IS NOT NULL

&#x20;AND end IS NOT NULL;



Q7. Display projects where both assigned employee and start date are NULL.

SELECT \*

&#x20;FROM Projects

&#x20;WHERE assignedto IS NULL

&#x20;AND start IS NULL;



Q8. Display projects that have a start date but no end date.

SELECT \*

&#x20;FROM Projects

&#x20;WHERE start IS NOT NULL

&#x20;AND end IS NULL;



Q9. Display projects whose assigned employee is available.

SELECT id, name, assignedto

&#x20;FROM Projects

&#x20;WHERE assignedto IS NOT NULL;



Q10. Display projects with all NULL values in start and end dates.

SELECT \*

&#x20;FROM Projects

&#x20;WHERE start IS NULL

&#x20;AND end IS NULL;



UPDATE Queries

Q1. Assign all unassigned projects to Frank.

UPDATE Projects

&#x20;SET assignedto = 'Frank'

&#x20;WHERE assignedto IS NULL;



Q2. Update today's date as the start date for projects that have not started.

UPDATE Projects

&#x20;SET start = CURDATE()

&#x20;WHERE start IS NULL;



Q3. Rename all completed projects as 'Completed'.

UPDATE Projects

&#x20;SET name = 'Completed'

&#x20;WHERE end IS NOT NULL;



Q4. Set today's date as the end date for projects that have no end date.

UPDATE Projects

&#x20;SET end = CURDATE()

&#x20;WHERE end IS NULL;



Q5. Assign 'Admin' to projects without an assigned employee.

UPDATE Projects

&#x20;SET assignedto = 'Admin'

&#x20;WHERE assignedto IS NULL;



Q6. Rename projects without a start date as 'Pending Project'.

UPDATE Projects

&#x20;SET name = 'Pending Project'

&#x20;WHERE start IS NULL;



Q7. Assign 'Manager' to projects having both start and end dates.

UPDATE Projects

&#x20;SET assignedto = 'Manager'

&#x20;WHERE start IS NOT NULL

&#x20;AND end IS NOT NULL;



Q8. Change the project name to 'In Progress' for projects with a start date but no end date.

UPDATE Projects

&#x20;SET name = 'In Progress'

&#x20;WHERE start IS NOT NULL

&#x20;AND end IS NULL;



Q9. Set the start date to '2024-12-01' for projects with NULL start date.

UPDATE Projects

&#x20;SET start = '2024-12-01'

&#x20;WHERE start IS NULL;



Q10. Set the end date to '2025-01-31' for projects with NULL end date.

UPDATE Projects

&#x20;SET end = '2025-01-31'

&#x20;WHERE end IS NULL;



DELETE Queries

Q1. Delete all unassigned projects.

DELETE FROM Projects

&#x20;WHERE assignedto IS NULL;



Q2. Delete projects that have not started.

DELETE FROM Projects

&#x20;WHERE start IS NULL;



Q3. Delete all completed projects.

DELETE FROM Projects

&#x20;WHERE end IS NOT NULL;



Q4. Delete projects that do not have an end date.

DELETE FROM Projects

&#x20;WHERE end IS NULL;



Q5. Delete projects where both assigned employee and start date are NULL.

DELETE FROM Projects

&#x20;WHERE assignedto IS NULL

&#x20;AND start IS NULL;



Q6. Delete projects with no assigned employee and no end date.

DELETE FROM Projects

&#x20;WHERE assignedto IS NULL

&#x20;AND end IS NULL;



Q7. Delete projects that have both start and end dates.

DELETE FROM Projects

&#x20;WHERE start IS NOT NULL

&#x20;AND end IS NOT NULL;



Q8. Delete projects that have a start date but no end date.

DELETE FROM Projects

&#x20;WHERE start IS NOT NULL

&#x20;AND end IS NULL;



Q9. Delete projects assigned to Frank.

DELETE FROM Projects

&#x20;WHERE assignedto = 'Frank';



Q10. Delete projects named 'Completed'.

DELETE FROM Projects

&#x20;WHERE name = 'Completed';













