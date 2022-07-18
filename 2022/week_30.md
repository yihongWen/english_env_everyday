## 07-18:

**Database Objects of SQL Server** 

​	Database objects can be anything from tables to small pieces of code that can be used to perform application functions in the database. 

**Tables** 

​	A table is simply a database object made up of columns and rows that can be used to store data. A database can contain as many as two billion tables with as many as 1,024 columns per table. The only limiting factor to the number of rows in the database is the amount of disk space that you have to allocate to that database. The maximum row length in an SQL Server table is 8,060 bytes long. Each column in the table will contain data only of a specific datatype. SQL Server supports two different types of tables—permanent and temporary. 

​	Permanent tables are created in the database and remain there until they are dropped. Normally, these tables are used to store permanent data, such as anything that is created by your users. These tables are created in the database that you specify. 

​	The other type of table is temporary tables. These tables are usually created by the user application for temporary storage space. Two types of temporary table exist. The first is local temporary tables. These tables are created by one user and accessible only by that user. The other type of temporary table is a global temporary table. These tables are created by one user and then accessible by any user who is on the system. A local temporary table is dropped as soon as the user who created it **logs out** of the system. A global temporary table is dropped as soon as the user who created the table logs out of the system, and any other users who have been referencing it log out. Temporary tables are created in the tempdb database. They are created with a prefix of # for local temporary tables and # # for global temporary tables. 

**Views**

​	Views are **intrinsically(本质的，内在的)** related to tables in that they are essentially virtual tables. Views are used to represent data from one table or more than one in an alternative way. Views are created only in the database that you are currently using. There are many reasons for using views, including: 

- Focusing on Specific Data
- Query Simplification
- Data Customization
- Security
- Exporting Data
- Simplifying Access to Partitioned Data

​	It is important for you to realize that there is no data at all stored in the view itself. The view is only a simpler way to access the data that is contained in other tables in the database. 



**Indexes** 

​	An index is a special type of database object that is associated with a table directly. An index is used to speed up access to the data in that table and can enforce some data integrity issues, such as uniqueness of rows in that table. Indexes contain keys that are made up of at least one column in the table. The keys allow SQL Server to **pinpoint(精准确定)** rows in the table quickly without needing to scan the entire table for the requested rows. If you create a table that contains no indexes on it, SQL Server will store the data in that table in no particular order. 

​	The two types of indexes that can be created on tables in SQL Server are as follows: 

- Clustered
- Nonclustered 

​	When you are working with indexes, it is important to remember that the columns which are frequently searched on, such as an employee’s ID number or last name, should be indexed. This will speed the process of getting at the data. 



**Datatypes** 

​	A datatype is a definition for the type of data that you are going to be placing in a table or variable. Datatypes are used for several purposes. First, they tell SQL Server what type of data to expect, **thereby allowing space allocation to be optimized for that specific datatype.** Secondly, they allow the developer to determine what type of data needs to be collected—for example, numeric data or character data—and force the user to input that type of data. Any attempt to input data not of that type results in an error. Lastly, they ensure consistency across all the rows in the table. Many different datatypes are available in SQL Server. If these datatypes are not enough for you, though, you can also create your own based on the original ones provided to you by SQL Server. 



**Constraints** 

​	Constraints are a way to ensure that data in your databases is in the form that you expect it to be. Constraints can be used to define rules on the format of data, ensure uniqueness in a table, ensure that data is actually entered into a column, and ensure that columns maintain integrity between tables. Five types of constraints can be used in SQL Server: 

- NOT NULL
- CHECK 
- UNIQUE
- PRIMARY KEY
- FOREIGN KEY

​	Constraints are very powerful tools if you use them correctly. 



**Stored Procedures** 

​	Stored procedures are groupings of SQL statements that have been compiled together into a single execution plan. These can be used to return data to the user and to achieve a consistent implementation of logic across applications. You can do a lot of things with stored procedures. The many advantages of using stored procedures include the following:

- SQL statements and logic that are used to perform similar tasks can be designed, coded, and tested at one place. Then, when applications need that functionality, all they have to do is to execute the stored procedure.
- Stored procedures can increase performance on the server by eliminating large amounts of network traffic required to execute large SQL scripts. Instead, all the client needs to do is to execute the single stored procedure. 
- Stored procedures can keep your users from having to know everything about the underlying table structure. All they need to know is that they have to execute a particular stored procedure to attain a specific result. 



**Triggers** 

​	Last but not least , you need to learn about triggers. Triggers are similar to stored procedures in that they are groupings of SQL statements. The major difference is how triggers are executed. Triggers are executed when a row is inserted, updated, or deleted from a table, depending on how the triggers were created. Triggers are a powerful way to enforce business rules when data is modified. A single table can have up to three different triggers on it. You can have a trigger that fires when an UPDATE occurs, one that fires when an INSERT occurs, and one that fires when a DELETE occurs. Triggers can be a way that the SQL Server automates business processes. For example, when an author has sold enough books to cover the advance that the publishing company paid, a trigger could be used to automatically begin calculating the **royalty（版税）** payments. Triggers fire after the record has been successfully modified in the table. If the modification fails because of a syntax error or constraint violation, the trigger is not fired. You need to be aware of one point of caution when dealing with triggers. Although triggers can be very powerful, they can also be very damaging to the performance of your server. Be very careful that you do not try to put too much functionality into your triggers because it will slow down response and can really frustrate your users. 