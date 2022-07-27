## 07-25:

**How Are Networks Used?** 

​	The fundamental purpose of networks—sharing resources—has evolved over the years to **encompass(包含)** many diverse tasks, and new applications for networking are being developed all the time. In the following sections, we discuss the more popular uses for today’s computer networks. 



**File Sharing** 

​	The oldest and most **ubiquitous（普遍存在的）** use for networks is sharing data files. One approach to sharing files involves placing the file in a shared location on one computer (acting as a server), and making it available to other computers (acting as clients) on the network. Other users who want access to the file can either open the shared copy directly or copy it over the network to their own local hard disks. Some database applications use file sharing to store a centralized database file on a server, allowing many users to view and update the file simultaneously. To accommodate this type of application, most NOSs provide functions that enable the application to lock the shared data at the file or data record level. The application can then coordinate access to the data and prevent database updates from stepping on each other



**Printer Sharing** 

​	Traditionally, printers are relatively expensive devices. **No matter what era（无论在什么年代）** of personal computing you look at, high-end printers can cost more than two or three client computers. (Of course, what constitutes a high-end printer has changed over time.) As a result, sharing printers became a primary use of networks early on —a tradition that survives today. To share a printer, you physically connect the printer to a computer acting as a server. (Printers are usually connected directly to the computer’s printer port, also called a parallel port.) Using the NOS, you share the printer over the network. Users can then print to your shared printer as easily as if the printer were directly connected to their own local PCs. Rather than going out the local printer port, the user’s data to be printed travels across the network to the server, and the server sends the data directly to its attached printer. Printer sharing is so **pervasive（普遍）** that some printer manufacturers (for example, Hewlett-Packard3 ) have developed printers that you can directly attach to the network—no server computer required. These printers are sometimes called network printers, because they include a built-in interface to the network. From a user’s perspective, network printers appear and behave just like printers shared by servers on the network. 



**Drive Sharing** 

​	When large hard disks and CD-ROM drives were relatively expensive devices, network users attached them to servers and shared them over the network. Users could access the contents of one or more shared CD-ROMs, or store and retrieve their own data in a directory on the server’s hard disk. A single hard disk might accommodate many users, each with his or her own private directory. This approach kept the cost of individual PCs lower, and the extra cost of server hardware was spread across many users. As prices of hard disks and CD-ROM drives fell, the tide shifted in the direction of equipping each client computer with plenty of local storage and its own CD-ROM drive. However, more recent trends in cost **reduction（减小、压缩）** in some organizations have begun to push the storage devices back to the server, allowing the use of very inexpensive client PCs. Some low-cost client computers don’t even contain hard disks; they rely entirely on storage space supplied by network servers. These low-cost clients are sometimes called diskless workstations. In addition to drives and printers, you can share other devices. All you need is the right device and the right software. For example, intelligent fax machines, modems, scanners, and other devices have been shared over computer networks. We won’t go into the details of each device here. Just remember that the device-sharing concept can reach beyond printers and drives. 



**Application Sharing**

​	In its simplest form, application sharing is nothing more than file sharing, where the files just happen to be the executable application files themselves. Instead of installing and running an application on a local hard disk, you place the application once on a server. Users then load and run the application over the network. Keep in mind that not all software vendors design their applications to run in this type of shared environment. Another aspect of application sharing involves placing a data file on a server and sharing it among several applications running on the network. (The application files themselves may or may not be shared.) In this environment, the application’s role includes coordinating all access to the shared data file. For example, a group scheduling application running on several networked PCs might store all scheduling data in a single shared file on a server. Likewise, some e-mail applications store all e-mail messages in a set of shared files on a single server computer. Some applications have two distinct parts—a client portion and a server portion. The two parts play specific roles in performing the application’s function. This approach is known as the client-server application model, or simply client-server. A server application lives on a server computer and runs there exclusively. The client side of the application resides on a client computer and provides the user interface to the server part. The two parts of the application coordinate and exchange data over the network. A good example of this approach is Microsoft SQL Server, a client-server database application that runs on Windows NT Server. One piece of the application runs on a Windows NT Server computer and provides all access to the contents of a database. The client piece runs on each client computer, and makes requests to the server over the network. 



**Remote Access**

​	More and more users these days are hitting the road with their laptop PCs in hand. At the same time, many other users are **opting（选择）** to skip the long **commute（通勤）** and work from home while **staying in touch** with the office. (Working at home and communicating with the office electronically has become known as **telecommuting（远程办公）**.) As all of these users become increasingly dependent on their networks at the office, the need to connect their computers from remote locations has become significantly more important over the last few years. Remote access is a generic term that actually refers to several alternative approaches. In the following sections, we discuss the most popular remote access techniques. 

- **REMOTE E-MAIL ACCESS**

​	If users need only to send and receive electronic mail messages, they can use a modem to dial in to an e-mail server at the office. Once connected, they can pick up their e-mail messages and compose and send messages to other users. This is a fairly straightforward task, but doesn’t give the user access to any other shared network resources. 

- **REMOTE CONTROL** 

​	If users need remote access to files on their desktop PCs at the office, they can implement an approach called remote control. This approach to remote access requires a special software package that runs on both the remote computer and on the user’s office PC. The software enables the user to take remote control of the office PC. The remote user’s keyboard, mouse, and video display act as if they’re directly attached to the PC at the office. The remote control software sends keyboard and mouse actions to the office PC, and receives changes in the display from the office PC. Each remote user takes control of exactly one PC on the office LAN, so each remotely controlled PC requires its own modem and copy of the remote control software. PC AnyWhere from Symantec is an example of remote control software.

 **REMOTE NODE** 

​	Users who need full access to shared resources on the LAN at the office must use a remote access approach called remote node. (A node refers to a computer or other device that’s directly attached to the network.) Most modern NOSs, including Windows 98, provide some form of remote node capability. With this approach, users can dial in to a remote access server at the office. Once they’re connected, they have complete access to the network—just as if their remote PC were directly connected to the network. Users can remotely access whatever shared resources they would normally be able to access at work. Remote nodes (remote access clients) can dial in to a single remote access server and have a virtual connection to the LAN. In contrast to remote control, the remote node approach funnels all remote users through a single server on the network. In the Microsoft world, remote node is referred to alternatively as RAS 3 (Remote Access Service) and DUN 4 (Dial-Up Networking). Windows 95 included remote access client software, and the Microsoft Plus!5 pack added a single-modem remote access server. Windows 98 includes both the client and server components, as does Windows NT Workstation. Windows NT Server includes the complete form of RAS, which can handle up to 256 simultaneous remote nodes (that is, when it’s equipped with up to 256 modems). 







## 07-26:

**Network Topologies** 

​	Networks require both network adapter hardware in each device to be connected, and some physical (or wireless) connection to hook them all together. If you consider a two-node network, you can think of the network adapters as the tin cans, and the connection as the string between them. But most real-world networks include more than two nodes, and this leads to many different ways to string them together. The arrangement of network nodes and connections between them is called the network’s topology. It’s simply a map of the layout of nodes and connections in the network. Three network topologies **predominate（占主导地位的）** today—namely, bus, star, and ring. 



**Bus Topology** 

​	In the bus network topology, you connect each node to the network along a single piece of network cable, called abus. (If you’re familiar with the term bus in the context of **motherboards（主板）**, the idea is similar. The bus provides the path for the data, and devices **tap into（接入）** the bus along its length to communicate with other devices.) As shown in Figure 10A-1, network nodes essentially tap into the bus at convenient locations along the way. Data travels from a node out onto the bus until it reaches the ends of the cable. **At each end of the bus, a device called a terminator is installed to prevent data signals from reflecting back onto the bus and causing errors.** A terminator is a special **resistor（电阻）** device that’s attached to an electrical ground. When the transmitted data hits the terminator, it doesn’t go any farther. **Reliability of the bus topology can be a problem in all but the smallest networks. If the single cable acting as the bus is severed at any point, the entire network can go down.** Even if many of the nodes are still connected to each other on the bus, a severed cable is no longer terminated correctly. Although it’s the lowest cost topology to implement, I don’t recommend selecting the bus topology unless you’re dealing with a total of three or four computers in the same room, and all the network cabling is easily accessible. 



**Star Topology** 

​	In the star network topology, you connect each network node to a central device called a hub. Small LANs with less than eight nodes usually need only one hub. Larger networks can require many hubs, and hubs can be connected to each other to tie all the nodes together into a single network. Figure 10A-2 shows an example of a network using the star topology. The network in this example actually consists of two stars each centered on its own hub. The hubs are tied together to provide a single **cohesive（团结的，使凝聚）** network. 

​	Hubs are usually connected together to expand the number of nodes in the network. Hubs typically allow four, eight, or sixteen nodes before another hub is required. In Figure 10A-2, for example, the upper hub uses seven of its eight connections for attaching nodes, and its eighth to connect to the other hub. This approach of connecting stars together is also sometimes used when setting up a WAN. If two branch offices each have their own star topology LANs, you can connect the two LANs together by connecting the two hubs together via a WAN connection. The concept of connecting hubs isn’t restricted to networks. **Airlines（航空公司）** typically select a **handful（少数）** of major airports as hubs, and create their routes based on traveling through these hubs. You can still get from any city to any other city, but you may have to travel through a hub or two along the way. So it is with the data on a star topology network. Every network node is connected, but data must travel through one or more hubs between its source and destination. One difference between airline hubs and network hubs is the role of the hub itself. Airline hubs, such as the Dallas-Fort Worth International Airport1 , for example, can be the beginning or end of a trip. In contrast, a network hub is always between the source and destination of the data. The data source and destination are always network nodes connected to the hub—never the hub itself. You get what you pay for when selecting a network topology. Star topologies are more expensive to implement than bus topologies. You must invest in at least one hub, even if you want to connect only two computers together. Each addition of four, eight, or sixteen nodes to the network may require an additional hub. In contrast, bus topologies require no additional external hardware, beyond the inexpensive terminators at each end of the bus. 



**Ring Topology** 

​	The ring network topology is shaped just like its name implies—it’s made up of an unbroken circle of network nodes. Essentially, each node is directly connected to its immediate neighbors. Data on the network flows in one direction around the ring, traveling from one node to the next along the way. Figure 10A-3 illustrates the ring topology. Conceptually, a ring is like a bus that has had its two ends brought together. In other words, a ring is like a circular bus, to which all nodes are directly attached. The ring topology can be **plagued（折磨、麻烦）** with reliability problems because it depends on an unbroken link between each **adjacent（临近的）** node on the network. If the ring is broken at any point along the way, the entire network stops functioning. 



**Physical and Logical Topologies**

​	In the topology discussion so far, I’ve focused on the physical layout of the network in terms of cabling and hubs. This is known as the physical topology of the network. But the physical topology doesn’t really tell the whole story. Each network also has a logical topology, which describes how data actually travels on the network. The physical and logical topology of the network can be the same, but often they aren’t. Think of the physical topology as the network layout you’d see if you looked at the physical network from outside. To understand the physical topology, you completely ignore how the data travels, and focus instead on the appearance of cables, hubs, and nodes that make up the network. To understand the logical topology, you need to become one with the data traveling on the network. Pretend you are the data, and follow the path it takes. The path you follow defines the network’s logical topology. Why is this important? Well, **it turns out that（原来是、证明）** most networks today use a physical star topology, but may have the logical topology of a bus, a star, or a ring. The internal wiring of the cables and hubs determines the network’s logical topology. So there are different types of hubs, connectors, and wiring, depending on the logical topology of the network you’re implementing. 

​	For example, a physical star topology may be wired with a logical bus topology. Unless the hub itself fails, a break in a single cable won’t bring down the entire network—just the node attached to the broken cable. A physical star topology can also be used to implement a logical ring topology, as shown in Figure 10A-4. Notice that the data travels in one direction only, creating a logical ring. Hubs come in many different flavors, because they can be wired to implement any of the three basic logical network topologies. For example, a hub that implements a ring topology, such as the one shown in Figure 10A-4, is called a multistation access unit (or MAU2 or MSAU3 ). Moreover, a hub can be either passive or active. A passive hub simply acts as a central wiring point, and does nothing to the signals that pass through it. In contrast, an active hub can provide a wide range of features. In its most basic form, an active hub **amplifies（放大）** transmitted signals, to prevent **distortion（失真）** and lost data. High-end active hubs can offer features that include sophisticated network management, **diagnostics（诊断）**, and reporting capabilities. 



**Choosing Between Network Topologies** 

​	The most prevalent physical network topology today is the star topology, even if it’s used to implement a different logical topology. Here’s why the star has become the standard approach to implementing other logical network topologies:

- Convenience—The star configuration causes all network wiring to **converge（汇聚）** in a central location, typically in a wiring closet or server room. This central location makes it convenient for the network administrator to configure, **troubleshoot（解决重大问题、排除故障）**, and maintain the physical network connections. 
- Flexibility—Because each network node is attached via its own **dedicated（专用、献身）** cable, the star approach makes it very easy to add, move, or remove individual nodes from the network without affecting other nodes. 
- Intelligence—As manufacturers create increasingly smarter hub devices, star topologies can take advantage of the intelligence built into these devices, including centralized network management and advanced troubleshooting capabilities. Even if a network doesn’t use intelligent hubs today, having the physical star topology in place makes it possible to insert intelligent hubs in the future. 



## 07-27:

**What Is TCP/IP?** 

​	TCP/IP refers to two network protocols (or methods of data transport) used on the Internet. They are Transmission Control Protocol and Internet Protocol, **respectively(分别地)**. These network protocols belong to a larger collection of protocols, or a protocol suite. These are collectively referred to as the TCP/IP suite. Protocols within the TCP/IP suite work together to provide data transport on the Internet. In other words, these protocols provide nearly all services available to today’s Net surfer. Some of those services include: 

- Transmission of electronic mail
- File transfers 
- Usenet news delivery 
- Access to the World Wide Web 

There are two classes of protocol within the TCP/IP suite. They are: 

- The network-level protocol 

- The application-level protocol 

​	Network-level protocols manage the **discrete（分离、分别）** mechanics of data transfer. These protocols are typically invisible to the user and operate deep **beneath（在下层）** the surface of the system. For example, the IP protocol provides packet delivery of the information sent between the user and remote machines. It does this based on a variety of information, most **notably（明显的）** the IP address of the two machines. Based on this and other information, IP guarantees that the information will be routed to its intended destination. Throughout this process, IP interacts with other network-level protocols engaged in data transport. Short of 1 using network utilities (perhaps a sniffer or other device that reads IP datagrams), the user will never see IP’s work on the system. Conversely, application-level protocols are visible to the user in some measure. For example, File Transfer Protocol (FTP) is visible to the user. The user requests a connection to another machine to transfer a file, the connection is established, and the transfer begins. During the transfer, a portion of the exchange between the user’s machine and the remote machine is visible (**primarily（主要的）** error messages and status reports on the transfer itself, for example, how many bytes of the file have been transferred at any given moment). For the moment, this explanation will suffice: TCP/IP refers to a collection of protocols that facilitate communication between machines over the Internet (or other networks running TCP/IP). 



**The History of TCP/IP** 

​	In 1969, the Defense Advanced Research Projects Agency (DARPA) **commissioned（受委托）** development of a network over which its research centers might communicate. Its **chief concern** was this network’s capability to **withstand（承受住）** a nuclear attack. In short, if the Soviet Union launched a nuclear attack, it was **imperative（必要得）** that the network remain intact to facilitate communication. The design of this network had several other requisites, the most important of which was this: It had to operate independently of any centralized control. Thus, if one machine was destroyed (or 10, or 100), the network would remain impervious. The prototype for this system emerged quickly, based in part on research done in 1962 and 1963. That prototype was called ARPANET. ARPANET reportedly worked well, but was subject to **periodic（阶段性得）** system crashes. Furthermore, long-term expansion of that network proved costly. A search was initiated for a more reliable set of protocols; that search ended in the mid-1970s with the development of TCP/IP. TCP/IP had significant advantages over other protocols. For example, TCP/IP was lightweight (it required **meager（贫乏、微博）** network resources). Moreover, TCP/IP could be implemented at much lower cost than the other choices then available. Because of these advantages, TCP/IP became exceedingly popular. In 1983, TCP/IP was integrated into release 4.2 of Berkeley Software Distribution (BSD) UNIX. Its integration into commercial forms of UNIX soon followed, and TCP/IP was established as the Internet standard. It has remained so (as of this writing). As more users **flock to（聚集）** the Internet, however, TCP/IP is being reexamined. More users translate to greater network load. To **ease（减轻）** that network load and offer greater speeds of data transport, some researchers have suggested implementing TCP/IP via satellite transmission. Unfortunately, such research has thus far produced **dismal（忧郁）** results. TCP/IP is apparently unsuitable for this implementation. Today, TCP/IP is used for many purposes, not just the Internet. For example, intranets are often built using TCP/IP. In such environments, TCP/IP can offer significant advantages over other networking protocols. One such advantage is that TCP/IP works on a wide variety of hardware and operating systems. Thus, one can quickly and easily create a heterogeneous network using TCP/IP. Such a network might have Macs, IBM compatibles, and so on. Each of these can communicate with its peers using a common protocol suite. For this reason, since it was first introduced in the 1970s, TCP/IP has remained extremely popular. 



**What Platforms Support TCP/IP?**

​	 Most platforms support TCP/IP. However, the quality of that support can vary. Today, most mainstream operating systems have native TCP/IP support (that is, TCP/IP support that is built into the standard operating system distribution). However, older operating systems on some platforms lack such native support. Table 10B-1 describes TCP/IP support for various platforms. If a platform has native TCP/IP support, it is labeled as such. If not, the name of a TCP/IP application is provided. Platforms that do not natively support TCP/IP can still implement it through the use of proprietary or third-party TCP/IP programs. In these instances, third-party products can offer varied functionality. Some offer very good support and others offer **marginal（微不足道）** support. For example, some third-party products provide the user with only basic TCP/IP. For most users, this is sufficient. (They simply want to connect to the Net, get their mail, and enjoy easy networking.) In contrast, certain third-party TCP/IP implementations are comprehensive. These may allow manipulation of compression, methods of transport, and other features common to the typical UNIX TCP/IP implementation. Widespread third-party support for TCP/IP has been around for only a few years. Several years ago, for example, TCP/IP support for DOS boxes was very slim. One interesting point about non-native, third-party TCP/IP implementations is this: Most of them do not provide servers within their distributions. Thus, although a user can connect to remote machines to transfer a file, the user’s machine cannot accept such a request. For example, a Windows 3.11 user using TCPMAN cannot—without installing additional software—accept a file-transfer request from a remote machine. 



**How Does TCP/IP Work?** 

​	TCP/IP operates through the use of a protocol stack. This stack is the sum total of all protocols necessary to complete a single transfer of data between two machines. (It is also the path that data takes to get out of one machine and into another.) The stack is broken into layers, five of which are of concern here. To grasp this layer concept, examine Figure 10B-1. After data has passed through the process illustrated in Figure 10B-1, it travels to its destination on another machine or network. There, the process is executed in reverse (the data first meets the physical layer and **subsequently（随后）** travels its way up the stack). Throughout this process, a complex system of error checking is employed both on the originating and destination machine. 

​	Each layer of the stack can send data to and receive data from its **adjoining（邻接）** layer. Each layer is also associated with multiple protocols. At each tier of the stack, these protocols are hard at work, providing the user with various services. 



**TCP/IP Is the Internet** 

​	TCP/IP basically comprises the Internet itself. It is a complex collection of protocols, many of which remain invisible to the user. On most Internet servers, a minimum of these protocols exist: 

- Transmission Control Protocol
- Internet Protocol
- Internet Control Message Protocol 
- Address Resolution Protocol 
- File Transfer Protocol 
- The Telnet1 protocol 
- The Gopher2 protocol 
- Network News Transfer Protocol 
- Simple Mail Transfer Protocol
-  Hypertext Transfer Protocol 

​	These are only a handful of the protocols run on the Internet. There are actually hundreds of them. Better than half of the primary protocols have had one or more security holes. In essence, the Internet was designed as a system with multiple avenues of communication. Each protocol is one such avenue. As such, there are hundreds of ways to move data across the Net. Until recently, utilizing these protocols called for accessing them one at a time. That is, to arrest a Gopher session and start a Telnet session, the user had to physically terminate the Gopher connection. The HTTP browser changed all that and granted the average user much greater power and functionality. Indeed, FTP, Telnet, NNTP3 , and HTTP are all available at the click of a button.