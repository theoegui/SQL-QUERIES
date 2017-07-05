# SQL-QUERIES
# SQL-QUERIES
This is a tutorial for new Users who are not familiar with basic SQL queries . I will provide syntax and a step by step guide on applying queries . 

#### We are going to skip over the basic installment on how to run a MySQL server version 5.6.16 · SID Version 2.6.9
#### DATABASE ENGINE InnoDB 2016 but instead go straight into applying the queries . 

XAMPP needs to be run.



![read me 1](https://user-images.githubusercontent.com/13667918/27870555-258ac6c8-6171-11e7-8b55-b0db40652cd7.jpg)
![read me 0](https://user-images.githubusercontent.com/13667918/27870560-2a75438e-6171-11e7-9bbf-84a0a3d15b2b.jpg)
![read me 1 5](https://user-images.githubusercontent.com/13667918/27870565-2f85bbb0-6171-11e7-8b37-40a67921b306.jpg)

![read me 1 5 part 2](https://user-images.githubusercontent.com/13667918/27872120-b6ac6900-6175-11e7-8f55-dfbc932e89bf.jpg)

Then in the url we type in http://localhost/SID/sid/sid.php
This is where we use my given data to apply my queries .
![read me 2](https://user-images.githubusercontent.com/13667918/27870579-376cc9ae-6171-11e7-991e-de71e47b7093.jpg)
![read me 3](https://user-images.githubusercontent.com/13667918/27870580-3783d824-6171-11e7-8a41-d3a7dd4ee42b.jpg)
This is just a super small example but moving forward , we will see more queries . 
In another tab ,  if you type in  http://localhost/CRUD/crud.php in the URL , you will have the DATABASE Engine directing you to a CRUD which is an acronym for the database operations Create, Read, Update, and Delete. 
![read me 4](https://user-images.githubusercontent.com/13667918/27871102-b132df7a-6172-11e7-9e18-2e1ca2552a9d.jpg)
The Data Access Layer communicates with the Data Storage Layer to perform CRUD operations. CRUD represents an acronym for the database operations Create, Read, Update, and Delete. The communication between two layers could be in the form of ad hoc SQL statements such as INSERT, SELECT, UPDATE, and DELETE. The stored procedures approach foregoes these SQL statements and uses only the EXECUTE statement on stored procedures.
Why CRUD?
There are several reasons for using stored procedures to perform CRUD operations instead of ad-hoc SQL statements:
Because of Performance!
After the first execution of a stored procedure, the procedures execution plan is stored in SQL Server’s procedure cache and reused for all following invocations of the stored procedure.
When any SQL statement is executed in SQL Server, the relational engine will first look through the procedure cache to verify that an existing execution plan for the specified SQL statement exists and reuse any existing plan, saving the overhead of parsing, optimization, and recompiling steps for the SQL statement. If the execution plan doesn’t exist which is the case with the ad-hoc SQL statements, SQL Server will generate a new execution plan for the query.
Decouples the SQL code from the other layers of the application
By removing the SQL statements from the application code, all the SQL can be kept in the database and nothing but stored procedure invocations in the client application. Using stored procedures to encapsulate the database access is also an effective way to decrease database coupling.
Prevents SQL injection attacks
Using stored procedures instead of string concatenation to build dynamic queries from user input data for all SQL Statements reduces the chance of SQL injection attacks because everything placed into a parameter gets quoted in the process.
CRUD stored procedures
There are some common naming conventions to differ CRUD procedures from other stored procedures in the database including:
The prefix should differ from the prefix used for other user defined stored procedures
Using the table name after the prefix insures that the CRUD procedures for the same table are grouped together
The procedure name should end with the name of the CRUD operation that it implements




######
But we will go over that in another time . 
OKay moving foward .....

![intro 2](https://user-images.githubusercontent.com/13667918/27877219-d245d89c-6187-11e7-8f67-4f2352768b30.jpg)
<img width="960" alt="intro 3" src="https://user-images.githubusercontent.com/13667918/27877218-d24598b4-6187-11e7-9164-f2744c99d175.png">
![intro 4](https://user-images.githubusercontent.com/13667918/27877216-d24111b8-6187-11e7-9898-3c44b9e88be7.jpg)
![intro 5](https://user-images.githubusercontent.com/13667918/27877221-d255a3da-6187-11e7-984d-d37bee87d263.jpg)
![intro 6](https://user-images.githubusercontent.com/13667918/27877217-d244a62a-6187-11e7-814e-852bdcd4fa19.jpg)

The FROM clause specifies the table.
The WHERE clause specifies the condition that must be satisfied for each row selected .

SELECT COUNT (*) FROM ALBUM WHERE label = 'Columbia';

Functions used to perform specific operations on data. Above is a function that is used to find the number of rows matching the condition in the WHERE CLAUSE.

There are so many select statements , its not even funny . Below is even more examples but eventually we will definitely go over them later.
![intro 7](https://user-images.githubusercontent.com/13667918/27880781-3b097e40-6194-11e7-8168-98819da57ef9.jpg)




