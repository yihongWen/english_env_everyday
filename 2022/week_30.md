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







## 07-19:

**Delphi Database Architecture** 

​	Database applications are built from user interface elements, components that manage the database or databases, and components that represent the data contained by the tables in those databases (datasets). How you organize these pieces is the architecture of your database application. 

​	By isolating database access components in data modules, you can develop forms in your database applications that provide a consistent user interface. By storing links to well-designed forms and data modules in the Object Repository as illustrated in Figure 7C-1, you and other developers can build on existing foundations rather than **starting over(从头开始)** from scratch for each new project. Sharing forms and modules also makes it possible for you to develop corporate standards for database access and application interfaces. 

​	Many aspects of the architecture of your database application depend on the type of database you are using, the number of users who will be sharing the database information, and the type of information you are working with. 

​	When writing applications that use information that is not shared among several users, you may want to use a local database in a single-tiered application. This approach can have the advantage of speed (because data is stored locally), and does not require the purchase of a separate database server and expensive site licenses. However, it is limited in how much data the tables can hold and the number of users your application can support. Writing a two-tiered application provides more multi-user support and lets you use large remote databases that can store far more information. 

​	When the database information includes complicated relationships between several tables, or when the number of clients grows, you may want to use a multi-tiered application. Multi-tiered applications include middle tiers that centralize the logic which governs your database interactions so that there is centralized control over data relationships. This allows different client applications to use the same data while ensuring that the data logic is consistent. They also allow for smaller client applications because much of the processing is off-loaded onto middle tiers. These smaller client applications are easier to install, configure, and maintain because they do not include the database connectivity software. Multi-tiered applications can also improve performance by spreading the data-processing tasks over several systems. 



**Planning for Scalability** 

​	The development process can get more involved and expensive as the number of tiers increases. Because of this, you may wish to start developing your application as a single-tiered application. As the amount of data, the number of users, and the number of different applications accessing the data grow, you may later need to **scale up（扩大、按比例增加）**  to a multi-tiered architecture. By planning for scalability, you can protect your development investment when writing a single- or two-tiered application so that the code can be reused as your application grows

​	The VCL data-aware components make it easy to write scalable applications by abstracting the behavior of the database and the data stored by the database. Whether you are writing a single-tiered, two-tiered, or multi-tiered application, you can isolate your user interface from the data access layer as illustrated in Figure 7C-2. 

​	A form represents the user interface, and contains data controls and other user interface elements. The data controls in the user interface connect to datasets which represent information from the tables in the database. A data source links the data controls to these datasets. By isolating the data source and datasets in a data module, the form can remain unchanged as you scale your application up. Only the datasets must change. Note some user interface elements require special attention when you are planning for scalability. For example, different databases enforce security in different ways. When you are using Delphi’s data access components (whether they use the BDE , ADO , or InterBase Express ) it is easy to scale from one-tiered to two-tiered. Only a few properties on the dataset must change to direct the dataset to connect to an SQL server rather than a local database. A flat-file database application is easily scaled to the client in a multi-tiered application because both architectures use the same client dataset component. In fact, you can write an application that acts as both a flat-file application and a multi-tiered client. If you plan to scale your application up to a three-tiered architecture eventually, you can write your one- or two-tiered application with that goal in mind. In addition to isolating the user interface, isolate all logic that will eventually reside on the middle tier so that it is easy to replace at a later time. You can even connect your user interface elements to client datasets (used in multi-tiered applications), and connect them to local versions of the InterBase-, BDE- or ADO-enabled datasets in a separate data module that will eventually move to the middle tier. If you do not want to introduce this **artifice（诡计、欺骗）** of an extra dataset layer in your one- and two-tiered applications, it is still easy to scale up to a three-tiered application at a later date. 

**Single-Tiered Database Applications** 

​	In single-tiered database applications, the application and the database share a single file system. They use local databases or files that store database information in a flat-file format. A single application comprises the user interface and incorporates the data access mechanism (either the BDE or a system for loading and saving flat-file database information). The type of dataset component used to represent database tables depends on whether the data is stored in a local database (such as Paradox1 , dBASE2 , Access3 , or FoxPro4 ) or in a flat file. Figure 7C-3 illustrates these two possibilities. 

**Two-Tiered Database Applications**

​	In two-tiered database applications, a client application provides a user interface to data, and interacts directly with a remote database server. Figure 7C-4 illustrates this relationship. 

​	In this model, all applications are database clients. A client requests information from and sends information to a database server. A server can process requests from many clients **simultaneously（同时的）**, coordinating access to and updating of data. 

​	Multi-Tiered Database Applications In multi-tiered database applications, an application is partitioned into pieces that reside on different machines. A client application provides a user interface to data. It passes all data requests and updates through an application server (also called a “remote data broker”). The application server, in turn, communicates directly with a remote database server or some other custom dataset. Usually, in this model, the client application, the application server, and the remote database server are on separate machines. Figure 7C-5 illustrates these relationships for different types of multi-tiered applications. 

​	You can use Delphi to create both client applications and application servers. The client application uses standard data-aware controls connected through a data source to one or more client dataset components in order to display data for viewing and editing. Each client dataset communicates with an application server through an IappServer interface that is implemented by the application server’s remote data module. The client application can use a variety of protocols (TCP/IP, HTTP, DCOM , MTS , or CORBA) to establish this communication. The protocol depends on the type of connection component used in the client application and the type of remote data module used in the server application. The application server contains provider components that mediate the communication between client datasets on the client application and the datasets on the application server. All data is passed between the client application and the provider components through the IAppServer interface. Usually, several client applications communicate with a single application server in the multi-tiered model. The application server provides a gateway to your databases for all your client applications, and it lets you provide enterprise-wide database tasks in a central location, accessible to all your clients. 