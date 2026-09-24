#### **Other Operators** 

**=============================**



MySQL offers various additional operators for specific purposes.

BETWEEN: Checks if a value falls within a specific range.

IN: Checks if a value is present within a list of specified values.

CASE: Used for conditional expressions and assigning values based on conditions 



###### **BETWEEN Operator**

**--------------------**



SELECT \*

FROM orders

WHERE order\_date BETWEEN '2024-03-15' AND '2024-03-20';



±This retrieves all orders placed between March 15th, 2024 (inclusive) and March 20th, 2024 (inclusive).



±BETWEEN: 

Checks if a value falls within a specific range.

STEP 1: Create Table

CREATE TABLE Orders (

&#x20;id INT,

&#x20;customer\_name VARCHAR(100),

&#x20;order\_date DATE,

&#x20;total\_amount DECIMAL(10,2)

&#x20;);



STEP 2: Insert Records

INSERT INTO Orders VALUES

&#x20;(1, 'Alice', '2024-03-01', 1500.00),

&#x20;(2, 'Bob', '2024-03-05', 450.00),

&#x20;(3, 'Charlie', '2024-03-10', 2500.00),

&#x20;(4, 'Diana', '2024-03-15', 800.00),

&#x20;(5, 'Eve', '2024-03-20', 1200.00),

&#x20;(6, 'Frank', '2024-03-25', 3000.00),

&#x20;(7, 'Grace', '2024-04-02', 1800.00),

&#x20;(8, 'Henry', '2024-04-08', 950.00),

&#x20;(9, 'Ivy', '2024-04-12', 2750.00),

&#x20;(10, 'Jack', '2024-04-18', 650.00),

&#x20;(11, 'Kevin', '2024-04-22', 4200.00),

&#x20;(12, 'Lily', '2024-05-01', 1350.00),

&#x20;(13, 'Michael', '2024-05-08', 5000.00),

&#x20;(14, 'Nancy', '2024-05-15', 2250.00),

&#x20;(15, 'Oliver', '2024-05-25', 900.00);



SELECT Queries

Q1. Display orders placed between '2024-03-03' and '2024-03-10'.

SELECT \*

&#x20;FROM Orders

&#x20;WHERE order\_date BETWEEN '2024-03-03' AND '2024-03-10';



Q2. Display orders placed between '2024-04-01' and '2024-04-30'.

SELECT \*

&#x20;FROM Orders

&#x20;WHERE order\_date BETWEEN '2024-04-01' AND '2024-04-30';



Q3. Display orders whose total amount is between 1000 and 3000.

SELECT \*

&#x20;FROM Orders

&#x20;WHERE total\_amount BETWEEN 1000 AND 3000;



Q4. Display orders whose total amount is between 500 and 1500.

SELECT \*

&#x20;FROM Orders

&#x20;WHERE total\_amount BETWEEN 500 AND 1500;



Q5. Display orders placed between '2024-05-01' and '2024-05-31'.

SELECT \*

&#x20;FROM Orders

&#x20;WHERE order\_date BETWEEN '2024-05-01' AND '2024-05-31';



Q6. Display customer names whose order amount is between 2000 and 5000.

SELECT customer\_name, total\_amount

&#x20;FROM Orders

&#x20;WHERE total\_amount BETWEEN 2000 AND 5000;



Q7. Display orders placed between '2024-03-15' and '2024-04-15'.

SELECT \*

&#x20;FROM Orders

&#x20;WHERE order\_date BETWEEN '2024-03-15' AND '2024-04-15';



Q8. Display orders whose amount is between 800 and 1800.

SELECT \*

&#x20;FROM Orders

&#x20;WHERE total\_amount BETWEEN 800 AND 1800;



Q9. Display orders placed between '2024-04-10' and '2024-05-10'.

SELECT \*

&#x20;FROM Orders

&#x20;WHERE order\_date BETWEEN '2024-04-10' AND '2024-05-10';



Q10. Display orders whose amount is between 2500 and 5000.

SELECT \*

&#x20;FROM Orders

&#x20;WHERE total\_amount BETWEEN 2500 AND 5000;



UPDATE Queries

Q1. Increase the total amount by 1000 for orders placed between '2024-03-04' and '2024-03-10'.

UPDATE Orders

&#x20;SET total\_amount = total\_amount + 1000

&#x20;WHERE order\_date BETWEEN '2024-03-04' AND '2024-03-10';



Q2. Increase the total amount by 500 for orders placed between '2024-04-01' and '2024-04-15'.

UPDATE Orders

&#x20;SET total\_amount = total\_amount + 500

&#x20;WHERE order\_date BETWEEN '2024-04-01' AND '2024-04-15';



Q3. Reduce the total amount by 200 for orders between 1000 and 2000.

UPDATE Orders

&#x20;SET total\_amount = total\_amount - 200

&#x20;WHERE total\_amount BETWEEN 1000 AND 2000;



Q4. Increase the total amount by 10% for orders between 2500 and 5000.

UPDATE Orders

&#x20;SET total\_amount = total\_amount + (total\_amount \* 0.10)

&#x20;WHERE total\_amount BETWEEN 2500 AND 5000;



Q5. Add 300 to orders placed between '2024-05-01' and '2024-05-31'.

UPDATE Orders

&#x20;SET total\_amount = total\_amount + 300

&#x20;WHERE order\_date BETWEEN '2024-05-01' AND '2024-05-31';



Q6. Reduce the total amount by 100 for orders placed between '2024-03-15' and '2024-03-31'.

UPDATE Orders

&#x20;SET total\_amount = total\_amount - 100

&#x20;WHERE order\_date BETWEEN '2024-03-15' AND '2024-03-31';



Q7. Increase the total amount by 750 for orders between 800 and 1500.

UPDATE Orders

&#x20;SET total\_amount = total\_amount + 750

&#x20;WHERE total\_amount BETWEEN 800 AND 1500;



Q8. Reduce the total amount by 500 for orders between 3000 and 5000.

UPDATE Orders

&#x20;SET total\_amount = total\_amount - 500

&#x20;WHERE total\_amount BETWEEN 3000 AND 5000;



Q9. Increase the total amount by 250 for orders placed between '2024-04-20' and '2024-05-10'.

UPDATE Orders

&#x20;SET total\_amount = total\_amount + 250

&#x20;WHERE order\_date BETWEEN '2024-04-20' AND '2024-05-10';



Q10. Add 100 to all orders placed between '2024-03-01' and '2024-05-31'.

UPDATE Orders

&#x20;SET total\_amount = total\_amount + 100

&#x20;WHERE order\_date BETWEEN '2024-03-01' AND '2024-05-31';



DELETE Queries

Q1. Delete orders placed between '2024-03-10' and '2024-03-20'.

DELETE FROM Orders

&#x20;WHERE order\_date BETWEEN '2024-03-10' AND '2024-03-20';



Q2. Delete orders placed between '2024-04-01' and '2024-04-15'.

DELETE FROM Orders

&#x20;WHERE order\_date BETWEEN '2024-04-01' AND '2024-04-15';



Q3. Delete orders whose total amount is between 500 and 1000.

DELETE FROM Orders

&#x20;WHERE total\_amount BETWEEN 500 AND 1000;



Q4. Delete orders whose total amount is between 2500 and 5000.

DELETE FROM Orders

&#x20;WHERE total\_amount BETWEEN 2500 AND 5000;



Q5. Delete orders placed between '2024-05-01' and '2024-05-31'.

DELETE FROM Orders

&#x20;WHERE order\_date BETWEEN '2024-05-01' AND '2024-05-31';



Q6. Delete orders whose total amount is between 1000 and 2000.

DELETE FROM Orders

&#x20;WHERE total\_amount BETWEEN 1000 AND 2000;



Q7. Delete orders placed between '2024-03-01' and '2024-03-05'.

DELETE FROM Orders

&#x20;WHERE order\_date BETWEEN '2024-03-01' AND '2024-03-05';



Q8. Delete orders placed between '2024-04-18' and '2024-05-08'.

DELETE FROM Orders

&#x20;WHERE order\_date BETWEEN '2024-04-18' AND '2024-05-08';



Q9. Delete orders whose total amount is between 1800 and 3000.

DELETE FROM Orders

&#x20;WHERE total\_amount BETWEEN 1800 AND 3000;



Q10. Delete orders placed between '2024-03-25' and '2024-04-08'.

DELETE FROM Orders

&#x20;WHERE order\_date BETWEEN '2024-03-25' AND '2024-04-08';



###### **IN Operator**

**---------------**



This operator checks if a value exists within a specified list of values 



SELECT \*

FROM customers

WHERE country IN ('USA', 'Canada', 'UK');

±This retrieves customer records where the country is either 'USA', 'Canada', or 'UK'.



STEP 1: Create Table

CREATE TABLE Emp (

&#x20;id INT,

&#x20;name VARCHAR(100),

&#x20;dept VARCHAR(20),

&#x20;salary INT

&#x20;);



STEP 2: Insert Records

INSERT INTO Emp VALUES

&#x20;(1, 'Rahul', 'IT', 50000),

&#x20;(2, 'Ramesh', 'HR', 35000),

&#x20;(3, 'Karan', 'Finance', 45000),

&#x20;(4, 'Mahesh', 'Marketing', 40000),

&#x20;(5, 'Suresh', 'IT', 55000),

&#x20;(6, 'Arjun', 'Sales', 38000),

&#x20;(7, 'Manish', 'Admin', 42000),

&#x20;(8, 'Ganesh', 'Finance', 47000),

&#x20;(9, 'Naresh', 'HR', 39000),

&#x20;(10, 'Rohan', 'IT', 52000),

&#x20;(11, 'Mohan', 'Sales', 41000),

&#x20;(12, 'Kishan', 'Marketing', 43000),

&#x20;(13, 'Dinesh', 'Admin', 46000),

&#x20;(14, 'Rajesh', 'Finance', 51000),

&#x20;(15, 'Kiran', 'IT', 48000);





SELECT Queries

Q1. Display employees from the IT and Finance departments.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE dept IN ('IT', 'Finance');



Q2. Display employees from the HR and Sales departments.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE dept IN ('HR', 'Sales');



Q3. Display employees from the Marketing and Admin departments.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE dept IN ('Marketing', 'Admin');



Q4. Display employees from the HR, IT, and Finance departments.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE dept IN ('HR', 'IT', 'Finance');



Q5. Display employees whose salary is 35000, 42000, or 60000.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE salary IN (35000, 42000, 60000);



Q6. Display employees from the Sales, Marketing, and Finance departments.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE dept IN ('Sales', 'Marketing', 'Finance');



Q7. Display employees from the Admin department.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE dept IN ('Admin');



Q8. Display employees whose salary is 39000, 43000, or 52000.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE salary IN (39000, 43000, 52000);



Q9. Display employees from the IT, Admin, and Sales departments.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE dept IN ('IT', 'Admin', 'Sales');



Q10. Display employees whose salary is 40000, 45000, or 50000.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE salary IN (40000, 45000, 50000);



UPDATE Queries

Q1. Increase salary by 2000 for employees in the HR or Marketing departments.

UPDATE Emp

&#x20;SET salary = salary + 2000

&#x20;WHERE dept IN ('HR', 'Marketing');



Q2. Increase salary by 3000 for employees in the IT and Finance departments.

UPDATE Emp

&#x20;SET salary = salary + 3000

&#x20;WHERE dept IN ('IT', 'Finance');



Q3. Increase salary by 1500 for employees in the Sales and Admin departments.

UPDATE Emp

&#x20;SET salary = salary + 1500

&#x20;WHERE dept IN ('Sales', 'Admin');



Q4. Increase salary by 5000 for employees earning 35000, 39000, or 43000.

UPDATE Emp

&#x20;SET salary = salary + 5000

&#x20;WHERE salary IN (35000, 39000, 43000);



Q5. Increase salary by 1000 for employees in the HR, IT, and Sales departments.

UPDATE Emp

&#x20;SET salary = salary + 1000

&#x20;WHERE dept IN ('HR', 'IT', 'Sales');



Q6. Increase salary by 2500 for employees earning 45000, 48000, or 52000.

UPDATE Emp

&#x20;SET salary = salary + 2500

&#x20;WHERE salary IN (45000, 48000, 52000);



Q7. Increase salary by 4000 for employees in the Admin department.

UPDATE Emp

&#x20;SET salary = salary + 4000

&#x20;WHERE dept IN ('Admin');



Q8. Increase salary by 3500 for employees in the Marketing and Finance departments.

UPDATE Emp

&#x20;SET salary = salary + 3500

&#x20;WHERE dept IN ('Marketing', 'Finance');



Q9. Increase salary by 500 for employees earning 40000, 41000, or 42000.

UPDATE Emp

&#x20;SET salary = salary + 500

&#x20;WHERE salary IN (40000, 41000, 42000);



Q10. Increase salary by 2000 for employees in the IT, Sales, and Admin departments.

UPDATE Emp

&#x20;SET salary = salary + 2000

&#x20;WHERE dept IN ('IT', 'Sales', 'Admin');



DELETE Queries

Q1. Delete employees from the Finance or Marketing departments.

DELETE FROM Emp

&#x20;WHERE dept IN ('Finance', 'Marketing');



Q2. Delete employees from the HR department.

DELETE FROM Emp

&#x20;WHERE dept IN ('HR');



Q3. Delete employees from the Sales and Admin departments.

DELETE FROM Emp

&#x20;WHERE dept IN ('Sales', 'Admin');



Q4. Delete employees whose salary is 35000, 39000, or 43000.

DELETE FROM Emp

&#x20;WHERE salary IN (35000, 39000, 43000);



Q5. Delete employees from the IT department.

DELETE FROM Emp

&#x20;WHERE dept IN ('IT');



Q6. Delete employees whose salary is 45000, 50000, or 55000.

DELETE FROM Emp

&#x20;WHERE salary IN (45000, 50000, 55000);



Q7. Delete employees from the Marketing and HR departments.

DELETE FROM Emp

&#x20;WHERE dept IN ('Marketing', 'HR');



Q8. Delete employees from the Admin department.

DELETE FROM Emp

&#x20;WHERE dept IN ('Admin');



Q9. Delete employees whose salary is 37000, 38000, or 41000.

DELETE FROM Emp

&#x20;WHERE salary IN (37000, 38000, 41000);



Q10. Delete employees from the IT, Finance, and Sales departments.

DELETE FROM Emp

&#x20;WHERE dept IN ('IT', 'Finance', 'Sales');



###### **LIKE Operator Practice Questions**

**------------------------------------------**



SELECT Queries (LIKE Operator)

Q1. Display employees whose names start with 'R'.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE name LIKE 'R%';



Q2. Display employees whose names end with 'sh'.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE name LIKE '%sh';



Q3. Display employees whose names contain 'ar'.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE name LIKE '%ar%';



Q4. Display employees whose names have exactly 5 characters.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE name LIKE '\_\_\_\_\_';



– Q5. Display employees whose names start with 'K' and end with 'n'.

SELECT

SELECT \*

&#x20;FROM Emp

&#x20;WHERE name LIKE 'K%n';



Q6. Display employees whose names have 'a' as the second character.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE name LIKE '\_a%';



Q7. Display employees whose names contain 'es'.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE name LIKE '%es%';



Q8. Display employees whose names end with 'n'.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE name LIKE '%n';



Q9. Display employees whose names start with 'M' and contain 'e'.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE name LIKE 'M%e%';



Q10. Display employees whose names have exactly 6 characters and end with 'h'.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE name LIKE '\_\_\_\_\_h';



Q11. Display employees whose names start with 'A'.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE name LIKE 'A%';



Q12. Display employees whose names end with 'an'.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE name LIKE '%an';



Q13. Display employees whose names contain 'oh'.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE name LIKE '%oh%';



Q14. Display employees whose names have exactly 7 characters.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE name LIKE '\_\_\_\_\_\_\_';



Q15. Display employees whose names start with 'S'.

SELECT \*

&#x20;FROM Emp

&#x20;WHERE name LIKE 'S%';



UPDATE Queries

Q1. Increase salary by 2000 for employees whose names start with 'R'.

UPDATE Emp

&#x20;SET salary = salary + 2000

&#x20;WHERE name LIKE 'R%';



Q2. Increase salary by 3000 for employees whose names end with 'sh'.

UPDATE Emp

&#x20;SET salary = salary + 3000

&#x20;WHERE name LIKE '%sh';



Q3. Increase salary by 1000 for employees whose names contain 'ar'.

UPDATE Emp

&#x20;SET salary = salary + 1000

&#x20;WHERE name LIKE '%ar%';



Q4. Increase salary by 500 for employees whose names have exactly 5 characters.

UPDATE Emp

&#x20;SET salary = salary + 500

&#x20;WHERE name LIKE '\_\_\_\_\_';



Q5. Increase salary by 2500 for employees whose names start with 'K' and end with 'n'.

UPDATE Emp

&#x20;SET salary = salary + 2500

&#x20;WHERE name LIKE 'K%n';



Q6. Increase salary by 1500 for employees whose names have 'a' as the second character.

UPDATE Emp

&#x20;SET salary = salary + 1500

&#x20;WHERE name LIKE '\_a%';



Q7. Increase salary by 4000 for employees whose names contain 'es'.

UPDATE Emp

&#x20;SET salary = salary + 4000

&#x20;WHERE name LIKE '%es%';



Q8. Increase salary by 1000 for employees whose names end with 'n'.

UPDATE Emp

&#x20;SET salary = salary + 1000

&#x20;WHERE name LIKE '%n';



Q9. Increase salary by 5000 for employees whose names start with 'M' and contain 'e'.

UPDATE Emp

&#x20;SET salary = salary + 5000

&#x20;WHERE name LIKE 'M%e%';



Q10. Increase salary by 2000 for employees whose names have exactly 6 characters and end with 'h'.

UPDATE Emp

&#x20;SET salary = salary + 2000

&#x20;WHERE name LIKE '\_\_\_\_\_h';



DELETE Queries

Q1. Delete employees whose names start with 'R'.

DELETE FROM Emp

&#x20;WHERE name LIKE 'R%';



Q2. Delete employees whose names end with 'sh'.

DELETE FROM Emp

&#x20;WHERE name LIKE '%sh';



Q3. Delete employees whose names contain 'ar'.

DELETE FROM Emp

&#x20;WHERE name LIKE '%ar%';



Q4. Delete employees whose names have exactly 5 characters.

DELETE FROM Emp

&#x20;WHERE name LIKE '\_\_\_\_\_';



Q5. Delete employees whose names start with 'K' and end with 'n'.

DELETE FROM Emp

&#x20;WHERE name LIKE 'K%n';



Q6. Delete employees whose names have 'a' as the second character.

DELETE FROM Emp

&#x20;WHERE name LIKE '\_a%';



Q7. Delete employees whose names contain 'es'.

DELETE FROM Emp

&#x20;WHERE name LIKE '%es%';



Q8. Delete employees whose names end with 'n'.

DELETE FROM Emp

&#x20;WHERE name LIKE '%n';



Q9. Delete employees whose names start with 'M' and contain 'e'.

DELETE FROM Emp

&#x20;WHERE name LIKE 'M%e%';



Q10. Delete employees whose names have exactly 6 characters and end with 'h'.

DELETE FROM Emp

&#x20;WHERE name LIKE '\_\_\_\_\_h';



###### **CASE Statement in MySQL**

**------------------------------**



The CASE statement is used to apply conditional logic in SQL. It works similarly to the if-else statement in programming languages.

Syntax

CASE

&#x20;   WHEN condition1 THEN result1

&#x20;   WHEN condition2 THEN result2

&#x20;   ...

&#x20;   ELSE result

END



Sample Table

CREATE TABLE employees (

&#x20;   emp\_id INT PRIMARY KEY,

&#x20;   emp\_name VARCHAR(50),

&#x20;   department VARCHAR(30),

&#x20;   salary DECIMAL(10,2),

&#x20;   experience INT,

&#x20;   age INT

);



INSERT INTO employees VALUES

(101,'Ravi','IT',65000,5,28),

(102,'Priya','HR',45000,2,24),

(103,'Amit','Finance',75000,8,35),

(104,'Sneha','IT',55000,3,27),

(105,'Rahul','Sales',40000,1,22),

(106,'Kiran','Finance',90000,12,40),

(107,'Anjali','HR',52000,4,29),

(108,'Suresh','Sales',68000,7,33);



CASE Examples

Example 1: Employee Salary Category

SELECT emp\_name,

salary,

CASE

&#x20;   WHEN salary >= 80000 THEN 'High Salary'

&#x20;   WHEN salary >= 60000 THEN 'Medium Salary'

&#x20;   ELSE 'Low Salary'

END AS salary\_category

FROM employees;



Output:



**Employee	Salary		Category**

Ravi		65000		Medium Salary

Priya		45000		Low Salary

Amit		75000		Medium Salary

Sneha		55000		Low Salary

Rahul		40000		Low Salary

Kiran		90000		High Salary

Anjali		52000		Low Salary

Suresh		68000		Medium Salary





Example 2: Experience Level

SELECT emp\_name,

experience,

CASE

&#x20;   WHEN experience >= 10 THEN 'Expert'

&#x20;   WHEN experience >= 5 THEN 'Senior'

&#x20;   WHEN experience >= 2 THEN 'Junior'

&#x20;   ELSE 'Fresher'

END AS experience\_level

FROM employees;



Example 3: Department BonusSELECT emp\_name,

department,

salary,

CASE

&#x20;   WHEN department='IT' THEN salary\*0.20

&#x20;   WHEN department='Finance' THEN salary\*0.15

&#x20;   WHEN department='HR' THEN salary\*0.10

&#x20;   ELSE salary\*0.05

END AS bonus

FROM employees;



Example 4: Voting Eligibility

SELECT emp\_name,

age,

CASE

&#x20;   WHEN age>=18 THEN 'Eligible'

&#x20;   ELSE 'Not Eligible'

END AS voting\_status

FROM employees;



Example 5: Grade Employees

SELECT emp\_name,

salary,

CASE

&#x20;   WHEN salary>=80000 THEN 'A'

&#x20;   WHEN salary>=60000 THEN 'B'

&#x20;   WHEN salary>=50000 THEN 'C'

&#x20;   ELSE 'D'

END AS grade

FROM employees;



Example 6: CASE in ORDER BY

Display IT employees first.

SELECT \*

FROM employees

ORDER BY

CASE

&#x20;   WHEN department='IT' THEN 1

&#x20;   ELSE 2

END;



Example 7: CASE in UPDATE

Increase salary based on experience.

UPDATE employees

SET salary =

CASE

&#x20;   WHEN experience>=10 THEN salary+10000

&#x20;   WHEN experience>=5 THEN salary+5000

&#x20;   ELSE salary+2000

END;



Example 8: CASE with Aggregate Function

SELECT

SUM(

CASE

&#x20;   WHEN department='IT'

&#x20;   THEN salary

&#x20;   ELSE 0

END

) AS total\_it\_salary

FROM employees;



Interview Questions (CASE)

Q1. Display employee name and salary status.

SELECT emp\_name,

salary,

CASE

WHEN salary>60000 THEN 'Good Salary'

ELSE 'Average Salary'

END AS status

FROM employees;



Q2. Display "Experienced" if experience is more than 5 years.

SELECT emp\_name,

CASE

WHEN experience>5 THEN 'Experienced'

ELSE 'Less Experienced'

END AS experience\_status

FROM employees;



SYSTEM INFORMATION FUNCTIONS



System Information Functions

These functions return information about the MySQL server, current user, current database, current date, current time, etc.



Q1. Display the current date.

SELECT CURDATE();



Q2. Display the current time.

SELECT CURTIME();



Q3. Display the current date and time.

SELECT NOW();



Q4. Display the current database.

SELECT DATABASE();



Q5. Display the current logged-in user.

SELECT USER();



Q6. Display the current MySQL version.

SELECT VERSION();



Q7. Display the current system date.

SELECT SYSDATE();



Q8. Display the current connection ID.

SELECT CONNECTION\_ID();



Q9. Display the current database user.

SELECT CURRENT\_USER();



Q10. Display the current UTC date.

SELECT UTC\_DATE();se



Q11. Display the current UTC time.

SELECT UTC\_TIME();



Q12. Display the current UTC date and time.

SELECT UTC\_TIMESTAMP();









