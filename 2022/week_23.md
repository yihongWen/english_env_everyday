## 05-30:

http://coding-geek.com/the-best-programming-language/

**the best programming language**

​	When I want to take a break at work, I sometimes read technology **forums(论坛)**. And there is one kind of posts that I really like: the flame wars between programming languages. I like these posts because you can see passionate and smart people who are arguing as if their lives were at play.

​	These posts have 2 advantages:

	- they make me laugh
	- I learn new stuff



​	If I had to sum up this kind of posts, it would be something like:

​	Post Title “Java is the best language” by NewJavaFanBoy 

- NewJavaFanBoy: Java is the best language because of its community. Moreover, it has really cool features like lambdas. Why so many people hate Java?

- FormerJavaFanBoy: Oracle killed Java.

- DotNetFanBoy: The evolution of Java is too slow, C# had lambdas a while ago. Moreover, some critical features like optional and named parameters are not in Java. Now that dotnet is more open sourced and can be run on Linux with Mono, Java is going to die.

- TrollRoxxoR: BecauseJavaDevelopersDontKnowHowToWriteCode

- RealG33k: Both your languages are for kids, C++ is way better but it’s for real developers only. Do you even know what SOLID means?

- HipsterGeek: So old and lame … you should try Node.js, it’s based on asynchronous calls and it’s very fast.

- LinusTorvalds: Pussies, a real developer uses C or assembly. You can’t have performances with those high level shits.

 

​	I hate PHP. I can’t explain why; it must be because I tried to learn it when I was 14 and it messed with my brain. But guess what, you’re reading this post on a server using PHP/NGINX (which is a **kickass（活力、粗暴）** server by the way). I’m good with Java. So, I could have used a Java framework running on a fast fat JVM. But, WordPress is a great platform. It’s often looked down by purists but it clearly answers my needs. The aim of my blog is not to be the fastest in the world (though it has surprisingly but painfully survived 2 Hacker News and Reddit front pages involving 500 simultaneous connections). I just want a user-friendly interface where I can share my thoughts.



**Which leads to my point: there is no best programming language, it depends on the situation.**

 

1) Do you need performances?

​	If yes, what kind of performances are we talking about?

- Seconds? Every language can do it!
- Milliseconds? Every language with good programmers can do it.
- Microseconds? At this step, you can remove all the interpreted languages (like python, which is a good language). I know that a **well-tuned（调整好的）** JVM with very good Java programmers can do it. I imagine that it’s the same for C#. Of course, a pure-compiled language can deal with that. But in all these cases the programmer’s skills are more important than the language.
- Nanoseconds? Only assembly or maybe C can deal with that.

So, in most situations developers’ skills are what matters.



2) What’s about the ecosystem?

​	More than the language itself, the ecosystem is important. I’ve used Visual Studio during my scholarship and I have been amazed by the **coherency（一致性）** of Microsoft’s ecosystem.

 	Now, I’m more an Eclipse guy. Even in the Java community, Eclipse is looked down by purists who now use IntelliJ IDEA. Eclipse is an open source software developed by different people and it’s clearly visible (in a bad way). Compared to the coherency of Visual Studio, you’ll find different logics in the different plugins of Eclipse.

​	But, if having tools is great, knowing how to use them is better. For example, when I started in Java, I was very slow. I learned by hearth some Eclipse keywords and it’s changed my developer life. I’ve also looked for useful plugins, and Eclipse has plenty of them, because it’s a rich ecosystem.

 

3) What’s about the online help?

​	Ok, you’re using your kickass programming language but don’t tell me you know every side of this language by hearth. Having a well known language is useful when you need help. A simple Google or StackOverflow search and you get your answer by Ninja_Guru_666 and I_AM_THE_EXPERT. If you’re more like an in-depth programmer, you can also check for the official documentation assuming it exists for the problem you’re looking for.

 

4) What are the skills of the team?

​	If the developers don’t really know how a computer works, using a compiled language is a suicidal move. And, compared to the purists, I don’t see why knowing (exactly) how a computer works makes you a good developer (though, I must admit, it helps; but there are more important skills).

​	It’s better not using the best tool but a known one. Moreover, many developers are fan boys. Using their preferred language will help them to stay motivated on the project.

 

5) The business side

​	An objective point of view is to see what the most in-demand languages are. It doesn’t mean they’re the best but at least you’ll get a job. In this case, Java, C#, PHP, SQL and JavaScript are clearly above all (at least in France).

​	Moreover, as a technical leader, it’s always good to check the skills in the market before choosing a technology. If you choose the best but rare technology to deal with your problem, good luck for finding skilled developers on the technology.

​	But what’s true in 2015 might change in 2018. ActionScript was a must have not so long ago. Likewise, with Swift, all the hours spent on Objective C will become obsolete in a few years.

To conclude, I’ll end up with a lame and (I hope) obvious conclusion: **there are no best programming languages or best frameworks; what’s best now might not exist tomorrow. A programming language is just a tool; what matters is the way you overcome your problems.**





## 05-31:

**Why are computer science degrees so math intensive when the field doesn't seem to use much math at all?**
	Well, Jamie Moore, you’ve been a developer for a whopping four years. Maybe you finally got past “**Associate(副的)** Software Developer.” You’ve been working on the easiest problems, which perhaps don’t use much math or computer science. If you continue to putter away as a web developer, maybe you never will use any math.

​	But there are software developers who solve hard problems in **demanding（难以满足）** jobs, and I can tell you from my actual experience, we use a shit-ton of math. We have to recognize and often invent novel algorithms. We build data structures, rather than relying on the pre-made ones in our programming language. We create compilers and interpreters for new languages. We apply new science to software development.

​	If you never try these things, I can see how you might find math irrelevant to computer science, but I assure you it is very relevant.





## 06-01:

**What happens if a programmer creates a lot of code only they understand for an important project, and then leaves?**
	Been there, seen that, got the coffee mug.

​	What happens is that if the programmer was reasonably good, the team works around this code and tries not to modify it. A **legend(传说)** grows up about what you have to do to make this **cranky(古怪的)**, **indecipherable(无法解释的)** code work. Often the developer himself becomes a legend. People praise him even though they don’t understand his work.

​	Eventually, this code needs to be modified. Some other engineer comes along who is willing to dig into the code until they understand it. What they discover is often that the code is a mess, that it was written while the legendary original developer was learning how to use new language idioms, and that’s why it is a mess. Sometimes it is discovered that the performance of this legendary code is horrible, or that the code often does not work as the legend says it should, so that it is the source of **subtle（微妙的、不易察觉的）** bugs.

​	The new engineer makes an effort to refactor the legendary code. This is met with expressions of horror from the other devs and their manager, because this code is legendary for its complexity.

​	Companies have code like this because they don’t have good development processes featuring code review and module tests. Perhaps the company dies before this code can be fixed.





## 06-02:

​	Today’s Internet is **arguably(可论证地)** the largest engineered system ever created by mankind, with hundreds of millions of connected computers, communication links, and **switches(交换机)**; with billions of users who connect via laptops, **tablets（平板）**, and smartphones; and with an array of new Internet-connected “things” including game consoles, **surveillance（监控）** systems, watches, eye glasses, **thermostats（温度调节器）**, **body scales（体重秤）**, and cars. Given that the Internet is so large and has so many **diverse（不同的）** components and uses, is there any hope of understanding how it works? Are there guiding principles and structure that can provide a foundation for understanding such an amazingly large and complex system? And if so, is it possible that it actually could be both interesting and fun to learn about computer networks? Fortunately, the answer to all of these questions is a resounding YES! Indeed, it’s our aim in this book to provide you with a modern introduction to the dynamic field of computer networking, giving you the principles and practical insights you’ll need to understand not only today’s networks, but tomorrow’s as well.

​	This first chapter presents a **broad（广泛）** overview of computer networking and the Internet. Our goal here is to paint a broad picture and set the context for the rest of this book, to see the forest through the trees. We’ll cover a lot of ground in this introductory chapter and discuss a lot of the pieces of a computer network, without losing sight of the big picture.

​	We’ll structure our overview of computer networks in this chapter as follows. After introducing some basic terminology and concepts, we’ll first examine the basic hardware and software components that make up a network. We’ll begin at the network’s edge and look at the end systems and network applications running in the network. We’ll then explore the core of a computer network, examining the links and the switches that transport data, as well as the access networks and physical media that connect end systems to the network core. We’ll learn that the Internet is a network of networks, and we’ll learn how these networks connect with each other.

​	After having completed this overview of the edge and core of a computer network, we’ll take the broader and more abstract view in the **second half** of this chapter. We’ll examine delay, loss, and throughput of data in a computer network and provide simple quantitative models for end-to-end throughput and delay: models that take into account transmission, propagation, and queuing delays. We’ll then introduce some of the key architectural principles in computer networking, **namely（也就是）**, protocol layering and service models. We’ll also learn that computer networks are vulnerable to many different types of attacks; we’ll survey some of these attacks and consider how computer networks can be made more secure. Finally, we’ll close this chapter with a brief history of computer networking.



## 06-03:

**1.1 What Is the Internet?**

**1.1.1 A Nuts-and-Bolts Description**

​	In this book, we’ll use the public Internet, a specific computer network, as our principal vehicle for discussing computer networks and their protocols. But what is the Internet? There are a couple of ways to answer this question. First, we can describe the **nuts and bolts（具体细节、描述）** of the Internet, that is, the basic hardware and software components that make up the Internet. Second, we can describe the Internet in terms of a networking infrastructure that provides services to distributed applications. Let’s begin with the nuts-and-bolts description, using Figure 1.1 to illustrate our discussion.

​	The Internet is a computer network that interconnects billions of computing devices **throughout（遍及）** the world. Not too long ago, these computing devices were primarily traditional desktop PCs, Linux workstations, and so-called servers that store and transmit information such as Web pages and e-mail messages. Increasingly, however, nontraditional Internet “things” such as laptops, smartphones, tablets, TVs, gaming consoles, thermostats, home security systems, home appliances, watches, eye glasses, cars, traffic control systems and more are being connected to the Internet. Indeed, the term computer network is beginning to sound a bit dated, given the many nontraditional devices that are being hooked up to the Internet. In Internet **jargon（行话）**, all of these devices are called hosts or end systems. By some estimates, in 2015 there were about 5 billion devices connected to the Internet, and the number will reach 25 billion by 2020 [Gartner 2014]. It is estimated that in 2015 there were over 3.2 billion Internet users worldwide, approximately 40% of the world population [ITU 2015]

​	End systems are connected together by a network of communication links and packet switches. We’ll see in Section 1.2 that there are many types of communication links, which are made up of different types of physical media, including **coaxial cable（同轴电缆）**, copper wire, **optical fiber（光纤）**, and radio **spectrum（频谱）**. Different links can transmit data at different rates, with the transmission rate of a link measured in bits/second. When one end system has data to send to another end system, the sending end system segments the data and adds header bytes to each segment. The resulting packages of information, known as packets in the jargon of computer networks, are then sent through the network to the destination end system, where they are **reassembled（重新组装）** into the original data.

​	A packet switch takes a packet arriving on one of its incoming communication links and forwards that packet on one of its outgoing communication links. Packet switches come in many shapes and flavors, but the two most prominent types in today’s Internet are **routers and link-layer switches**. Both types of switches forward packets toward their ultimate destinations. Link-layer switches are typically used in access networks, while routers are typically used in the network core. The sequence of communication links and packet switches traversed by a packet from the sending end system to the receiving end system is known as a route or path through the network. Cisco predicts annual global IP traffic will pass the zettabyte (10 bytes) threshold by the end of 2016, and will reach 2 zettabytes per year by 2019 [Cisco VNI 2015].

​	Packet-switched networks (which transport packets) are in many ways similar to transportation networks of highways, roads, and intersections (which transport vehicles). Consider, for example, a factory that needs to move a large amount of **cargo（货物）** to some destination **warehouse（仓库）** located thousands of kilometers away. At the factory, the cargo is segmented and loaded into a fleet of trucks. Each of the trucks then independently travels through the network of highways, roads, and intersections to the destination warehouse. At the destination warehouse, the cargo is unloaded and grouped with the rest of the cargo arriving from the same shipment. Thus, in many ways, packets are analogous to trucks, communication links are analogous to highways and roads, packet switches are analogous to intersections, and end systems are analogous to buildings. Just as a truck takes a path through the transportation network, a packet takes a path through a computer network.

​	End systems access the Internet through Internet Service Providers (ISPs), including residential ISPs such as local cable or telephone companies; corporate ISPs; university ISPs; ISPs that provide WiFi access in airports, hotels, coffee shops, and other public places; and cellular data ISPs, providing mobile access to our smartphones and other devices. Each ISP is in itself a network of packet switches and communication links. ISPs provide a variety of types of network access to the end systems, including residential broadband access such as cable modem or DSL, high-speed local area network access, and mobile wireless access. ISPs also provide Internet access to content providers, connecting Web sites and video servers directly to the Internet. The Internet is all about connecting end systems to each other, so the ISPs that provide access to end systems must also be interconnected. These lower-tier ISPs are interconnected through national and international upper-tier ISPs such as Level 3 Communications, AT&T, Sprint, and NTT. An upper-tier ISP consists of high-speed routers interconnected with high-speed fiber-optic links. Each ISP network, whether upper-tier or lower-tier, is 21 managed independently, runs the IP protocol (see below), and conforms to certain naming and address conventions. We’ll examine ISPs and their interconnection more closely in Section 1.3

​	End systems, packet switches, and other pieces of the Internet run protocols that control the sending and receiving of information within the Internet. The Transmission Control Protocol (TCP) and the Internet Protocol (IP) are two of the most important protocols in the Internet. The IP protocol specifies the format of the packets that are sent and received among routers and end systems. The Internet’s principal protocols are collectively known as TCP/IP. We’ll begin looking into protocols in this introductory chapter. But that’s just a start—much of this book is concerned with computer network protocols!

​	Given the importance of protocols to the Internet, it’s important that everyone agree on what each and every protocol does, so that people can create systems and products that interoperate. This is where standards come into play. Internet standards are developed by the Internet Engineering Task Force (IETF) [IETF 2016]. The IETF standards documents are called requests for comments (RFCs). RFCs started out as general requests for comments (hence the name) to resolve network and protocol design problems that faced the precursor to the Internet [Allman 2011]. RFCs tend to be quite technical and detailed. They define protocols such as TCP, IP, HTTP (for the Web), and SMTP (for e-mail). There are currently more than 7,000 RFCs. Other bodies also specify standards for network components, most notably for network links. The IEEE 802 LAN/MAN Standards Committee [IEEE 802 2016], for example, specifies the Ethernet and wireless WiFi standards





## 06-04:

**1.1.2 A Services Description** 

​	Our discussion above has identified many of the pieces that make up the Internet. But we can also describe the Internet from an entirely different angle—namely, as an infrastructure that provides services to applications. In addition to traditional applications such as e-mail and Web surfing, Internet applications include mobile smartphone and tablet applications, including Internet messaging, mapping with real-time road-traffic information, music streaming from the cloud, movie and television streaming, online social networks, video conferencing, multi-person games, and location-based recommendation systems. The applications are said to be distributed applications, since they involve multiple end systems that exchange data with each other. Importantly, Internet applications run on end systems— they do not run in the packet switches in the network core. Although packet switches facilitate the exchange of data among end systems, they are not concerned with the application that is the source or sink of data.

​	 Let’s explore a little more what we mean by an infrastructure that provides services to applications. To this end, suppose you have an exciting new idea for a distributed Internet application, one that may greatly benefit humanity or one that may simply make you rich and famous. How might you go about transforming this idea into an actual Internet application? Because applications run on end systems, you are going to need to write programs that run on the end systems. You might, for example, write your programs in Java, C, or Python. Now, because you are developing a distributed Internet application, the programs running on the different end systems will need to send data to each other. And here we get to a central issue—one that leads to the **alternative（另一种）** way of describing the Internet as a platform for applications. How does one program running on one end system instruct the Internet to deliver data to another program running on another end system?

​	End systems attached to the Internet provide a socket interface that specifies how a program running on one end system asks the Internet infrastructure to deliver data to a specific destination program running on another end system. This Internet socket interface is a set of rules that the sending program must follow so that the Internet can deliver the data to the destination program. We’ll discuss the Internet socket interface in detail in Chapter 2. For now, let’s draw upon a simple analogy, one that we will frequently use in this book. Suppose Alice wants to send a letter to Bob using the postal service. Alice, of course, can’t just write the letter (the data) and drop the letter out her window. Instead, the postal service requires that Alice put the letter in an envelope; write Bob’s full name, address, and zip code in the center of the envelope; seal the envelope; put a stamp in the upper-right-hand corner of the envelope; and finally, drop the envelope into an official postal service mailbox. Thus, the postal service has its own “postal service interface,” or set of rules, that Alice must follow to have the postal service deliver her letter to Bob. In a similar **manner（方式）**, the Internet has a socket interface that the program sending data must follow to have the Internet deliver the data to the program that will receive the data. 

​	The postal service, of course, provides more than one service to its customers. It provides express delivery, reception confirmation, ordinary use, and many more services. In a similar manner, the Internet provides multiple services to its applications. When you develop an Internet application, you too must choose one of the Internet’s services for your application. We’ll describe the Internet’s services in Chapter 2.

​	We have just given two descriptions of the Internet; one in terms of its hardware and software components, the other in terms of an infrastructure for providing services to distributed applications. But perhaps you are still confused as to what the Internet is. What are packet switching and TCP/IP? What are routers? What kinds of communication links are present in the Internet? What is a distributed application? How can a thermostat or body scale be attached to the Internet? If you feel a bit **overwhelmed（被压倒）** by all of this now, don’t worry—the purpose of this book is to introduce you to both the nuts and bolts of the Internet and the principles that govern how and why it works. We’ll explain these important terms and questions in the following sections and chapters.



## 06-05:

**1.1.3 What Is a Protocol?** 

​	Now that we’ve got a bit of a feel for what the Internet is, let’s consider another important **buzzword(流行术语)** in computer networking: protocol. What is a protocol? What does a protocol do?

**A Human Analogy**

 It is probably easiest to understand the notion of a computer network protocol by first considering some human analogies, since we humans execute protocols all of the time. Consider what you do when you want to ask someone for the time of day. A typical exchange is shown in Figure 1.2. Human protocol (or good manners, at least) **dictates（命令）** that one first offer a greeting (the first “Hi” in Figure 1.2) to initiate communication with someone else. The typical response to a “Hi” is a returned “Hi” message. **Implicitly（含蓄地）**, one then takes a **cordial（友好的）** “Hi” response as an indication that one can **proceed（继续进行）** and ask for the time of day. A different response to the initial “Hi” (such as “Don’t bother me!” or “I don’t speak English,” or some unprintable reply) might indicate an unwillingness or inability to communicate. In this case, the human protocol would be not to ask for the time of day. Sometimes one gets no response at all to a question, in which case one typically gives up asking that person for the time. Note that in our human protocol, there are specific messages we send, and specific actions we take in response to the received reply messages or other events (such as no reply within some given amount of time). Clearly, transmitted and received messages, and actions taken when these messages are sent or received or other events occur, play a central role in a human protocol. If people run different protocols (for example, if one person has manners but the other does not, or if one understands the concept of time and the other does not) the protocols do not interoperate and no useful work can be accomplished. The same is true in networking—it takes two (or more) communicating entities running the same protocol in order to accomplish a task.

​	Let’s consider a second human analogy. Suppose you’re in a college class (a computer networking class, for example!). The teacher is **droning（发出嗡嗡声）** on about protocols and you’re confused. The teacher stops to ask, “Are there any questions?” (a message that is transmitted to, and received by, all students who are not sleeping). You raise your hand (transmitting an implicit message to the teacher). Your teacher acknowledges you with a smile, saying “Yes . . .” (a transmitted message encouraging you to ask your question—teachers love to be asked questions), and you then ask your question (that is, transmit your message to your teacher). Your teacher hears your question (receives your question message) and answers (transmits a reply to you). Once again, we see that the transmission and receipt of messages, and a set of conventional actions taken when these messages are sent and received, are at the heart of this question-and-answer protocol.



**Network Protocols**

​	A network protocol is similar to a human protocol, except that the entities exchanging messages and taking actions are hardware or software components of some device (for example, computer, smartphone, tablet, router, or other network-capable device). All activity in the Internet that involves two or more communicating remote entities is governed by a protocol. For example, hardware-implemented protocols in two physically connected computers control the flow of bits on the “wire” between the two network interface cards; congestion-control protocols in end systems control the rate at which packets are transmitted between sender and receiver; protocols in routers determine a packet’s path from source to destination. Protocols are running everywhere in the Internet, and consequently much of this book is about computer network protocols.

​	As an example of a computer network protocol with which you are probably familiar, consider what happens when you make a request to a Web server, that is, when you type the URL of a Web page into your Web browser. The scenario is illustrated in the right half of Figure 1.2. First, your computer will send a connection request message to the Web server and wait for a reply. The Web server will eventually receive your connection request message and return a connection reply message. Knowing that it is now OK to request the Web document, your computer then sends the name of the Web page it wants to fetch from that Web server in a GET message. Finally, the Web server returns the Web page (file) to your computer.



​	Given the human and networking examples above, the exchange of messages and the actions taken when these messages are sent and received are the key defining elements of a protocol: 

> A protocol defines the format and the order of messages exchanged between two or more communicating entities, as well as the actions taken on the transmission and/or receipt of a message or other event. 



​	The Internet, and computer networks in general, make extensive use of protocols. Different protocols are used to accomplish different communication tasks. As you read through this book, you will learn that some protocols are simple and straightforward, while others are complex and intellectually deep. Mastering the field of computer networking is equivalent to understanding the what, why, and how of networking protocols.



**1.2 The Network Edge**

​	In the previous section we presented a high-level overview of the Internet and networking protocols. We are now going to **delve（钻研）** a bit more deeply into the components of a computer network (and the Internet, in particular). We begin in this section at the edge of a network and look at the components with which we are most familiar—namely, the computers, smartphones and other devices that we use on a daily basis. In the next section we’ll move from the network edge to the network core and examine switching and routing in computer networks.

​	Recall from the previous section that in computer networking jargon, the computers and other devices connected to the Internet are often referred to as end systems. They are referred to as end systems because they sit at the edge of the Internet, as shown in Figure 1.3. The Internet’s end systems include desktop computers (e.g., desktop PCs, Macs, and Linux boxes), servers (e.g., Web and e-mail servers), and mobile devices (e.g., laptops, smartphones, and tablets). Furthermore, an increasing number of non-traditional “things” are being attached to the Internet as end systems (see the Case History feature).

​	End systems are also referred to as hosts because they host (that is, run) application programs such as a Web browser program, a Web server program, an e-mail client program, or an e-mail server program. Throughout this book we will use the terms hosts and end systems interchangeably; that is, host = end system. Hosts are sometimes further divided into two categories: clients and servers. Informally, clients tend to be desktop and mobile PCs, smartphones, and so on, whereas servers tend to be more powerful machines that store and distribute Web pages, stream video, relay e-mail, and so on. Today, most of the servers from which we receive search results, e-mail, Web pages, and videos reside in large data centers. For example, Google has 50-100 data centers, including about 15 large centers, each with more than 100,000 servers.

CASE HISTORY:THE INTERNET OF THINGS 

​	Can you imagine a world in which just about everything is wirelessly connected to the Internet? A world in which most people, cars, bicycles, eye glasses, watches, toys, hospital equipment, home sensors, classrooms, video surveillance systems, atmospheric sensors, store-shelf products, and pets are connected? This world of the Internet of Things (IoT) may actually be just around the corner. By some estimates, as of 2015 there are already 5 billion things connected to the Internet, and the number could reach 25 billion by 2020 [Gartner 2014]. These things include our smartphones, which already follow us around in our homes, offices, and cars, reporting our geolocations and usage data to our ISPs and Internet applications. But in addition to our smartphones, a wide-variety of non-traditional “things” are already available as products. For example, there are Internet-connected **wearables(可穿戴的)**, including watches (from Apple and many others) and eye glasses. Internet-connected glasses can, for example, upload everything we see to the cloud, allowing us to share our visual experiences with people around the world in realtime. There are Internet-connected things already available for the smart home, including Internet-connected thermostats that can be controlled remotely from our smartphones, and Internet-connected body scales, enabling us to graphically review the progress of our diets from our smartphones. There are Internet-connected toys, including dolls that recognize and interpret a child’s speech and respond appropriately. The IoT offers potentially revolutionary benefits to users. But at the same time there are also huge security and privacy risks. For example, attackers, via the Internet, might be able to hack into IoT devices or into the servers collecting data from IoT devices. For example, an attacker could **hijack（劫持）** an Internet-connected doll and talk directly with a child; or an attacker could hack into a database that stores personal health and activity information collected from wearable devices. These security and privacy concerns could **undermine（破坏）** the consumer confidence necessary for the technologies to meet their full potential and may result in less widespread adoption [FTC 2015].
