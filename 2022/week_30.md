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





## 07-21:

**Internet and Information Superhighway** 

​	Networks have become a fundamental, if not the most important, part of today’s information systems. They form the **backbone（脊柱、骨干）** for information sharing in enterprises, and in governmental and scientific groups. That information can take several forms. It can be notes and documents, data to be processed by another computer, files sent to colleagues, and even more **exotic（奇异）** forms of data. 

​	Most of these networks were installed in the late 60s and 70s, when network design was the “s**tate of the art（最新水平、发展水平）**” topic of computer research and sophisticated implementers. It resulted in multiple networking models such as packet-switching technology, collision-detection local area networks, hierarchical enterprise networks, and many other excellent technologies. 

​	From the early 70s on, another aspect of networking became important: protocol layering, which allows applications to communicate with each other. A complete range of architectural models were proposed and implemented by various research teams and computer manufacturers. 

​	The result of all this great **know-how（技术、实际知识）** is that today any group of users can find a physical network and an architectural model suitable for their specific needs. This ranges from cheap asynchronous lines with no other error recovery than a bit-per-bit **parity（奇偶校验）** function, through full-function wide area networks (public or private) with reliable protocols such as public packet-switching networks or private SNA networks, to high-speed but limited-distance local area networks. 

​	The down side of this exploding information sharing is the rather painful situation when one group of users wants to extend its information system to another group of users who happen to have a different network technology and different network protocols. As a result, even if they could agree on a type of network technology to physically interconnect the two locations, their applications (such as mailing systems) still would not be able to communicate with each other because of the different protocols. 

​	This situation was recognized rather early (beginning of the 70s) by a group of researchers in the U.S. who came up with a new principle: internetworking. Other official organizations became involved in this area of interconnecting networks, such as ISO. All were trying to define a set of protocols, layered in a well-defined suite, so that applications would be able to talk to other applications, regardless of the underlying network technology and the operating systems where those applications run. 



**Internetworks** 

​	Those original designers, funded by the Defense Advanced Research Projects Agency (DARPA2 ), of the ARPANET3 protocol suite introduced fundamental concepts such as layering and virtualizing in the world of networking, well before ISO even took an interest in networking. 

​	The official organization of those researchers was the ARPANET Network Working Group, which had its last general meeting in October 1971. DARPA continued its research for an internetworking protocol suite, from the early NCP (Network Control Program) host-to-host protocol to the TCP/IP protocol suite, which took its current form around 1978. At that time, DARPA was well known for its pioneering of packet-switching over radio networks and satellite channels. The first real implementations of the Internet were found around 1980 when DARPA started converting the machines of its research network (ARPANET) to use the new TCP/IP protocols. In 1983, the transition was completed and DARPA demanded that all computers willing to connect to its ARPANET use TCP/IP. 

​	DARPA also contracted Bolt, Beranek, and Newman to develop an implementation of the TCP/IP protocols for Berkeley UNIX on the VAX1 and funded the University of California at Berkeley2 to distribute that code free of charge with their UNIX operating system. The first release of the Berkeley Software Distribution to include the TCP/IP protocol set was made available in 1983 (4.2BSD). **From that point on（从那时起）,** TCP/IP spread rapidly among universities and research centers and has become the standard communications subsystem for all UNIX connectivity. The second release (4.3BSD) was distributed in 1986, with updates in 1988 and 1990. 4.4BSD was released in 1993. Due to funding constraints, 4.4BSD was the last release of the BSD by the Computer Systems Research Group of the University of California at Berkeley. 

​	As TCP/IP internetworking spread rapidly, new wide area networks were created in the U.S. and connected to ARPANET. In turn, other networks in the rest of the world, not necessarily based on the TCP/IP protocols, were added to the set of interconnected networks. The result is what is described as the Internet. Some examples of the different networks that have played key roles in this development are described in the next sections. 



**The Internet** 

​	What exactly is the Internet? First, the word internet 3 (also internetwork) is simply a contraction of the phrase interconnected network. However, when written with a capital “I” the Internet refers to a worldwide set of interconnected networks, so the Internet is an internet, but the reverse does not apply. The Internet is sometimes called the connected Internet. The Internet consists of the following groups of networks: 

- Backbones: large networks that exist primarily to interconnect other networks. Currently the backbones are NSFNET1 in the US, EBONE2 in Europe, and large commercial backbones. 
- Regional networks connecting, for example, universities and colleges. 
- Commercial networks providing access to the backbones to subscribers, and networks owned by commercial organizations for internal use that also have connections to the Internet. 
- Local networks, such as campus-wide university networks. 

​	In many cases, particularly for commercial, military and government networks, traffic between these networks and the rest of the Internet is restricted. 



**Information Superhighway** 

​	One recent and important **initiative（倡议）** was the creation of the U.S. **Advisory（顾问）** Council on the National Information Infrastructure (NIIAC3 ) headed by U.S. **Vice（副的）** President Al Gore4 (who has been credited with coining the phrase “information superhighway”). The Advisory Council, which was made up of representatives from many areas of industry, government, entertainment and education, met for a period of two years from 1994-6. At the end of their term, they concluded their work with the publishing of two major reports: 

- **Kickstart（启动）** Initiative: Connecting America’s Communities to the Information Superhighway
- A Nation of Opportunity: Realizing the Promise of the Information Superhighway 

​	Among the findings in these reports is the goal that every person in the U.S. should have access to the Internet by the year 2005, with all schools and libraries being connected by the year 2000. Although the reports do not specify direct government funding for expansion of the Internet, preferring “commercial and competitive initiatives” to be the driving force, it does give a responsibility to all levels of government to ensure fair access and remove **regulatory obstacles（监管障碍）**. Both reports may be found at: http://www.benton.org/contents.html

​	From a more international perspective, the Group of Seven (G71 ) ministers met in Brussels2 in February 1995 to discuss the emerging Global Information Infrastructure (GII3 ). The conference was attended by science, technology and economic ministers of Canada, the United Kingdom, France, Japan, Germany, Italy and the United States, and focused on technological, cultural and economic issues regarding the development of an international infrastructure. Both the NIIAC and the GII described above were important initiatives which increased acceptance, and encouraged further growth, of the Internet.

​	Another **substantive（实质性）** government **affirmation（肯定）** for the Internet came, in 1996, in the form of the Next Generation Internet initiative. This was launched by the Clinton administration with the goals of: 

- Connecting universities and national labs with networks that are 100-1000 times faster than today’s (as of5 October 1996) Internet. 
- Promote experimentation with the next generation of networking technologies.
-  Demonstrate new applications that meet important national goals and missions. 

​	The initiative included funding of $100 million for 1998



**Future of the Internet** 

​	Trying to predict the future of the Internet is not an easy task. Few would have imagined even say , three years ago, the extent to which the Internet has now become a part of everyday life in business, homes and schools. There are a number of things, however, about which we can be fairly certain. 

​	Bandwidth requirement will continue to increase at massive rates; not only is the number of Internet users growing rapidly, but the applications being used are becoming more advanced and therefore need more bandwidth. This is the reason why the number of core (backbone) service providers has grown from four in 1995 to around 48 today (whereas the number of Internet connection providers has grown only moderately). However, new technologies such as Dense Wave Division Multiplexing (DWDM1 ) will help to get the most bandwidth from currently installed fiber. Today it is possible to hear radio stations from almost any part of the globe via the Internet. Today this is at around AM quality. Soon FM-quality radio and video-on-demand will be driving the bandwidth requirement.

​	Many businesses have already completed an experimental period of Internet access and are moving towards using the Internet for serious business use both intra- and inter-company. This has been made possible by the rapid advances in TCP/IP security technologies made in only the last one to two years. In the not too distant future, the availability of private, secure high bandwidth networking from Internet providers may well make many companies question the **feasibility（可行性）** of their current in-house wide area networks. Today we already have Voice over IP technology. As this technology **matures（成熟）** we are almost certain to see a sharing of bandwidth between voice and data across the Internet. This raises some interesting questions for phone companies. The cost to a user of an Internet connection between New York and Japan is the same as a connection within New York—not so a phone connection. This, and the fact that the Internet is **deregulated（解除管制）**, will raise many interesting questions in the years to come. 



## 07-22:

**ATM and Its Advantages** 

**What Is ATM?** 

​	The Asynchronous Transfer Mode (ATM) is a packet switching and multiplexing technique. Even though the word “asynchronous” appears in its description, it is not in any way an asynchronous transmission procedure. Because of the way it has been designed, it is particularly suitable for high-bandwidth and low-delay applications. With ATM, information is sent out in fixed-size packets or cells, each containing in its header a VCI that provides a means for creating multiple logical channels and multiplexing them as needed. Because the cells have a fixed size, they may contain unused bits. 

​	ATM is actually a very simple protocol: it merely transfers data from one point to another, and does not, by itself, provide any error recovery. However, ATM has been designed to interoperate with other, existing protocols. In fact, it can accommodate almost any upper-layer protocols that support end-to-end error recovery. 

​	The complete ATM protocol stack is shown in Figure 8C-1. The higher-layer protocols shown in the **topmost（最顶端）** box are application-specific. For example, they could be the standard file transfer protocol at the application layer with transmission control protocol (TCP) at the transport layer and Internet protocol (IP) at the network layer. Or, they could be simply the network-layer protocol for call and connection controls with a suitable application layer on top. As the name implies, the ATM adaptation layer (AAL1 ) “adapts” the upper-layer packets to the ATM layer below. While the details might vary from one service to another (e.g., connectionless data services, connection-oriented data services, **constant-bit-rate（固定比特传输）** data services, variable-bit-rate data services, etc.), this adaptation is achieved by adding a header, a trailer, and some fill octets to the upper-layer packets and segmenting them into fixed-size ATM cells. Below this layer is the so-called ATM layer. This layer can be thought of as a link-layer protocol. However, in some respects, it is different from other link-layer protocols. For example, with the high-level data link control (HDLC1 ) or Q.921 link access procedures on the D channel (LAPD2 ) protocol, the length of a frame varies—it may vary from 2 octets to 256 octets. With the IEEE3 802.3 protocol, the length of a packet, excluding the **preamble（前同步码）** and sync bits, may be anywhere from 64 octets to 1518 octets. In ATM, cell length is fixed at 53 octets. Also, unlike the link-layer protocols, ATM does not provide for acknowledgment procedures at the receiver. Errors can be detected in a cell, but not corrected. It is assumed that the transmission medium is highly reliable. 

​	Blocks of user data of variable lengths from upper layers are passed to the ATM Adaptation Layer (AAL), which adds headers, trailers, padding octets, and/or cyclic redundancy check (CRC4 ) bits according to some rules that depend upon the service type. Each resulting data block is segmented into smaller blocks, which are then **encapsulated（封密的）** into 53-octet cells in the ATM layer. It is these ATM cells that are transmitted to the destination. Many different media-dependent, physical-layer interfaces can be used for ATM. 



**Advantages of ATM** 

​	There are many advantages of an ATM network. Some of them are listed below: 

**Label switching** 

​	The ATM protocol, like the **frame relay protocol（帧中继）**, is ideally suited for label switching. It works in the following way: in a traditional packet-switched network, when a packet arrives at a router, it examines its layer 3 header and routes the packet to the next hop along an appropriate route based upon the destination address. Since the network layer address generally contains much more information than would be required in making the routing decision, the layer 3 routing process is relatively complex. In label switching, the layer 3 address is mapped to a shorter identifier, which is called a label. It is important to emphasize here that a label is not an explicit address of an end-point. When the packet is routed to the next hop, the label is sent along with it as part of the header so that the router at the next hop can use it to derive subsequent routing information (see Figure 8C-2). In ATM, labels are formed with the 24-bit virtual path identifier (VPI1 ) and virtual channel identifier (VCI) fields

​	Label switching offers a number of advantages. First, since packets can now be routed using a label as an index into the switch memory to determine the next hop, and since labels are shorter than IP addresses, it is easier to build a label-switching router. Second, if IP packets are to be routed between any two end-points in an ATM network in the traditional way, either virtual circuits must be connected in a full **mesh（网状）** configuration among ATM switches, or cut-through switched virtual channels (SVCs2 ) must be established using an appropriate protocol. Label switching **obviates（排除）** the need for such mesh connections and reduces the number of peer routers that need to communicate with each other. Consequently, a label-switching network is cheaper and faster. Third, label switching in an ATM environment is similar in many respects to label switching in other protocols. It may, therefore, be possible to use common methods for packet forwarding and even network management. 

**Low latency**

​	An important feature of the ATM protocol is its low latency and **seamless（无缝）** capacity to span local area networks (LANs) and wide area networks (WANs). ATM’s low latency results from the fact that all packets in the ATM layer have a fixed length. To see this, consider Figure 8C-3 (a), which shows a server with three inputs. Assume that all packets have a fixed size, d. The packets on any input link may arrive randomly with respect to the other input lines. If the server scans the inputs every d seconds, which is the length of a packet, then the average service delay for any packet on any input is d/2 seconds. Perfect scheduling is possible here because the packet size is known a priori. For example, if the data rate on each input line is 25 Mb/s1 , then for 53-octet ATM cells, the service period is 16.96 microseconds, and the average delay is 8.48 microseconds. 

​	Next, consider the case where the size of a packet varies from some minimum value, say L, to a maximum value, M. This is shown in Figure 8C-3 (b) and is applicable to Ethernet. In this case, the server must scan the inputs frequently enough to match the length of the shortest packets; otherwise, these packets will be subjected to long delays. For example, if the packet size varies from 2 octets to 100 octets, the server should scan the inputs every 640 ns1 , which may be an **excessive burden（过载）** on the CPU. If the service period is increased to 16.96 microseconds, the average delay is about 13 times the size of the shortest packet. If all packets are fixed-length, scheduling of network resources is much easier. 



High-speed and high-bandwidth 

​	Because of its low latency, ATM is particularly suitable for applications that require high-speed transport and high bandwidths. For example, one can use ATM in a network backbone that interconnects traditional LANs such as Ethernets and token ring LANs. Currently, there are many high-speed LANs such as gigabit Ethernets and **metropolitan（大都市、本地、城域网）** area networks (MANs2 ) covering tens of kilometers in diameter using such protocols as fiber-distributed data interface (FDDI3 ) and distributed queue dual bus (DQDB4 ). ATM could very well form the basis of the new generation of high-speed LANs and MANs. Furthermore, ATM is equally suitable for applications that do not require high speed or high capacity. For example, currently, vendors are offering ATM switches at 25.6, 44.736, 51.84, 155, and 622 Mb/s bandwidths with various cabling types—two- or four-wire category 3 unshielded twisted pair (UTP5 ), multi-mode and single-mode fibers, and so on6 . 



**Integrated network** 

​	Normally, a packet protocol is only suitable for **bursty（突发性）**, variable-bit-rate services, and would not be able to transport information that is sensitive to delays. For example, the public-switched telephone network (PSTN7 ) can only transport circuit-switched information. An X.25 or frame relay network can handle only packet-switched data. The ATM protocol has been designed such that it can carry not only bursty, variable-bit-rate services, but also delay-sensitive information such as voice and video that would normally be carried by circuit-switched networks. In fact, over the last few years, a rich set of procedures and protocols that enable ATM to support many different services have been developed by the ATM Forum 1 —connection-oriented as well as connectionless, constant-bit-rate as well as variable, and they provide different qualities of service according to the application and customer needs. Thus, with ATM, it is possible to provide all different services with a single, integrated network. 



**Integrated access from customer premises** 

​	ATM provides a means for achieving integrated access to broadband services from public or private networks. Services such as compact disc (CD)-quality music, pay-per-view movie channels, high-definition TV, high-speed Internet data downloading, etc. can all be combined with traditional, circuit-switched voice and low-speed data services and then presented over a single ATM pipe to the customer premises, where a set-top box would demultiplex these services. The user could even request special services from a network provider using an upstream control channel. 



**Interworking with existing protocols and legacy LANs** 

​	There are many instances where new applications would almost certainly require the bandwidth and speed of an ATM network. One such example involves collaboration among different research organizations with high-resolution, high-bandwidth imaging data. The ATM network, if installed, would still be able to interwork with traditional data networking protocols and legacy LANs such as Ethernet, token ring, and FDDI. Thus, the existing network infrastructure needs to be augmented only when or where necessary, leading to a graceful but less expensive evolution to the new technology. 



**Bandwidth-on-demand** 

​	Bandwidth-on-demand is another **innate（先天）** benefit of ATM. In private networks, higher bandwidths can be requested by users. However, generally, they must be **provisioned（预分配）** through network managers, and cannot be assigned dynamically at connection setup time. With some private networks that are equipped with inverse multiplexing capability at both ends, it may be possible to request and obtain increased bandwidth dynamically. Even then, the range is rather limited. With ATM, users may request a desired bandwidth when originating a call, and the network would attempt to dynamically allocate the requested bandwidth only if the customer had subscribed to this feature at subscription time. Furthermore, for ATM networks, there are traffic and **congestion（拥塞）** control mechanisms in place which, in the event of congestion, allow the network to maintain the quality of service for each customer with minimum **degradation（退化）**. Thus, initially, one could install a network with only a minimum amount of reserve capacity, and add to the network only when the demand for bandwidth has grown to a point where it is no longer possible to provide each customer with the subscribed quality of service. 





## **07-23**

**Computer Networks:**

**INTRODUCTION** 

​	Computer networks, the widespread sharing of information among groups of computers and their users, are a central part of the information **age(时代)**. The popular **adoption（收养、使用）** of the personal computer (PC) and the local area network (LAN) during the 1980s has led to the capacity to access information on a distant database; download an application from overseas; send a message to a friend in a different country; and share files with a colleague—all from a personal computer. 

​	The networks that allow all this to be done so easily are sophisticated and complex entities. They rely for their effectiveness on many cooperating components. The design and deployment of the worldwide computer network can be viewed as one of the great technological wonders of recent decades. 



**MODEMS AND COMPUTER BUREAUX**

​	As recently as the 1970s, computers were expensive, **fragile（易碎的、易损坏的）** machines that had to be looked after by specialists and kept in a controlled environment. They could be used either by plugging in a terminal directly or by using a phone line and modem to gain access from a distance. Because of their high cost, they tended to be centralized resources to which a user had to arrange their own access. During this time, organizations that offered access time on a mainframe computer—computer bureaux—flourished. Computer networks during this period were not commercially available. Even so, one of the most significant developments to shape the modern world of technology was initiated at this time: experimentation by the US Defence Department in distributing computer resources to provide **resilience（复原）** against failure. This work is now known as the Internet. 



**LOCAL AREA NETWORKS**

​	One of the most dramatic events in computer networking has been the introduction and rapid growth of the local area network (LAN) as a way to standardize the system of linking computers used in office systems. As the name suggests, this is a means of connecting a number of computing elements together. At the simplest level, a LAN provides no more than a shared medium (such as a coaxial cable to which all computers and printers are connected) along with a set of rules that govern the access to that medium. The most widely used LAN, Ethernet, uses a mechanism called Carrier Sense Multiple Access-Collision Detect (CSMA-CD2 ). This means that each connected device can only use the cable when it has established that no other device is using it. If there is **contention（看法、观点）**, the device looking for a connection backs off and tries again later. The Ethernet transfers data at 10M bits/sec3 , which is fast enough to make the distance between devices insignificant. They appear to be connected directly to their destination. 

​	There are many different layouts (such as bus, star, ring) and a number of different access protocols for LANs. Despite this variety, all LANs share the feature that they are limited in range (typically they cover one building) and are fast enough to make the connecting network invisible to the devices that use it. 

​	In addition to providing shared access, modern LANs can also give users a wide range of sophisticated facilities. Management software packages are available to control the way in which devices are configured on the LAN, how users are administered, and how network resources are controlled. A widely adopted structure on local networks is to have a number of servers that are available to a (usually much greater) number of clients. The former, usually powerful computers, provide services such as print control, file sharing, and mail to the latter, which are usually personal computers. 



**ROUTERS AND BRIDGES** 

​	The facilities on most LANs are very powerful. Most organizations do not wish to have small isolated islands of computing facilities. They usually want to extend facilities over a wider area so that groups can work without having to be located. Routers and bridges are specialized devices that allow two or more LANs to be connected. The bridge is the more basic device and can only connect LANs of the same type. The router is a more intelligent component that can interconnect many different types of computer network. Many large companies have corporate data networks that are founded on a collection of LANs and routers. From the user’s point of view, this arrangement provides them with a physically diverse network that looks like one **coherent（连贯）** resource. 



**WIDE AREA NETWORKS** 

​	At some point, it becomes impractical to extend a LAN any further. Physical limitation sometimes drives this, but **more often than not（通常）** there are more convenient or cheaper ways to extend a computer network. Two major components in most real computer networks are the public telephone and data networks. These provide long distance links that extend a LAN into a wide area network. Nearly all of the national network operators offer services for the interconnection of computer networks. These services range from simple, low speed data links that work over the public telephone network to sophisticated high-speed data services that are **ideally（理想的）** suited to the interconnection of LANs. These high-speed data services are usually referred to as broadband connections. It is anticipated that they will provide the necessary links between LANs that make what is called the information superhighway a reality.



**DISTRIBUTED COMPUTING** 

​	It would be easy to assume that computers will all be able to work together once they have broadband connection. But how do you get computers made by different manufacturers in different countries to work together across the world? Until recently, most computers were built with their own interfaces and were structured their own unique way. A computer could talk to one of its own kind but would have difficulty communicating with a “foreigner”. There were only a privileged few with the time, knowledge, and equipment to extract what they wanted from a variety of computing resources. By the 1990s, the level of commonality across different computers reached the stage where they could interwork effectively. This allows virtually anyone to use a remote machine to good effect. The main contributors to this are: 

**Client Server** 

​	Instead of building computer systems as **monolithic(整体的、单一的)** systems, there is now general agreement that they should be constructed as client/server systems. The client (a PC user) requests a service (such as printing) and the server (a LAN-connected processor) provides it. This **consensus（共识）** view on the structure of a computer system means that there is a separation of functions previously bundled together. The implementation details that flow from a simple concept go a long way to enabling all computers to be treated uniformly. 

**Object Technology** 

​	Another way to build computer systems works from the **premise（前提、假设）** that they should be built from well-defined parts—objects which are encapsulated, defined, and implemented so that they can be independent agents. The adoption of objects as a means of building computer systems has helped to allow interchangeability of parts. 

**Open Systems** 

​	This term covers the general aim of building computer systems so that they can readily be interconnected, and hence distributed. In practice, open systems are all about **unbundling** all the complexities of a computer system and using similar structure across different systems. And this **entails（需要）** a mixture of standards (which tell the manufacturers what they should be doing) and **consortia（联合）** (groups of like-minded people who help them to do it). The overall effect is that they can talk to each other. The **ultimate（最终）** aim of all of the work in distributed systems is to allow anyone to buy computers from a number of different manufacturers, to site them wherever is convenient, to use broadband connections to link them, and to operate them as one cooperating machine that takes full advantage of the fast links.



**SECURITY AND MANAGEMENT** 

​	Having fast computer networks built of machines that can talk to each other is not the end of the story. The **spectres（幽灵）** of the “information superhighwayman ” and the “information superroadworks ” have yet to be dealt with. 

​	Security With ever increasing amounts of important information being **entrusted（委托）** to ever more distributed computers, computer security becomes ever more important. In a highly distributed system it would be all too easy for an informed superhighwayman to access **confidential（机密）** information without being seen. The Data Encryption System (DES1 ) standard for protecting computer data, introduced in the late 1970s, has more recently been supplemented by “public key” systems that allow users to **scramble（打乱、变化）** and **unscramble** their messages easily without a third party intruding. 

​	Management It is a full-time job to keep a LAN operating as it should. Keeping a computer network that is distributed across the world running smoothly takes the challenge of network management a step further. The essential concepts for managing distributed and diverse networks have received a lot of attention lately. There are now enough tools and standards for this important aspect of computer networks to allow global networks to be supervised effectively.



## 07-24:

**Switched LAN Network Designs** 

​	A successful switched internetworking solution must combine the benefits of both routers and switches in every part of the network, as well as offer a flexible evolution path from shared-media networking to switched internetworks. In general, incorporating switches in campus network designs results in the following benefits: 

- High bandwidth 
- Quality of service (QoS) 
- Low cost 
- Easy configuration 

​	Switching and bridging sometimes can result in **nonoptimal(非最优)** routing of packets. This is because every packet must go through the root bridge of the spanning tree. When routers are used, the routing of packets can be controlled and designed for optimal paths. Cisco now provides support for improved routing and redundancy in switched environments by supporting one instance of the spanning tree per VLAN . 



General Network Design Principles 

​	Good network design is based on many concepts that are summarized by the following key principles: 

- Examine single points of failure carefully—There should be redundancy in the network so that a single failure does not isolate any portion of the network. There are two aspects of redundancy that need to be considered: backup and load balancing. In the event of a failure in the network, there should be an alternative or backup path. Load balancing occurs when two or more paths to a destination exist and can be utilized depending on the network load. The level of redundancy required in a particular network varies from network to network.
- Characterize application and protocol traffic—For example, the flow of application data will profile client-server interaction and is crucial for efficient resource allocation, such as the number of clients using a particular server or the number of client workstations on a segment.
- Analyze bandwidth availability—For example, there should not be an **order of magnitude（数量级）** difference between the different layers of the hierarchical model. It is important to remember that the hierarchical model refers to conceptual layers that provide functionality. The actual **demarcation（界限）** between layers does not have to be a physical link—it can be the backplane of a particular device.
- Build networks using a hierarchical or modular model—The hierarchy allows autonomous segments to be internetworked together. 



​	Figure 9B-1 shows a high-level view of the various aspects of a hierarchical network design. A hierarchical network design presents three layers—core, distribution, and access—with each layer providing different functionality. 

​	The core layer is a high-speed switching backbone and should be designed to switch packets as fast as possible. This layer of the network should not perform any packet manipulation access lists and filtering that would slow down the switching of packets. 

​	The distribution layer of the network is the demarcation point between the access and core layers and helps to define and differentiate the core. The purpose of this layer is to provide boundary definition and is the place at which packet manipulation can take place. In the campus environment, the distribution layer can include several functions, such as the following: 

- Address or area aggregation
- Departmental or workgroup access
- Broadcast/multicast domain definition
- VLAN routing
- Any media transitions that need to occur
- Security

​	In the non-campus environment, the distribution layer can be a **redistribution（重新分配）** point between routing domains or the demarcation between static and dynamic routing protocols. It can also be the point at which remote sites access the corporate network. The distribution layer can be summarized as the layer that provides policy-based connectivity

​	The access layer is the point at which local end users are allowed into the network. This layer may also use access lists or filters to further optimize the needs of a particular set of users. In the campus environment, access-layer functions can include the following:

- Shared bandwidth
- Switched bandwidth
- MAC layer filtering
-  Microsegmentation 

​	In the non-campus environment, the access layer can give remote sites access to the corporate network via some wide-area technology, such as Frame Relay, ISDN, or leased lines. It is sometimes mistakenly thought that the three layers (core, distribution, and access) must exist in clear and distinct physical entities, but this does not have to be the case. The layers are defined to aid successful network design and to represent functionality that must exist in a network. The instantiation of each layer can be in distinct routers or switches, can be represented by a physical media, can be combined in a single device, or can be omitted altogether. The way the layers are implemented depends on the needs of the network being designed. Note, however, that for a network to function optimally, hierarchy must be maintained. With respect to the hierarchical model, traditional campus LANs have followed one of two designs—single router and distributed backbone—as shown in Figure 9B-2. 

​	In the single-router design, the core and distribution layers are present in a single entity—the router. Core functionality is represented by the backplane of the router and distribution is represented by the router. Access for end users is through individual- or chassis-based hubs. This design suffers from scalability constraints because the router can only be in one physical location, so all segments end at the same location—the router. The single router is responsible for all distribution functionality, which can cause CPU overload. The distributed backbone design uses a high-speed backbone media, typically FDDI, to spread routing functionality among several routers. This also allows the backbone to traverse floors, a building, or a campus. 



**Switched LAN Network Design Principles** 

​	When designing switched LAN campus networks, the following factors must be considered:

- Broadcast radiation—Broadcast radiation can become fatal—that is, 100 percent of host CPU cycles can be consumed by processing broadcast and multicast packets. Because of delays inherent in **carrier sense multiple access collision detect** (CSMA/CD) technologies, such as Ethernet, any more than a small amount of broadcast traffic will adversely affect the operation of devices attached to a switch. Although VLANs reduce the effect of broadcast radiation on all LANs, there is still a scaling issue as to how many hosts should reside on a given VLAN. A router allows for larger network designs because a VLAN can be subsegmented depending on traffic patterns. However, in a nonoptimal network design, a single router can be burdened with large amounts of traffic.
-  Well-behaved VLANs—A well-behaved VLAN is a VLAN in which 80 percent or more of the traffic is local to that VLAN. In an example in which the Marketing, MIS , and Engineering departments each have an individual VLAN segment, the 80 percent rule is violated when a user in the Marketing VLAN reads mail from the MIS VLAN, mounts servers from the Engineering VLAN, and sends e-mail to members of the Engineering VLAN. 
- Available bandwidth to access routing functionality—Inter-VLAN traffic must be routed, so the network design must allocate enough bandwidth to move inter-VLAN traffic from the source, through the device that provides routing functionality, and to the destination. 
- Appropriate placement of administrative boundaries—Switching has the effect of flattening networks, and the deployment of switching outside of your administrative boundary can **adversely（不利的）** affect the network within your administrative boundary. 

​	Campus network designs are evolving rapidly with the deployment of switching at all levels of the network—from the desktop to the backbone. Three topologies have emerged as generic network designs: 

- Scaled Switching 

- Large Switched/Minimal Routing

- Distributed Routing/Switching 



Scaled Switching 

​	The scaled switching design shown in Figure 9B-3 deploys switching at all levels of the network without the use of routers. In this design, each layer consists of switches, with switches in the access layer providing 10-Mbps1 Ethernet or 16-Mbps Token Ring to end users. Scaled switching is a low-cost and easy-to-install solution for a small campus network. It does not require knowledge of address structure, is easy to manage, and allows all users to communicate with one another. However, this network comprises a single broadcast domain. If a scaled switched network needs to grow beyond the broadcast domain, it can use VLANs to create multiple broadcast domains. Note that when VLANs are used, end users in one VLAN cannot communicate with end users in another VLAN unless routers are deployed. 

Large Switched/Minimal Routing 

​	The large switched/minimal routing design deploys switching at the access layer of the network, either ATM switching or LAN switching at the distribution layer of the network, and ATM/LAN switching at the core. Figure 9B-4 shows an example of this network design. 

​	In the case of ATM in the distribution layer, the following key issues are relevant:

- LANE2 support on routers and switches. 
- Support for UNI3 3.X signaling (including point-to-multipoint). 



If redundancy is provided by a virtual PVC4 or SVC5 mesh, the mesh is a single point of failure. In the case of LAN switching in the distribution layer, the following key issues are relevant:

- Support for VLAN trunking technology in each device. 
- The switches in the distribution layer must run the Spanning-Tree Protocol to prevent loops, which means that some connections will be blocked and load balancing cannot occur. 

​	To scale the large switched/minimal routing design, a logical hierarchy must be imposed. The logical hierarchy consists of VLANs and routers that enable inter-VLAN communication. In this topology, routing is used only in the distribution layer, and the access layer depends on bandwidth through the distribution layer to gain access to high-speed switching functionality in the core layer. The large switched/minimal routing design scales well when VLANs are designed so that the majority of resources are available in the VLAN. Therefore, if this topology can be designed so that 80 percent of traffic is intra-VLAN and only 20 percent of traffic is inter-VLAN, the bandwidth needed for inter-VLAN routing is not a concern. However, if inter-VLAN traffic is greater than 20 percent, access to routing in the core becomes a scalability issue. For optimal network operation, scalable routing content is needed at the distribution layer of the network. 

Distributed Routing/Switching 

​	The distributed routing/switching design deploys switching in the access layer, routing in the distribution layer, and some form of high-speed switching in the core layer, as shown in Figure 9B-5. The distributed routing/switching design follows the classic hierarchical network model both physically and logically. Because it provides high bandwidth for access to routing functionality, this design scales very well. This design is optimized for networks that do not have the 80/20 pattern rule. If servers are centralized, most traffic is inter-VLAN; therefore, high routing content is needed. 





