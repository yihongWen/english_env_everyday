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



## 07-28:

**Network-Level Protocols** 

​	Network protocols are those protocols that **engage(参加)** in (or facilitate) the transport process transparently. These are invisible to the user unless that user employs utilities to monitor system processes. Important network-level protocols include:

- The Address Resolution Protocol (ARP) 
- The Internet Control Message Protocol (ICMP) 
- The Internet Protocol (IP) 
- The Transmission Control Protocol (TCP) 



**The Address Resolution Protocol**

​	 The Address Resolution Protocol (ARP) serves the **critical（关键的）** purpose of mapping Internet addresses into physical addresses. This is vital in routing information across the Internet. Before a message (or other data) is sent, it is packaged into IP packets, or blocks of information suitably formatted for Internet transport. These contain the numeric Internet (IP) address of both the originating and destination machines. Before this package can leave the originating computer, however, the hardware address of the recipient (destination) must be discovered. (Hardware addresses differ from Internet addresses.) This is where ARP makes its **debut（首次出现）**. 

​	An ARP request message is broadcast on the subnet. This request is received by a router that replies with the requested hardware address. This reply is caught by the originating machine and the transfer process can begin. ARP’s design includes a cache. To understand the ARP cache concept, consider this: Most modern HTML browsers (such as Netscape Navigator or Microsoft’s Internet Explorer) utilize a cache. This cache is a portion of the disk (or memory) in which elements from often-visited Web pages are stored (such as buttons, headers, and common graphics). This is logical because when you return to those pages, these **tidbits（常用信息、花边新闻）** don’t have to be reloaded from the remote machine. They will load much more quickly if they are in your local cache. Similarly, ARP implementations include a cache. In this manner, hardware addresses of remote machines or networks are remembered, and this memory **obviates the need（不在需要）** to conduct subsequent ARP queries on them. This saves time and network resources. Can you guess what type of security risks might be involved in maintaining such an ARP cache? Address caching (not only in ARP but in all instances) poses a unique security risk. If such address-location entries are stored, it makes it easier for a cracker to **forge（伪造）** a connection from a remote machine, claiming to **hail（招呼、致意）** from one of the cached addresses. 



**The Internet Control Message Protocol** 

​	The Internet Control Message Protocol handles error and control messages that are passed between two (or more) computers or hosts during the transfer process. It allows those hosts to share that information. In this respect, ICMP is critical for diagnosis of network problems. Examples of diagnostic information gathered through ICMP include: 

- When a host is down
- When a gateway is congested or inoperable
- Other failures on a network 



**The Internet Protocol** 

​	IP belongs to the network layer. The Internet Protocol provides packet delivery for all protocols within the TCP/IP suite. Thus, IP is the heart of the incredible process by which data traverses the Internet. To explore this process, I have drafted a small model of an IP datagram (see Figure 10C-1). 

​	As illustrated, an IP datagram is composed of several parts. The first part, the header, is composed of **miscellaneous(混杂的)** information, including originating and destination IP address. Together, these elements form a complete header. The remaining portion of a datagram contains whatever data is then being sent. The amazing thing about IP is this: If IP datagrams encounter networks that require smaller packages, the datagrams bust apart to accommodate the recipient network. Thus, these datagrams can fragment during a journey and later be reassembled properly (even if they do not arrive in the same sequence in which they were sent) at their destination. Even further information is contained within an IP datagram. Some of that information may include identification of the protocol being used, a header checksum, and a time-to-live specification. This specification is a numeric value. While the datagram is traveling the void, this numeric value is constantly being decremented. When that value finally reaches a zero state, the datagram dies. Many types of packets have time-to-live limitations. Some network utilities (such as Traceroute) utilize the time-to-live field as a marker in diagnostic routines. In closing, IP’s function can be reduced to this: providing packet delivery over the Internet. As you can see, that packet delivery is complex in its implementation. 



**The Transmission Control Protocol** 

​	The Transmission Control Protocol is the chief protocol employed on the Internet. It facilitates such mission-critical tasks as file transfers and remote sessions. TCP accomplishes these tasks through a method called reliable data transfer. In this respect, TCP differs from other protocols within the suite. In unreliable delivery, you have no guarantee that the data will arrive in a perfect state. In contrast, TCP provides what is sometimes referred to as reliable stream delivery. This reliable stream delivery ensures that the data arrives in the same sequence and state in which it was sent. The TCP system **relies on** a virtual circuit that is established between the requesting machine and its target. This circuit is opened via a three-part process, often referred to as the three-part handshake. The process typically follows the pattern illustrated in Figure 10C-2. 

​	After the circuit is open, data can simultaneously travel in both directions. This results in what is sometimes called a f**ull-duplex（全双工的）** transmission path. Full-duplex transmission allows data to travel to both machines at the same time. In this way, while a file transfer (or other remote session) is underway, any errors that arise can be forwarded to the requesting machine. TCP also provides extensive error-checking capabilities. For each block of data sent, a numeric value is generated. The two machines identify each transferred block using this numeric value. For each block successfully transferred, the receiving host sends a message to the sender that the transfer was clean. Conversely, if the transfer is unsuccessful, two things may occur: 

-  The requesting machine receives error information 
- The requesting machine receives nothing When an error is received, the data is retransmitted unless the error is fatal, in which case the transmission is usually halted. 

Similarly, if no confirmation is received within a specified time period, the information is also retransmitted. This process is repeated as many times as necessary to complete the transfer or remote session. 





## 07-29:

**How Does the Internet Work?** 

​	The Internet is based on the concept of a client-server relationship between computers, also called a client/server architecture. In a client/server architecture, some computers act as servers, or information providers, while other computers act as clients, or information receivers. The client/server architecture is not one-to-one—that is, a single client computer may access many different servers, and a single server may be accessed by a number of different client computers. Prior to the mid-1990s, servers were usually very powerful computers such as mainframes or supercomputers, with extremely high processing speeds and large amounts of memory. Personal computers and workstations, **however, are now capable of acting as Internet servers due to advances in computing technology.** A client computer is any computer that receives information from a server and is often a personal computer.

​	To access information on the Internet, a user must first log on, or connect, to the client computer’s host network. A host network is a network that the client computer is part of, and is usually a local area network (LAN). Once a connection has been established, the user may request information from a remote server. If the information requested by the user resides on one of the computers on the host network, that information is quickly retrieved and sent to the user’s terminal. If the information requested by the user is on a server that does not belong to the host LAN, then the host network connects to other networks until it makes a connection with the network containing the requested server. In the process of connecting to other networks, the host may need to access a router, a device that determines the best connection path between networks and helps networks to make connections. 

​	Once the client computer makes a connection with the server containing the requested information, the server sends the information to the client in the form of a file. A special computer program called a browser enables the user to view the file. Examples of Internet browsers are Mosaic , Netscape, and Internet Explorer. Most Internet files are multimedia documents—that is, text, graphics, photographs, audio, and video may be combined in a single document. Non-multimedia documents do not need browsers to view their text-only contents and many multimedia documents provide access to text-only versions of their files. The process of retrieving files from a remote server to the user’s terminal is called downloading. One of the strengths of the Internet is that it is structured around the concept of hypertext. The term hypertext is used to describe an interlinked system of documents in which a user may jump from one document to another in a **nonlinear(非线形的)**, associative way. The ability to jump from one document to the next is made possible through the use of hyperlinks—portions of the hypertext document that are linked to other related documents on the Internet. By clicking on the hyperlink, the user is immediately connected to the document specified by the link. Multimedia files on the Internet are called hypermedia documents. 



**Accessing the Internet** 

​	Access to the Internet falls into two broad categories: **dedicated（专用）** access and dial-up access. With dedicated access, the computer is directly connected to the Internet via a router, or the computer is part of a network linked to the Internet. With dial-up access, a computer connects to the Internet with a temporary connection, generally over a telephone line using a modem—a device that converts the electrical signals from a computer into signals that can be transmitted over traditional telephone lines. A modem is needed because computers are digital, meaning that their signals are made up of **discrete（离散）** units, while most telephone lines are analog, meaning that they carry signals that are continuous instead of discrete. Once a signal has traveled over the telephone line, a second modem is required at the other end of the line to reconvert the transmitted signals from analog to digital. A great many companies, called Internet Service Providers (ISPs), provide dial-up access to the Internet for a modest fee. Examples of ISPs are America Online (AOL ), the Microsoft Network (MSN , and CompuServe .



**Packaging Information** 

​	All data transmitted over the Internet is divided up into small units of information called packets, each of which is labeled with a unique number indicating its place in the data stream—the flow of information between computing devices. When the various packets that make up a set of data arrive at their destination, they are re-assembled using the unique labels given them. If part of the network over which the packets are sent is **malfunctioning（出故障）**, or down, special automatic features of the Internet’s routing equipment re-route the packets so that they travel over functioning portions of the network. Other features make sure that all the data packets arrive intact, automatically requesting that missing or incomplete packets be re-sent from the source. This system, called packet-switching, uses a series of protocols, or rules, known as TCP/IP (Transmission Control Protocol/Internet Protocol).



**Network Addressing** 

​	To be part of the Internet a computer must have a unique Internet Protocol (IP) network address so that messages can be correctly routed to and from the machine over the Internet. Internet addresses are called URLs (Uniform Resource Locators). Some URLs are a string of numbers, but because long strings of numbers are difficult for people to remember, other addressing conventions are also used. An example of this convention is: http://encarta.msn.com/downloads/pryearbk.asp. The http indicates the protocol—in this instance the hypertext transfer protocol—used to access the particular location on the Internet. The name after the **colon（冒号）** and double slash (encarta.msn.com) indicates the hostname, which is the name of a specific computer system connected to the Internet. The remaining names after the hostname indicate various files to which the specific URL points. In the example URL, the file pryearbk is located within the directory downloads. Other files located in the same directory will have a similar URL, the only difference being the name of the file, or files, at the end of the address . Special name servers map IP numbers to domain names (msn.com in the above URL) and guarantee that the correct IP number of the source and the destination are provided for all packets.



**E-Mail** 

​	The most widely used tool on the Internet is electronic mail, or e-mail (see Figure 11A-1). E-mail is used to send written messages between individuals or groups of individuals, often geographically separated by large distances. E-mail messages are generally sent from and received by mail servers—computers that are dedicated to processing and directing e-mail. Once a server has received a message it directs it to the specific computer that the e-mail is addressed to. To send e-mail, the process is reversed. A very convenient and inexpensive way to transmit messages, e-mail has dramatically affected scientific, personal, and business communications. E-mail is the basis of much organized exchange between groups of individuals. List servers, for example, make it possible to address a list of subscribers either in one-way communication, as in keeping interested people up-to-date on a product, or two-way communication, as in online discussion groups.  Another use of e-mail is **Usenet（新闻组）**, in which discussions on a particular subject are grouped together into newsgroups. There are thousands of newsgroups covering an extremely wide range of subjects. Messages to a newsgroup are not posted directly to the user, but are accessible in the form of an ordered list on a dedicated local news server. The networking of these servers makes such discussions available worldwide. Associated software not only enables users to choose which messages they want to read, but also to reply to them by posting messages to the newsgroup.

 

**Transmission Schemes** 

​	Before the introduction of the World Wide Web, various standards and types of software existed for transmitting data over the Internet. Many of these are still in use, with Telnet, File Transfer Protocol (FTP), and Gopher among the most popular. Telnet allows an Internet user to connect to a distant computer and use that computer as if he or she were using it directly. FTP is a method of moving files from one computer to another over the Internet, even if each computer has a different operating system or storage format. Gopher is an improvement on FTP, making it easier to list and retrieve files remotely. While these transmission protocols and software are still in use, the WWW is much easier to use and is used much more often than earlier transmission protocols. 



**Bandwidth** 

​	The amount of data that a computer network can transmit is called the bandwidth of the network and is usually measured in kilobits per second (Kbps) or megabits per second (Mbps). A bit—the smallest unit of information that computers can process—can have one of two values, either 0 or 1. A kilobit is one thousand bits, while a megabit is one million bits. The transportation of information between routers generally uses communication lines dedicated to this function, with capacities currently ranging from 64 Kbps up to as much as several hundred Mbps. The speed at which information can be transmitted across the Internet depends on the lowest information transporting capacity along the route and the number of people using that route at any given time. A narrow bandwidth somewhere along the route acts as a **bottleneck（瓶颈）** to data transport, and the more people using the line, the less information each of them can transport at any one time. 

## 

## 07-30:

**What’s E-Mail?** 

​	In computer science, e-mail is the **abbreviation（缩写词）** of the term electronic mail, method of transmitting data or text files from one computer to another over an internet, intranet, or the Internet. E-mail enables computer users to send messages and data quickly through a local area network or beyond through a nationwide or worldwide communication network. E-mail came into widespread use in the 1990s and has become a major development in business and personal communications.

​	E-mail users create and send messages from individual computers using commercial e-mail programs or mail-user agents (MUAs). Most of these programs have a text editor for composing messages. The user sends a message to one or more recipients by specifying destination addresses. When a user sends an e-mail message to several recipients at once, it is sometimes called broadcasting.

​	The address of an e-mail message includes the source and destination of the message. Different addressing conventions are used depending upon the e-mail destination. An interoffice message distributed over an intranet, or internal computer network, may have a simple scheme, such as the employee’s name, for the e-mail address. E-mail messages sent outside of an intranet are addressed according to the following convention: the first part of the address contains the user’s name, followed by the symbol @, the domain name, the institution’s or organization’s name, and finally the country name. 

​	A typical e-mail address might be sally@abc.com. In this example sally is the user’s name, abc is the domain name—the specific company, organization, or institution that the e-mail message is sent to or from, and the suffix com indicates the type of organization that abc belongs to—com for commercial, org for organization, edu for educational, mil for military, and gov for governmental. An e-mail message that originates outside the United States or is sent from the United States to other countries has a **supplementary（补充、附加）** suffix that indicates the country of origin or destination. Examples include uk for the United Kingdom, fr for France, and au for Australia.

​	E-mail data travels from the sender’s computer to a network tool called a message transfer agent (MTA1 ) that, depending on the address, either delivers the message within that network of computers or sends it to another MTA for distribution over the Internet. The data file is eventually delivered to the private mailbox of the recipient, who retrieves and reads it using an e-mail program or MUA. The recipient may delete the message, store it, reply to it, or forward it to others. Modems are important devices that have allowed for the use of e-mail beyond local area networks. 

​	Modems convert a computer’s binary language into an analog signal and transmit the signal over ordinary telephone lines. Modems may be used to send e-mail messages to any destination in the world that has modems and computers able to receive messages. 

​	E-mail messages display technical information called headers and footers above and below the main message body. In part, headers and footers record the sender’s and recipient’s names and e-mail addresses, the times and dates of message transmission and receipt, and the subject of the message. In addition to the plain text contained in the body of regular e-mail messages, an increasing number of e-mail programs allow the user to send separate files attached to e-mail transmissions. This allows the user to append large text- or graphics-based files to e-mail messages.

​	E-mail has had a great impact on the amount of information sent worldwide. It has become an important method of transmitting information previously **relayed（转发、传播）** via regular mail, telephone, **courier（快递）**, fax, television, and radio. 



**Videoconferencing（视频会议）** 

​	Thanks to the constantly evolving world of Internet communication, anybody with a reasonably sophisticated computer system can now experience videoconferencing—speaking, seeing, and sometimes writing to another person simultaneously. 

​	As with other Internet communication software, the problems you may experience with videoconferencing involve the type of equipment you are using and the speed of your Internet connection. If you want to experience all the features of a product like CU-SeeMe1 , you must have speakers, a microphone, and a video camera. Fortunately, there are several palm-sized video cameras available through most any computer store, catalog, or Web site for under $100. You must also ensure that you have the correct drivers and any other related software configured properly on your computer in order for these **peripherals（外围设备）** to work. 

​	Additionally, remember that videoconferencing will work best if both parties are on the same kind and speed of Internet connection. Some of the demos, shareware, and freeware listed in this section will not work at all if you have less than a 28.8K2 -capable modem, so if you plan to use videoconferencing on a regular basis, you should at the least have a 56K modem for adequate video performance. 

​	The first time you use videoconferencing, you may be surprised to realize how many people can see you if you simply jump into an existing conference. A typical videoconference is like a chat room, only the image of each person in the conversation is displayed in their window on your monitor. It is always a good idea to participate in a few of these general conferences to get an idea of how you will look and sound, and to see how other people behave. 

​	Good videoconferencing **netiquette（网络礼节）**—particularly for business and other related nonpersonal conferencing—involves much more than the general good netiquette you’re expected to use with other kinds of Internet communication. Today’s average computer users are accustomed to knowing that no one else can see them or their office space when they are sending e-mail or participating in a text-only chat session. However, with videoconferencing, both you and much of the room or space around you will be visible to your video camera as well. If you want or need to seem professional to the person you’re calling, you may not want to videoconference in your old college sweatshirt without brushing your hair. Also, look around at your walls, your desk, and anyplace else around your computer that may be photographed by your video camera. Keep this area tidy and clutter-free, and consider moving any questionable decorations such as that Playboy calendar.



**REALISTIC EXPECTATIONS(切实的希望)** 

​	People have waited a long time for videoconferencing to emerge—it was, in fact, one of the primary plans for TV when it was first developed, and before the concept of broadcast TV took over. The phone companies have spent millions on fascinating studies of videoconferencing, resulting in some demonstration projects and some marketed products, but no videoconferencing system has ever **taken off（开始、流行）**  like Internet videoconferencing. The images aren’t necessarily better and the convenience factors haven’t improved much over the best system available previously, but the costs now are **substantially（大量的）** better:

- Transmission costs beyond the basic Internet connection are **negligible（微不足道）** now (**versus（与...相比）** high, **metered（按计量）**, long-distance costs before). 
- Video cameras suitable for videoconferencing have dropped in price from thousands of dollars to barely over $100. 
- The computer, purchased and used for other purposes, easily takes the place of hundreds of dollars of dedicated electronics that formerly would have had to be purchased. 

Keep these advantages in mind when experimenting with current videoconferencing systems. They are interesting, and they work, but you will have to decide if they can adequately handle your personal or business needs. 



**Motion** 

​	Normal TV images are made up of two interlaced images, each of which is displayed for approximately 1 ⁄60 of a second. The full motion picture is therefore made up of 30 full frames per second. In online videoconferencing, images are rarely refreshed more than 20 times per second; in fact, it is not unusual for images to be updated only once or twice per second. Videoconferencing is therefore often at least a bit **jerky（不稳定）** in **depicting（描绘）** motion, and sometimes more **akin（相似）** to a slide show than a movie. As usual, the faster the connection the more frequent the refreshes. 



**Resolution（分辨率）** 

​	Depending on the resolution setting of your computer monitor, your videoconferencing images will be about 2″ by 3″. While most systems let you resize the image, this doesn’t necessarily mean that you will be getting more image information; you will be seeing the same image enlarged. You may at times want to enlarge the image so that you can view it from a greater distance, but do understand that at the same viewing distance the larger image will just look **coarser（粗糙的）**.



**Uses**

​	Online videoconferencing has been used primarily for social interaction. Businesses could benefit from videoconferencing, as long as expectations are realistic. The low resolution and image update frequencies will not allow people’s responses or expressions to be as visible as in a normal TV conference, and **definitely（当然）** not as good as in person. Still, in some cases where these other contacts are out of the question, the videoconference may provide some feel for the other person, and some increased sense of communication. For some purposes, you can use the videoconferencing systems to display things such as appearances of rooms, machines, landscapes, and movements of large and small living things. For many purposes, however, you may need the extra resolution of scanned images or digital still cameras. Consider the possibilities for a video system that enables you to distribute images for almost no cost after the initial outlay. Monitoring systems, teaching, and scientific research are among thousands of possibilities. 

**HARDWARE CONSIDERATIONS** 

​	Cameras suitable for black-and-white videoconferencing are sometimes available for prices as low as $50, and color cameras are as low as $100. These cameras usually connect directly to your computer’s input/output ports. Because videoconferencing exchanges images of limited speed and resolution, there is little need to purchase a higher-quality camera. If you currently have a video camera or **camcorder（摄像机）** you might want to purchase a video capture card to provide your videoconferencing images. The video capture card can better make use of a high quality camera for other uses such as grabbing video images for Web page use. To have two-way conversations (like a telephone) instead of those that only allow one speaker at a time (like a CB radio), you will need a full duplex sound card. These are available in a variety of quality levels and are often not much more expensive than the simplex boards. 



**VIDEOCONFERENCING SYSTEMS** 

​	The following is information about several videoconferencing systems. CU-SeeMe CU-SeeMe is a free videoconferencing system that is available for Windows 3.1, 95, and NT; Amiga; Mac OS; OS/2; and Linux operating systems. This large operating-system base and the fact that the system is free, easy to use, and has been available longer than most other videoconferencing systems would be enough to make it an exceptionally popular system.

​	 There is, however, another feature that adds to its popularity—the use of reflectors. Reflectors enable groups of people to videoconference together. Reflectors work by receiving the video packets from each video camera in the videoconference, and then sending the combined video signals out to all who are viewing the conference. CU-SeeMe can also be used for one-to-one videoconferencing without the use of a reflector site; signals are sent by direct connection (DC) between the two sites. (Private chat requires downloading separate plug-in software.) Most CU-SeeMe videoconferencing is done in **monochrome（黑白照片）**, but an enhanced version is available that supports color conferencing. You can get a feel for videoconferencing by downloading the software and visiting reflector sites as a lurker—a conference viewer without a camera. Some reflector sites discourage lurking because it slows down the reflector, but others accept or encourage lurking. Keep watch for indications at the reflector site of their guidelines on this and other netiquette matters.



iVisit

​	 www.ivisit.com/index.html Another excellent option for one-to-one or small group videoconferencing is iVisit’s software. It is available for free download for Macintosh, Windows 95, and Windows NT platforms. Instead of using reflectors as CU-SeeMe does for groups, iVisit establishes direct connections between each member of the videoconference. This enables private conferences free of concerns about reflector guidelines and over usage. These direct connections, however, do tax the capacity of your own modem and ISP connection, and the image quality as groups get larger. In addition to the monochrome and color video, iVisit supports simultaneous audio and text chats. 



Microsoft’s NetMeeting

​	 http://microsoft.com/netmeeting/ NetMeeting 2.1’s videoconferencing tools are designed to work with any camera or capture card that supports Video for Windows2 to transmit video images. (Viewing videoconferences doesn’t require extra hardware or software beyond NetMeeting itself.) The video component of NetMeeting provides real-time video images when using a 28.8 Kbps or faster modem. These images can be resized and the image quality can be adjusted for the preferred balance between video quality and system performance. 

RESOURCES

​	Because videoconferencing systems use various compression and transmitting standards, most systems are not interoperable with each other. For extra tools, information, and other resources it is usually best to look for sites provided by the software manufacturer or sites that specialize in the videoconferencing system you are interested in. 

CU-SeeMe cool site

​	 www.rocketcharged.com/cu-seeme/ This informal site is an excellent resource for those new to videoconferencing, and specifically to those interested in using the free CU-SeeMe system. The site contains links to software, files of frequently asked questions, and lists of reflectors (used for multiple-user videoconferences). 

CU-SeeMe home page

 http://cu-seeme.cornell.edu/ From the source of the CU-SeeMe project at Cornell University3 , where CU-SeeMe originated in 1993, you can get information on hardware requirements and software downloads. 

Bill Woodland’s CU-SeeMe page

​	 http://cu-seeme.cornell.edu/~WCW Bill Woodland provides not only an excellent general resource for CU-SeeMe background information, but also access to one of the best reflector site lists





## 07-31:

**Information Revolution**

**Introduction** 

​	Information Revolution refers to the fundamental changes in the production and use of information, occurring in the late 20th century. Human societies throughout history have had “information specialists” (from traditional healers to newspaper editors); and they have had “information technologies” (from cave painting to **accountancy(会计)**); but two interrelated developments, social and technological, **underpin（支持、证实）** the diagnosis that an information revolution is now occurring. 



**Social and Technological Developments** 

​	First, there are social and organizational changes. Information-processing has become increasingly visible and important in economic, social, and political life. One familiar piece of evidence is the statistical growth of occupations specializing in information activities. Numerous studies have demonstrated substantial growth in information-based occupations. These occupations now take the largest **share（份额）** of employment in the United States, the United Kingdom, and many other industrial societies. The biggest category is information processors—mainly office workers—followed by information producers, distributors, and infrastructure workers.

​	Second, there is technological change. The new information technology (IT) based on microelectronics, together with other innovations such as **optical discs（光盘）** and fibre optics, underpins huge increases in the power, and decreases in the costs, of all sorts of information-processing. (The term “information-processing” covers the generation, storage, transmission, manipulation, and display of information, including numerical, textual, audio, and video data.) The information-processing aspects of all work can be reshaped through IT, so the revolution is not limited to information occupations: for example, industrial robots change the nature of factory work.

​	 Computing and telecommunications (and also such areas as broadcasting and publishing) used to be quite distinct industries, involving distinct technologies. Now they have converged around certain key activities, such as use of the Internet. Using the same underlying technologies, modern computing and telecommunication devices handle data in digital form. Such data can be shared between, and processed by, many different devices and media, and used in a vast range of information-processing activities.

​	 The pace of adoption of new IT has been very speedy: it is **markedly（显著的）** more rapid than that of earlier revolutionary technologies, such as the steam engine or electric motor. Within 25 years of the invention of the microprocessor, it had become commonplace in practically every workplace and many homes: present not only in computers, but also in a huge variety of other devices, from telephones and television sets to washing machines and children’s toys. 



**The Direction of the Information Revolution** 

​	The outcome of the information revolution is seen by some commentators as likely to be as profound as the shift from agricultural to industrial society. Others see the transformation as essentially a change from one form of industrial society to another, as has happened in earlier technological revolutions. 

​	One major issue is how rapidly social institutions adapt to take advantage of the new ways of doing things that new IT makes possible. While some jobs and some areas of people’s lives do seem to have changed rapidly, many others appear to have been affected relatively little. Historians point out that it can take a very long time for what in retrospect seems the obvious way to use a technology to become standard practice. For example, electric motors were first used as if they were steam engines, with one centralized motor powering numerous devices, rather than numerous small motors, each powering its own appliance. 

​	New IT has often been introduced into well-established patterns of working and living without radically altering them. For example, the traditional office, with secretaries working at keyboards and notes being written on paper and manually exchanged, has remained remarkably stable, even if personal computers have replaced typewriters. Often the technology that gains acceptance is that which most easily fits within traditional ways of doing things. For example, the fax machine, which could take hand-written or typed notes, and was often delegated to a secretary to use, was hugely successful in the 1980s. At the beginning of that decade, it had been predicted that fax would rapidly die out, and e-mail would take its place; but this proved to involve too much organizational change. 



**Trends in Employment** 

​	The tendency to fit a new technology into established structures, rather than to start afresh every time, has often been documented. It is one reason for the absence of the huge office job losses that were being predicted in the late 1970s and early 1980s, when word processing first began to be taken up on a large scale. However, this is no reason to assume that existing structures will endure. Industrial interest in new forms of organization, such as novel management structures, coordination of activities over large distances by means of telecommunications, teleworking, and other forms of distance working, indicates willingness to consider change. 

​	The “**hollow（空洞）** firm” is one effort to gain flexibility. The company attempts to **dispense（分发）** with the direct ownership and operation of many facilities that would traditionally have belonged to it, instead **outsourcing（外包）** production, distribution, and other tasks to other firms. Many computer companies, for example, buy in many or most of their components from specialist suppliers, and some firms do little more than design the computer for others to assemble. 

​	A related idea is “**delayering（去层次化）**”, or “**flattening（扁平化）**”, in which the company tries to do away with the numerous layers of middle management and administration that have traditionally processed information, and communication flows between the senior staff and the **shop floor（工作场所、工人）** or fieldworkers. New information systems are typically used to allow rapid communication across a reduced number of organizational layers. 

​	By the late 1990s the integration of office IT is becoming apparent: material is increasingly exchanged by e-mail (which has finally established itself); many professionals use personal computers directly, often at home and while traveling, as well as in the office; and increasingly, personal computers are networked. Whether a loss of **clerical（文书）** jobs will result remains much debated. Some commentators point to job losses in office-based sectors such as financial services, which use IT intensively, as a **harbinger（先驱）** of things to come. Others argue that the unemployment problems of industrial societies are related more to political and economic changes than to the use of new technology. Indeed, new information-related services are emerging, creating new jobs. While some office jobs may have gone, some other traditional clerical jobs have been upgraded to involve new functions made possible with new IT, such as desktop publishing, database management, and customer services. A similar debate has concerned the quality of working life—whether skills have been enhanced or reduced, and whether working conditions have been improved or **degraded（退化）**, in the information revolution. Evidence to date indicates a mixed picture. There are certainly some areas in which conditions have **worsened（恶化）** and skills have been lost, and many low-skill jobs have been created—for example, in cooking and serving fast food. Yet there is also a tendency for more jobs to be upgraded, and new technical skills and skill combinations are in demand. Large-scale **deskilling（降低技术性）** has not taken place. **Polarization（两极分化）** of the workforce in terms of quality of work and levels of wages has ensued; at the same time a **gulf（海湾、鸿沟）** has been opening between employed and unemployed people. Whether this is a result of the information revolution, or of more or less **coincidental（巧合）** economic and political factors, the threat is evident of a widening social gulf between the “information-rich” and the “information-poor”.  The former have information-processing skills, access to advanced technologies in their work, and the money to invest in IT at home for themselves and their children; the latter do not. 



**Information Technology and the Consumer**

​	 At different rates IT is **diffusing（扩散）** into the home. The implications of consumer innovations can be substantial. Widespread use of cars facilitated new ways of life, with a growth of **suburban（郊区）** living and out-of-town shopping centres, and a decline of train and bus services. The expansion of consumer IT is associated with changes in ways of working (for example, telework), playing (new home entertainment systems), shopping (teleshopping), and learning (multimedia products of various sorts). IT can be used in monitoring body conditions (digital thermometers, pulse meters, and blood-pressure meters are available), and in providing health and lifestyle monitoring and advice (recommending exercise levels, medical check-ups, or diets). Telephone helplines have long offered advice, counselling, and medical services; these and many other services are beginning, sometimes in **rudimentary（基本的）** form, to be provided on the Internet. 



**Problems of the Information Revolution** 

​	Public transport was challenged by the shift to cars, and familiar aspects of such public services as education and health could be challenged in the information revolution. Wider concerns over changing relations between private and public activities are reflected in debates about potential or already emerging problems, such as: 

- Threats to privacy (unauthorized access to personal data, increasing **surveillance（监视）** of public spaces by security cameras, etc.)
- The **alleged（声称）** growth of “privatism” (a decline in shared activities as individuals pursue their own interests in isolation)
- The scope for participation. (How far can people have a say in the use of IT in ways that affect them? Do new media support the emergence of new social movements, and of new forms of interest groups, **lobbying（游说）**, and **mobilization（动员）**?) 
- Questions about the ownership of knowledge. (Who has the right to charge for what kinds of information? Should large parts of the media be controlled by a few large companies? What is the scope for freedom of information to be practised by governments?)



​	All this is in addition to the problems of information inequalities mentioned earlier. The information revolution fundamentally involves a change in the role of information-processing in our society. It is not surprising that fundamental questions are being raised about access to, and the use of, intimate and valuable sorts of information. The outcome of the information revolution depends on social action and social choices as well as on technological developments. Just as industrial societies around the world take various forms, and there are very different ways of life within them, so it is likely that there will be a wide range of information societies. However, as new IT permits more global communication, and more firms expand into global markets, there are also strong forces at work to share elements of different cultures around the world on an unprecedented scale. 

