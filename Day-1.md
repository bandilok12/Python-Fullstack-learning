#### **A. FRONTEND**

**====================**



* Frontend is the visual and interactive layer of a website or application that users directly see and interact with through a web browser or mobile app.
* It is also called the Client Side because it runs on the user's device (browser/mobile).



**Responsibilities of Frontend**

**-----------------------------**

* Displays web pages and user interface (UI).
* Accepts user input (forms, buttons, search boxes).
* Validates user input before sending it to the server.
* Calls Backend APIs to fetch or send data.
* Displays the response received from the backend.
* Provides animations and interactive effects.
* Ensures responsive design for mobile, tablet, and desktop devices.



**Common Frontend Technologies**

**----------------------------**



**Technology**		**Purpose**

HTML		Structure of the webpage

CSS		Styling and layout

JavaScript	Interactivity and dynamic behavior

Bootstrap	Responsive UI framework

React.js	JavaScript library for building UI

Angular		Frontend framework

Vue.js		Progressive JavaScript framework

TypeScript	JavaScript with static typing



**Frontend Examples**

**-----------------**

* Login page
* Registration form
* Shopping cart
* Dashboard
* Profile page
* Online payment page



**Real-Time Example**

**-----------------**

When you click the Login button:

1. Frontend collects username and password.
2. Sends them to the backend through an API.
3. Waiting for the response.
4. Displays either:
* Login Successful
* Invalid Username/Password





#### **B. BACKEND**

**==================**



* Backend is the server-side part of an application.
* Users cannot see it directly, but it performs all the business logic, security, data processing, and database operations.
* It acts as the brain of the application.



**Responsibilities of Backend**

**---------------------------**

* Processes client requests
* Implements business logic
* Connects with databases
* Performs CRUD operations
* Authenticates and authorizes users
* Encrypts passwords and sensitive data
* Generates reports
* Sends emails and notifications
* Handles file uploads/downloads
* Returns responses to the frontend



**Common Backend Technologies**

**---------------------------**



**Technology			Purpose**

Java			Backend Programming Language

Spring Boot		Java Framework

Node.js			JavaScript Runtime

Python(Django/Flask)	Backend Development

PHP			Web Development

.NET			Microsoft Backend Framework

Go			High-performance Backend

Ruby on Rails		Rapid Web Development



**Databases Used**

**--------------**

* MySQL
* PostgreSQL
* Oracle
* SQL Server
* MongoDB
* Firebase



**Backend Tasks Example**

**---------------------**

Suppose a user logs in:

1. Receives username/password.
2. Checks the database.
3. Verifies password.
4. Generates JWT Token or Session.
5. Sends success/failure response.



Real-Time Example

\-----------------

In an Online Banking System:

* Checks account balance
* Validates transaction
* Transfers money
* Updates database
* Sends SMS/Email confirmation

All these happen in the backend.





#### **C. API (Application Programming Interface)**

**=========================================================================**

* An API is a set of rules and protocols that allows two different applications or systems to communicate and exchange data without exposing their internal implementation.
* It acts as a bridge between the Frontend and Backend or between two different software systems.



**Simple Definition**

**-----------------**

API = Communication Bridge



**Restaurant Analogy**

**------------------**



You (Client)  →  gives order to Waiter (API)  →  Kitchen (Server) prepares food

Kitchen       →  gives food to Waiter (API)    →  You receive your meal





**Types of APIs:**

**--------------**



Type			Description		Example

REST API	Uses HTTP, most common		Weather app fetching data

SOAP API	XML-based, used in banking	Net banking transactions

GraphQL		Fetch only what you need	Facebook, GitHub

WebSocket API	Real-time, two-way		WhatsApp, Live scores



**Real-Time Scenario:**

**-------------------**

Booking a flight on MakeMyTrip:

* MakeMyTrip doesn't own airline data
* It calls IndiGo's API, Air India's API etc.
* Each airline API returns available seats \& prices
* MakeMyTrip displays all results in one place
* You never saw the API — but it did all the connecting! 



#### **Storage Areas**

======================

As part of our applications we required to store data like Customers information, or billing information, calls information...etc to store this data we required storage areas.



There are 2 types of storage areas such as

1\. Temporary Storage Areas

2\. Permanent Storage Areas.



**1. Temporary Storage Areas**

================================

These are the memory areas where the data will be stored temporally.

EG: all JVM memory areas(like Heap Area,Stack Area, Method area, PC Registers, Native Method stacks). Once JVM Shutdown all these memory areas will be cleared automatically.



**2. Permanent Storage Areas.**

================================

also known as persistent storage areas. Here we can store data permanently

example: Files Systems, Databases, Data warehouse, Bigdata..etc





#### **File Management System(FMS)**

\-----------------------------------------------

def: A File Management System is a System where data is stored in files on the operation systems, each application program must handle its own storage data, retrieval and updating. File Systems can be provided by the Local Operating System.



File systems are best suitable for to store very less amount of information(like KB)



example:- a library management system storing books in separate text files likes, books.txt, members.txt



**Limitations of File Management Systems(FMS)**

\-------------------------------------------------

1\. Data Redundancy :- same data is stored in multiple files

2\. Data Inconsistency :- updates in one file may not be reflected in another.

3\. poor Data Security :- No proper accessed control.

4\. Difficult Data Retrieval : searching requires custom programs.

5\. Integrity issues :- No Constraints(eg: rollnumber uniqueness)

6\. Scalability issues : hard to manage as data grows.



To overcome the above problems of File systems , we should go for databases.

##### 

#### **Database Management System**

\----------------------------------------------

definition: a DBMS is a Collection of Programs that enables users to create,manage, and manipulate databases.



it acts as an interface between user and database.



**Advantages**

\-----------

1\. We can store huge amounts of information in databases.

2\. Query language support is available for every database and hence we can perform database operations very easily.

3\. To access data present in the database, compulsory username and password must be required. hence data is secured.

4\. inside database data will be stored in the form of tables. While developing database table schemas, database admin fallow various normalization techniques and we can implement various constraints like Unique key constraint, primary key constraints, ..etc which prevent data duplication. hence there is no chance of data inconsistency problems.



**Limitation of Databases**

\----------------------------

1\) Databases cannot store huge amounts of information like terabytes(1000gb)of data.

2\) Database can provide support for only structured data(tabular data or relational data) and cannot provide support for semi structured data like(xml files)and unstructured data (like video files, audio files,images..etc)



To overcome these problems we should go for advanced storage areas like bigdata,Data warehouses. Etc. 





#### **Interview Questions**

**==================================**



**Q: What are the differences between File Management System(FMS) and Database Management System(DBMS)**

\----------------------------------------------------------------------------------------------------

1\. data is stored in separate files

&#x20;  data is stored in a structured database.

2\. High data redundancy(duplicate data)

&#x20;  reduces data redundancy

3\. difficult to maintain and update

&#x20;  easy to maintain and update

4\. security is limited

&#x20;  provides strong security mechanisms.

5\. data sharing is difficult

&#x20;  multiple users can access data simultaneously.

6\. no relationship between files.

&#x20;  supports relationships between tables.

7\. Backup and recovery are difficult

&#x20;  provides backup and recovery features

8\. Data inconsistency may cause anomalies.

&#x20;  maintains data consistency and integrity.

9\. suitable for small applications

&#x20;   suitable for small, medium and large applications.



**Q: What is the difference between a File System and a DBMS?**

\-------------------------------------------------------------

A file system stores data in separate files and may lead to data redundancy, and security issues, A DBMS stores data in structured manner using tables, reduces redundancy, provides security, supports multiple users, and ensures data consistency and integrity.













