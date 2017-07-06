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



![dsc_0077](https://user-images.githubusercontent.com/13667918/27890791-250ab846-61c3-11e7-9ad9-b538b512d33b.JPG)
![dsc_0078](https://user-images.githubusercontent.com/13667918/27890793-250fe6ea-61c3-11e7-8114-0377b2984593.JPG)
![dsc_0079](https://user-images.githubusercontent.com/13667918/27890789-2509689c-61c3-11e7-855b-cd524790a0ae.JPG)
![dsc_0080](https://user-images.githubusercontent.com/13667918/27890792-250dd724-61c3-11e7-8603-312d1f88b039.JPG)
![dsc_0081](https://user-images.githubusercontent.com/13667918/27890790-2509abf4-61c3-11e7-9cfc-9601f1acdbd4.JPG)
![dsc_0082](https://user-images.githubusercontent.com/13667918/27890788-25070e44-61c3-11e7-94d8-3d77858bd482.JPG)
![dsc_0083](https://user-images.githubusercontent.com/13667918/27890794-2519fff4-61c3-11e7-9aa7-74b8d48e372b.JPG)
![dsc_0084](https://user-images.githubusercontent.com/13667918/27890795-251be846-61c3-11e7-9551-1829113a5521.JPG)
![dsc_0085](https://user-images.githubusercontent.com/13667918/27890798-251ef09a-61c3-11e7-9c01-4aa0b92ae05f.JPG)
![dsc_0086](https://user-images.githubusercontent.com/13667918/27890796-251e258e-61c3-11e7-97f7-b15b8799d0c9.JPG)
![dsc_0087](https://user-images.githubusercontent.com/13667918/27890799-252074ec-61c3-11e7-813a-90000e5fccf4.JPG)
![dsc_0088](https://user-images.githubusercontent.com/13667918/27890797-251ee67c-61c3-11e7-9ff6-4a85e8a1f414.JPG)
![dsc_0089](https://user-images.githubusercontent.com/13667918/27890802-2530b6cc-61c3-11e7-9cab-990ec5919426.JPG)
![dsc_0090](https://user-images.githubusercontent.com/13667918/27890801-253097a0-61c3-11e7-95f8-64c81986c6e8.JPG)
![dsc_0091](https://user-images.githubusercontent.com/13667918/27890800-25307afe-61c3-11e7-8483-ec2d4b8d3012.JPG)
![dsc_0092](https://user-images.githubusercontent.com/13667918/27890805-25334a0e-61c3-11e7-824c-bf8d2662f4da.JPG)
![dsc_0093](https://user-images.githubusercontent.com/13667918/27890803-2530bb36-61c3-11e7-8258-fd7a14b0dde6.JPG)
![dsc_0094](https://user-images.githubusercontent.com/13667918/27890804-2531a01e-61c3-11e7-87b8-c2cbc85fbfc0.JPG)
![dsc_0095](https://user-images.githubusercontent.com/13667918/27890809-254a74b8-61c3-11e7-94db-7b70b628fc2c.JPG)
![dsc_0096](https://user-images.githubusercontent.com/13667918/27890806-2545c350-61c3-11e7-936e-1f68b3d01ed9.JPG)
![dsc_0097](https://user-images.githubusercontent.com/13667918/27890808-2548f94e-61c3-11e7-8ab7-92e472d0fc99.JPG)
![dsc_0098](https://user-images.githubusercontent.com/13667918/27890807-25468e98-61c3-11e7-9e35-c526f84e119e.JPG)
![dsc_0099](https://user-images.githubusercontent.com/13667918/27890810-254e6622-61c3-11e7-8a94-d98b5f46fa90.JPG)
![dsc_0100](https://user-images.githubusercontent.com/13667918/27890811-255db74e-61c3-11e7-9843-26ced1a9c075.JPG)
![dsc_0101](https://user-images.githubusercontent.com/13667918/27891524-707e2e02-61c8-11e7-8010-b777f16301ca.JPG)
![dsc_0102](https://user-images.githubusercontent.com/13667918/27891525-7082ccbe-61c8-11e7-9a7b-b9099d65c431.JPG)
![dsc_0103](https://user-images.githubusercontent.com/13667918/27891528-7093f67e-61c8-11e7-85c8-c285b40f667f.JPG)
![dsc_0104](https://user-images.githubusercontent.com/13667918/27891526-70890fa2-61c8-11e7-8b5a-75879646be37.JPG)
![dsc_0105](https://user-images.githubusercontent.com/13667918/27891529-70994ff2-61c8-11e7-9db8-f5ff30c3c51f.JPG)
![dsc_0106](https://user-images.githubusercontent.com/13667918/27891527-708db548-61c8-11e7-877e-779a098ebee2.JPG)
![dsc_0107](https://user-images.githubusercontent.com/13667918/27891530-709b37b8-61c8-11e7-9b80-45e22e8afb77.JPG)
![dsc_0108](https://user-images.githubusercontent.com/13667918/27891534-70a76cb8-61c8-11e7-9f5d-dcd2de974a5c.JPG)
![dsc_0109](https://user-images.githubusercontent.com/13667918/27891531-70a4b6bc-61c8-11e7-9fc6-52cfc738b90f.JPG)
![dsc_0110](https://user-images.githubusercontent.com/13667918/27891533-70a6ea68-61c8-11e7-8851-40897eb47e4f.JPG)
![dsc_0111](https://user-images.githubusercontent.com/13667918/27891532-70a547b2-61c8-11e7-8802-e7120803c63c.JPG)
![dsc_0112](https://user-images.githubusercontent.com/13667918/27891535-70a79882-61c8-11e7-90e0-bf23a532d500.JPG)
![dsc_0113](https://user-images.githubusercontent.com/13667918/27891536-70b69c1a-61c8-11e7-85e8-af571ab40b46.JPG)
![dsc_0114](https://user-images.githubusercontent.com/13667918/27891537-70b7b492-61c8-11e7-9f6e-ea2eaa7e057f.JPG)
![dsc_0115](https://user-images.githubusercontent.com/13667918/27892092-aaed759a-61cb-11e7-879b-aa0ab8640599.JPG)
![dsc_0116](https://user-images.githubusercontent.com/13667918/27892093-aaf17532-61cb-11e7-9ce3-3d725fafb701.JPG)
![dsc_0118](https://user-images.githubusercontent.com/13667918/27892094-aaf6878e-61cb-11e7-89c5-8858511e75a2.JPG)
![dsc_0119](https://user-images.githubusercontent.com/13667918/27892096-aafc2568-61cb-11e7-9e62-a3ba32e6714c.JPG)
![dsc_0120](https://user-images.githubusercontent.com/13667918/27892095-aaf75b82-61cb-11e7-804f-ee6ece66ae31.JPG)
![dsc_0121](https://user-images.githubusercontent.com/13667918/27892097-aafe3c9a-61cb-11e7-9edf-ec2b17ffe5c4.JPG)
![dsc_0123](https://user-images.githubusercontent.com/13667918/27892098-ab02e704-61cb-11e7-855f-5319ef2a186e.JPG)
![dsc_0124](https://user-images.githubusercontent.com/13667918/27892099-ab0c2c92-61cb-11e7-9a48-d7d77557f0ee.JPG)

