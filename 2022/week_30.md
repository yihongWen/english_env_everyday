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



## 07-20:

**Telecommunications and Computer：**

​	Telecommunications allows people around the world to contact one another, to access information instantly, and to communicate from remote areas. Telecommunications usually involves a sender of information and one or more recipients linked by a technology, such as a telephone system, that transmits information from one place to another. Telecommunications devices convert different types of information, such as sound and video, into electronic signals. The signals can then be transmitted by means of media such as telephone wires or radio waves. When a signal reaches its destination, the device on the receiving end converts the electronic signal back into an understandable message, such as sound over a telephone, moving images on a television, or words and pictures on a computer screen. Telecommunications enables people to send and receive personal messages across town, between countries, and to and from outer space. It also provides the key medium for news, data, information and entertainment. 

​	Telecommunications messages can be sent in a variety of ways and by a wide range of devices. The messages can be sent from one sender to a single receiver (point-to-point) or from one sender to many receivers (point-to-multipoint). Personal communications, such as a telephone conversation between two people or a **facsimile（传真）** (fax) message, usually involve point-to-point transmission. Point-to-multipoint telecommunications, often called broadcasts, provide the basis for commercial radio and television programming. 

​	Telecommunications begin with messages that are converted into electronic signals. The signals are then sent over a medium to a receiver, where they are decoded back into a form that the person receiving the message can understand. There are a variety of ways to create and decode signals, and many different ways to transmit signals. 

​	Devices such as the **telegraph（电报）** and telephone relay messages by creating **modulated（调制）** electrical **impulses（脉冲）**, or impulses that change in a systematic way. These impulses are then sent by wires, radio waves, or other media to a receiver that decodes the modulation. The telegraph, the earliest method of delivering telecommunications, works by converting the **contacts（接触）** (connections between two **conductors（导体）** that permit a flow of current) between a telegraph key and a metal conductor into electrical impulses. These impulses are sent along a wire to a receiver, which converts the impulses into short and long bursts of sound or into dots and dashes on a simple printing device. Specific sequences of dots and dashes represent letters of the alphabet. In the early days of the telegraph, these sequences were decoded by telegraph operators. In this way, telegraph operators could transmit and receive letters that spelled words. Later versions of the telegraph could **decipher（破译）** letters and numbers automatically. Telegraphs have been largely replaced by other forms of telecommunications, such as **fax machines（传真机）** and electronic mail (e-mail), but they are still used in some parts of the world to send messages. 

​	Telegraphs, telephones, radio, and television all work by modifying electronic signals, making the signals imitate, or **reproduce（复制、重现）**, the original message. This form of transmission is known as analog transmission. Computers and other types of electronic equipment, however, transmit digital information. Digital technologies convert a message into electronic form first by measuring different qualities of the message, such as the pitch and volume of a voice, many times. These measurements are then encoded into multiple series of binary numbers, or 1s and 0s. Finally, digital technologies create and send electrical impulses that correspond to the series of 1s and 0s. Digital information can be transmitted faster and more clearly than analog signals, because the electrical impulses only need to correspond to two digits and not to the full range of qualities that compose the original message, such as the pitch and volume of a human voice. While digital transmissions can be sent over wires, cables or radio waves, they must be decoded by a digital receiver. New digital telephones and televisions are being developed to make telecommunications more efficient. 

​	Most personal computers communicate with each other and with larger networks, such as the Internet, by using the ordinary telephone network. Since the telephone network functions by converting sound into electronic signals, the computer must first convert its digital data into sound. Computers do this with a device called a modem, which is short for **modulator（调制器）**/demodulator. A modem converts the stream of 1s and 0s from a computer into an analog signal that can then be transmitted over the telephone network, as a speaker’s voice would. The modem of the receiving computer demodulates the analog sound signal back into a digital form that the computer can understand. 

​	Telecommunications systems deliver messages using a number of different transmission media, including copper wires, fiber-optic cables, communication **satellites（卫星）**, and microwave radio. One way to categorize telecommunications media is to consider whether or not the media uses wires. Wire-based (or wireline) telecommunications provide the initial link between most telephones and the telephone network, and are a reliable means for transmitting messages. Telecommunications without wires, commonly referred to as wireless communications, use technologies such as cordless telephones, cellular radio telephones, walkie-talkies, citizens band (CB1 ) radios, pagers, and satellites. Wireless communications offer increased mobility and flexibility. 

​	Individual people, businesses, and governments use many different types of telecommunications systems. Some systems, like the telephone system, use a network of cables, wires, and switching stations for point-to-point communication. Other systems, such as radio and television, broadcast signals through space, which can be received by anyone who has a device to receive them. Some systems make use of several types of media to complete a transmission. For example, a telephone call may travel by means of copper wire, fiber-optic cable, and radio waves as the call is sent from sender to receiver. All telecommunications systems are constantly evolving as telecommunications technology improves. 

​	Computer telecommunications, with the ability to send and receive audio, video, text, software, and multimedia, is one of the fastest-growing segments of the telecommunications market. Computer telecommunications takes advantage of existing telephone connections to transmit digital data. This type of transmission is frequently done over the Internet, a decentralized network of personal, business, government, educational computers, and sources of information. Some computers connect directly to the digital portion of the telephone network using the Integrated Services Digital Network (ISDN), but this requires the installation of special devices and telephone line conditioning. An improved modem system for regular phone lines, called Digital Subscriber Line (DSL1 ), is being developed to increase modem speed tremendously. 

​	Electronic mail, or e-mail, is a key attraction of the Internet and a common form of computer telecommunications. E-mail is a text-based message delivery system that allows information such as typed messages and multimedia to be sent to individual computer users. Local e-mail messages (within a building or a company) typically reach addressees by traveling through wire-based internal networks. E-mail that must travel across town or across a country to reach the final destination usually travels through the telephone network. Other computer telecommunications technologies that businesses frequently use include automated banking terminals and devices for credit card transactions that bill charges directly to a customer’s bank account. 

​	Personal computers have pushed the limits of the telephone system as more and more complex computer messages are being sent over telephone lines, and at rapidly increasing speeds. This need for speed has encouraged the development of digital transmission technology. Innovations in fiber-optic technology will hopefully keep up with the growing use of personal computers for telecommunications. The next generation of cellular telephones, pagers, and televisions will also benefit from the speed and clarity of digital telecommunications. 

​	Telecommunications and information technologies are merging and converging. This means that many of the devices that we associate with only one function may evolve into more versatile equipment. This convergence is already happening in various fields. Some telephones and pagers are able to store not only phone numbers but also names and personal information about callers. Advanced phones with keyboards and small screens are now in development that can access the Internet and send and receive e-mail. Personal computers can now access information and video entertainment and are in effect becoming a combined television set and computer terminal. Television sets, which we currently associate with broadcast and cable-delivered video programming, are able to gain access to the Internet through add-on appliances. Future modifications and technology innovations may **blur（模糊）** the distinctions between appliances even more. 

​	Convergence of telecommunications technologies will also trigger a change in the content available and the composition of the content provider. Both television and personal computers will be incorporating new multimedia, interactive, and digital features. For example, an entertainment program might have on-screen pointers to World Wide Web pages containing more information about the actors. **In the near term（在短期内）** , before the actualization of a fully digital telecommunications world, devices like modems will still be necessary to provide an essential link between the old analog world and the upcoming digital one. 

