
# SQL-QUERIES ########
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

![part 1](https://user-images.githubusercontent.com/13667918/27924017-4de51a64-624e-11e7-9215-131ea1736041.jpg)
![part 2](https://user-images.githubusercontent.com/13667918/27924014-4de15578-624e-11e7-8115-12217c17409d.jpg)
![part 3](https://user-images.githubusercontent.com/13667918/27924013-4de0448a-624e-11e7-9946-1dd8a5f24d31.jpg)
![part 4](https://user-images.githubusercontent.com/13667918/27924015-4de14eb6-624e-11e7-88fc-87621e859d72.jpg)
![part 5](https://user-images.githubusercontent.com/13667918/27924012-4ddf4e9a-624e-11e7-8384-d264fb44907c.jpg)
![part 6](https://user-images.githubusercontent.com/13667918/27924016-4de498b4-624e-11e7-9051-f2e44abacc5a.jpg)
![part 7](https://user-images.githubusercontent.com/13667918/27924020-4e090c80-624e-11e7-8a7a-e7af4cf05750.JPG)
![part 8](https://user-images.githubusercontent.com/13667918/27924018-4e079b7a-624e-11e7-84f5-244a080a85d4.JPG)
![part 9](https://user-images.githubusercontent.com/13667918/27924022-4e0cef26-624e-11e7-8ab7-457a3cf22458.jpg)
![part 10](https://user-images.githubusercontent.com/13667918/27924023-4e0d92b4-624e-11e7-84a3-132b10260ed6.jpg)
![part 11](https://user-images.githubusercontent.com/13667918/27924021-4e0af54a-624e-11e7-9f0f-ad6c53594446.jpg)
![part 12](https://user-images.githubusercontent.com/13667918/27924019-4e07bd08-624e-11e7-9d67-51dbd66cc52c.jpg)
![part 13](https://user-images.githubusercontent.com/13667918/27924027-4e32955a-624e-11e7-81b0-09774f4cf1a1.jpg)
![part 14](https://user-images.githubusercontent.com/13667918/27924024-4e3159ce-624e-11e7-84fd-98c5b57059f3.jpg)
![part 15](https://user-images.githubusercontent.com/13667918/27924028-4e3327cc-624e-11e7-95fb-860a9c45248c.jpg)
![part 16](https://user-images.githubusercontent.com/13667918/27924029-4e344116-624e-11e7-9ef1-235acb3dd913.jpg)
![part 17](https://user-images.githubusercontent.com/13667918/27924026-4e3262ce-624e-11e7-9931-20f24c5ad789.jpg)
![part 18](https://user-images.githubusercontent.com/13667918/27924025-4e31d5ca-624e-11e7-98a4-25536d498837.jpg)
![part 19](https://user-images.githubusercontent.com/13667918/27924035-4e57e1fc-624e-11e7-9b63-6e21741c5c84.jpg)
![part 20](https://user-images.githubusercontent.com/13667918/27924033-4e55973a-624e-11e7-85a7-86c6ca9156dd.jpg)
![part 21](https://user-images.githubusercontent.com/13667918/27924034-4e57b632-624e-11e7-9d0e-ccd9bdfc429f.jpg)
![part 22](https://user-images.githubusercontent.com/13667918/27924032-4e5397dc-624e-11e7-9997-16ba13817fc3.jpg)
![part 23](https://user-images.githubusercontent.com/13667918/27924030-4e508984-624e-11e7-9a13-404b4c7d5eb4.jpg)
![part 24](https://user-images.githubusercontent.com/13667918/27924031-4e528220-624e-11e7-8893-27965d9421ee.jpg)
![part 25](https://user-images.githubusercontent.com/13667918/27924036-4e74fa76-624e-11e7-98ea-67a6eb3cea5d.jpg)
![part 26](https://user-images.githubusercontent.com/13667918/27924040-4e7b5dee-624e-11e7-8b68-3a1d48987d89.jpg)
![part 27](https://user-images.githubusercontent.com/13667918/27924038-4e79c59c-624e-11e7-9210-bbe90c99a16b.JPG)
![part 28](https://user-images.githubusercontent.com/13667918/27924039-4e7ae5a8-624e-11e7-8e0c-e2d431af01d9.jpg)
![part 29](https://user-images.githubusercontent.com/13667918/27924037-4e795a26-624e-11e7-8243-e3e96b427bcf.jpg)
![part 30](https://user-images.githubusercontent.com/13667918/27924041-4e7dd6a0-624e-11e7-8f13-d40efa014716.jpg)
![part 31](https://user-images.githubusercontent.com/13667918/27924042-4e9bb300-624e-11e7-9962-dd844ef74047.jpg)
![part 32](https://user-images.githubusercontent.com/13667918/27924043-4e9da41c-624e-11e7-844b-931aa76f8767.jpg)
![part 33](https://user-images.githubusercontent.com/13667918/27924044-4e9dda04-624e-11e7-8daa-fc2f0a48e8ef.jpg)
![part 34](https://user-images.githubusercontent.com/13667918/27924047-4ea09136-624e-11e7-9ada-5a50222e34a4.jpg)
![part 35](https://user-images.githubusercontent.com/13667918/27924045-4e9efbb4-624e-11e7-8bb3-c24bd89bb333.jpg)
![part 36](https://user-images.githubusercontent.com/13667918/27924046-4e9fe0f6-624e-11e7-81ad-f19fb13a0593.jpg)
![part 37](https://user-images.githubusercontent.com/13667918/27924048-4ec5041c-624e-11e7-995a-f0fd9f551aee.jpg)
![part 38](https://user-images.githubusercontent.com/13667918/27924050-4ec5f00c-624e-11e7-8892-085d6198af07.jpg)
![part 39](https://user-images.githubusercontent.com/13667918/27924049-4ec5a8e0-624e-11e7-990d-04accba9b52d.jpg)
![part 40](https://user-images.githubusercontent.com/13667918/27924053-4ece1b38-624e-11e7-9e93-57b9e4143914.jpg)
![part 41](https://user-images.githubusercontent.com/13667918/27924051-4ec6fcae-624e-11e7-93d3-b71357d9ead7.jpg)
![part 42](https://user-images.githubusercontent.com/13667918/27924052-4ec86bc0-624e-11e7-80c3-62475c200584.jpg)
![part 43](https://user-images.githubusercontent.com/13667918/27924058-4ef6864a-624e-11e7-9097-9ba269378c6e.jpg)
![part 44](https://user-images.githubusercontent.com/13667918/27924055-4ef3af2e-624e-11e7-8e77-205275d28779.jpg)
![part 45](https://user-images.githubusercontent.com/13667918/27924059-4ef6a6c0-624e-11e7-90cc-b17e60c34624.jpg)
![part 46](https://user-images.githubusercontent.com/13667918/27924060-4efa0040-624e-11e7-9f69-6c581ba0cab8.JPG)
![part 47](https://user-images.githubusercontent.com/13667918/27924056-4ef57bd8-624e-11e7-9ab2-30512e52651c.jpg)
![part 48](https://user-images.githubusercontent.com/13667918/27924057-4ef600f8-624e-11e7-8ed7-3edbdcb46c81.JPG)
![part 49](https://user-images.githubusercontent.com/13667918/27924064-4f1a990e-624e-11e7-8905-4e5a123ebe4f.JPG)
![part 50](https://user-images.githubusercontent.com/13667918/27924066-4f1bfd58-624e-11e7-8b5d-61d563d74ca3.jpg)
![part 51](https://user-images.githubusercontent.com/13667918/27924063-4f1a4058-624e-11e7-9c29-84ff7f977b0b.JPG)
![part 52](https://user-images.githubusercontent.com/13667918/27924065-4f1b4eda-624e-11e7-995e-cc208bc5a6d6.jpg)
![part 53](https://user-images.githubusercontent.com/13667918/27924062-4f1948ce-624e-11e7-931c-e15347c5fff3.jpg)
![part 54](https://user-images.githubusercontent.com/13667918/27924061-4f18cd86-624e-11e7-9964-4e3e3d6e9610.JPG)
![part 55](https://user-images.githubusercontent.com/13667918/27924067-4f3b7f3e-624e-11e7-9082-362d8c81dc3a.jpg)
![part 56](https://user-images.githubusercontent.com/13667918/27924068-4f3bf932-624e-11e7-9372-5eb79982c84d.JPG)
![part 57](https://user-images.githubusercontent.com/13667918/27924069-4f3c530a-624e-11e7-82ec-9dfc568670ba.jpg)
![part 58](https://user-images.githubusercontent.com/13667918/27924070-4f3c8528-624e-11e7-8a7b-4bf12b2208bb.jpg)
![part 59](https://user-images.githubusercontent.com/13667918/27924071-4f40528e-624e-11e7-8d73-b9ebd10eeed6.JPG)
![part 60](https://user-images.githubusercontent.com/13667918/27924072-4f432f2c-624e-11e7-9cd7-69220b5ce20a.jpg)
![part 61](https://user-images.githubusercontent.com/13667918/27924075-4f6821b0-624e-11e7-9126-95ff7c1bd80b.jpg)
![part 62](https://user-images.githubusercontent.com/13667918/27924074-4f6768f6-624e-11e7-9256-08a5d9545f8c.JPG)
![part 63](https://user-images.githubusercontent.com/13667918/27924076-4f690922-624e-11e7-821e-51ad69397f4a.JPG)
![part 64](https://user-images.githubusercontent.com/13667918/27924073-4f650cf0-624e-11e7-8ea0-64f488c6e774.jpg)
![part 65](https://user-images.githubusercontent.com/13667918/27924093-4f9ed4a8-624e-11e7-96a7-90c0db8dcd90.JPG)
![part 66](https://user-images.githubusercontent.com/13667918/27924077-4f6966ec-624e-11e7-84f7-e545d05faf24.jpg)
![part 67](https://user-images.githubusercontent.com/13667918/27924079-4f838b80-624e-11e7-9ca8-a9e7c9d6e8a1.jpg)
![part 68](https://user-images.githubusercontent.com/13667918/27924082-4f87eed2-624e-11e7-8122-95e1944cbcc5.jpg)
![part 69](https://user-images.githubusercontent.com/13667918/27924078-4f82f1f2-624e-11e7-8b8d-0f3429e6505d.jpg)
![part 70](https://user-images.githubusercontent.com/13667918/27924081-4f84f40c-624e-11e7-855f-0354bda865ed.JPG)
![part 71](https://user-images.githubusercontent.com/13667918/27924080-4f838dba-624e-11e7-9256-fc8a7ec4ca78.jpg)
![part 72](https://user-images.githubusercontent.com/13667918/27924083-4f896186-624e-11e7-91f5-a5a024e87916.JPG)
![part 73](https://user-images.githubusercontent.com/13667918/27924085-4f8e996c-624e-11e7-87af-1dd26d0923c9.jpg)
![part 74](https://user-images.githubusercontent.com/13667918/27924087-4f9281e4-624e-11e7-9be4-05534217c65f.jpg)
![part 75](https://user-images.githubusercontent.com/13667918/27924084-4f8eb280-624e-11e7-9d59-80a88787c789.JPG)
![part 76](https://user-images.githubusercontent.com/13667918/27924089-4f960062-624e-11e7-9d00-0dee8cf3b8eb.jpg)
![part 77](https://user-images.githubusercontent.com/13667918/27924088-4f93c450-624e-11e7-8632-393053158015.jpg)
![part 78](https://user-images.githubusercontent.com/13667918/27924090-4f985646-624e-11e7-99a5-4d657419c0c6.JPG)
![part 79](https://user-images.githubusercontent.com/13667918/27924092-4f9b2cae-624e-11e7-8d27-13361a8268c0.jpg)
![part 80](https://user-images.githubusercontent.com/13667918/27924095-4fa08fa0-624e-11e7-8db2-64ad0996bdb0.JPG)
![part 81](https://user-images.githubusercontent.com/13667918/27924103-4fb37930-624e-11e7-829d-5f16c5834e05.jpg)
![part 82](https://user-images.githubusercontent.com/13667918/27924094-4f9f7f34-624e-11e7-876a-0a4adcdbd0f1.JPG)
![part 83](https://user-images.githubusercontent.com/13667918/27924096-4fa3e344-624e-11e7-8813-c26132c6a82d.jpg)
![part 84](https://user-images.githubusercontent.com/13667918/27924097-4fa61d12-624e-11e7-88cc-5cf4868eb1c2.jpg)
![part 85](https://user-images.githubusercontent.com/13667918/27924099-4fac49d0-624e-11e7-9def-6b28ebff1971.JPG)
![part 86](https://user-images.githubusercontent.com/13667918/27924098-4fa88a7a-624e-11e7-99f4-6c99879dc20a.jpg)
![part 87](https://user-images.githubusercontent.com/13667918/27924101-4faef5c2-624e-11e7-9246-17d5aa936d7e.jpg)
![part 88](https://user-images.githubusercontent.com/13667918/27924100-4fae80b0-624e-11e7-88df-e0371bfb5779.JPG)
![part 89](https://user-images.githubusercontent.com/13667918/27924102-4fb1713a-624e-11e7-991d-e60eb97f8d54.jpg)
![part 90](https://user-images.githubusercontent.com/13667918/27924105-4fbcb4e6-624e-11e7-9b5b-f6c7f3914f0e.JPG)
![part 91](https://user-images.githubusercontent.com/13667918/27924104-4fba2d34-624e-11e7-9d52-871ab60a2b15.jpg)
![part 92](https://user-images.githubusercontent.com/13667918/27924107-4fbd316e-624e-11e7-9c45-b64e49272331.jpg)
![part 93](https://user-images.githubusercontent.com/13667918/27924106-4fbceace-624e-11e7-952a-8c6f3b5d51c2.JPG)
![part 94](https://user-images.githubusercontent.com/13667918/27924108-4fbe8e38-624e-11e7-859f-cd4e1ad3f25c.jpg)
![part 95](https://user-images.githubusercontent.com/13667918/27924109-4fc245b4-624e-11e7-8dd0-76139944e816.JPG)
![part 96](https://user-images.githubusercontent.com/13667918/27924110-4fc5c9f0-624e-11e7-84ad-7d2a3cc33b63.jpg)
![part 97](https://user-images.githubusercontent.com/13667918/27924112-4fc70a72-624e-11e7-9264-e3fc737167d5.jpg)
![part 98](https://user-images.githubusercontent.com/13667918/27924113-4fcb92c2-624e-11e7-84f5-a66a65af715c.JPG)
![part 99](https://user-images.githubusercontent.com/13667918/27924111-4fc648a8-624e-11e7-8dc7-9c74c15f4798.jpg)
![part 100](https://user-images.githubusercontent.com/13667918/27924114-4fcd05bc-624e-11e7-827d-fef216a7e895.JPG)
![part 101](https://user-images.githubusercontent.com/13667918/27924118-4fd68bbe-624e-11e7-9995-f837b69878da.jpg)
![part 102](https://user-images.githubusercontent.com/13667918/27924116-4fd46320-624e-11e7-89d1-16ce3dd8d993.JPG)
![part 103](https://user-images.githubusercontent.com/13667918/27924115-4fd2ce52-624e-11e7-9ffa-488793b7dbd0.JPG)
![part 104](https://user-images.githubusercontent.com/13667918/27924117-4fd6131e-624e-11e7-850a-dcd617a7ed12.jpg)
![part 105](https://user-images.githubusercontent.com/13667918/27924119-4fdfe038-624e-11e7-8528-dff5581ec704.jpg)
![part 106](https://user-images.githubusercontent.com/13667918/27924121-4fe0626a-624e-11e7-898d-5b9695fdf352.jpg)
![part 107](https://user-images.githubusercontent.com/13667918/27924122-4fe3dc7e-624e-11e7-8fe9-729af3768e66.JPG)
![part 108](https://user-images.githubusercontent.com/13667918/27924123-4fe47bfc-624e-11e7-8980-b6c76f978374.jpg)
![part 109](https://user-images.githubusercontent.com/13667918/27924120-4fdff7b2-624e-11e7-924e-4c270c74b76f.jpg)
![part 110](https://user-images.githubusercontent.com/13667918/27924124-4fe5d9f2-624e-11e7-8897-d6d10dae6986.JPG)
![part 111](https://user-images.githubusercontent.com/13667918/27924128-4ff0dbe0-624e-11e7-90df-73a1ffc776fe.JPG)
![part 112](https://user-images.githubusercontent.com/13667918/27924126-4fe924fe-624e-11e7-9fda-21d1967fcdaf.jpg)
![part 113](https://user-images.githubusercontent.com/13667918/27924125-4fe8c806-624e-11e7-9924-b72051e6fa9a.jpg)
![part 114](https://user-images.githubusercontent.com/13667918/27924129-4ff1e45e-624e-11e7-81e3-8145cc98d418.jpg)
![part 115](https://user-images.githubusercontent.com/13667918/27924127-4fee731e-624e-11e7-9991-410e25505926.JPG)
![part 116](https://user-images.githubusercontent.com/13667918/27924130-4ff4a568-624e-11e7-8e2b-2b0da9eccd6f.JPG)
![part 117](https://user-images.githubusercontent.com/13667918/27924131-4ff4e23a-624e-11e7-8a8e-983fa51bc591.jpg)
![part 118](https://user-images.githubusercontent.com/13667918/27924132-4ff8238c-624e-11e7-858b-ed976a907712.jpg)
![part 119](https://user-images.githubusercontent.com/13667918/27924142-501101b8-624e-11e7-9601-1e73ddc360d4.jpg)
![part 120](https://user-images.githubusercontent.com/13667918/27924134-4ffacace-624e-11e7-9f29-1dd3662a69b8.jpg)
![part 121](https://user-images.githubusercontent.com/13667918/27924133-4ffa6516-624e-11e7-9e11-e1780ebe9f68.jpg)
![part 122](https://user-images.githubusercontent.com/13667918/27924137-50033b96-624e-11e7-8ee5-435804952fdd.jpg)
![part 123](https://user-images.githubusercontent.com/13667918/27924136-5001bc1c-624e-11e7-9fee-f8f1f5a01b2f.JPG)
![part 124](https://user-images.githubusercontent.com/13667918/27924135-50009c9c-624e-11e7-8fda-4b494ac861e5.JPG)
![part 125](https://user-images.githubusercontent.com/13667918/27924139-500a253c-624e-11e7-9be5-4ce46b6df16c.JPG)
![part 126](https://user-images.githubusercontent.com/13667918/27924141-500e24ca-624e-11e7-8a7d-0208d14a41da.JPG)
![part 127](https://user-images.githubusercontent.com/13667918/27924138-50080928-624e-11e7-8403-22dd02ed940d.JPG)
![part 128](https://user-images.githubusercontent.com/13667918/27924143-5014217c-624e-11e7-9dc3-c4ac93b95ca7.JPG)
![part 129](https://user-images.githubusercontent.com/13667918/27924140-500ca8a2-624e-11e7-9be5-92b4645d16d7.JPG)
![part 130](https://user-images.githubusercontent.com/13667918/27924148-502bbb66-624e-11e7-8f89-6cf9344ca9a0.JPG)
![part 131](https://user-images.githubusercontent.com/13667918/27924145-5027eb94-624e-11e7-9773-0311831217d5.JPG)
![part 132](https://user-images.githubusercontent.com/13667918/27924146-50283982-624e-11e7-8713-385f92cffc47.JPG)
![part 133](https://user-images.githubusercontent.com/13667918/27924144-5025f64a-624e-11e7-9288-c16a2539c671.JPG)
![part 134](https://user-images.githubusercontent.com/13667918/27924147-502be578-624e-11e7-9302-7d0149be2720.JPG)
