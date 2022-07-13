## 07-11:

​	The Java language is a remarkable example of programming language evolution. Java builds on the familiar and useful features of C++ while removing its complex, dangerous, and **superfluous(多余的)** elements. The result is a language that is safer, simpler, and easier to use. The following sections describe Java in contrast to C++. 

**Java Is Familiar and Simple** 

​	If you have ever programmed in C++, you will find Java’s appeal to be **instantaneous（即时的）**. Since Java’s syntax mirrors that of C++, you will be able to write Java programs within minutes. Your first programs will come quickly and easily, with very little programming overhead. 

​	You will have the feeling that you have eliminated a lot of **clutter（杂乱的）** from your programs—and you will have. All the **cryptic（神秘）** header files and **preprocessor（预处理）** statements of C and C++ are gone. All the **arcane（神秘）** #define statements and **typedefs（类定义的）** have been taken away. You will no longer have to **delve（钻研）** through several levels of header files to correctly reference API calls. And no one will have to **suffer（受苦）** to **figure out（理解）** how to use your software. 

​	Java programs simply import the software packages they need. These packages may be in another directory, on another drive, or on a machine on the other side of the Internet. The Java compiler and interpreter figure out what objects are referenced and supply the necessary linkage. 



**Java Is Object-Oriented** 

​	If you think C++ is an object-oriented programming language, you are in for a big surprise . After using Java to write a few programs, you’ll get a better feeling for what object-oriented software is all about. I know I did. 

​	Java deals with classes and objects, pure and simple . They **aren’t just（不仅仅是）** more data structures that are available to the programmer—they are the basis for the entire programming language. 

​	In C++, you can declare a class, but you don’t have to. You can declare a structure or a union instead. You can declare a whole bunch of loosely associated variables and use them with C-style functions. In Java, classes and objects are at the center of the language. Everything else revolves around them. You can’t declare functions and procedures. They don’t exist. You can’t use structures, unions, or typedefs. They’re gone, too. You either use classes and objects or you don’t use Java. It’s that simple. 

​	Java provides all the **luxuries（奢侈）** of object-oriented programming: class **hierarchy（层次）**, inheritance, **encapsulation（封装）**, and **polymorphism（多态）**—in a context that is truly useful and efficient. 

​	The main reason for developing object-oriented software, besides clarity and simplicity, is the **desperate（渴望的）** hope that somehow the objects you develop will be reused. Java not only encourages software reuse, it demands it. To write any sort of Java program, no matter how simple, you must build on the classes and methods of the Java API. 

​	Once you have begun developing software in Java, you have two choices: 

- Build on the classes you have developed, thereby reusing them. 

-  Rewrite your software from scratch, copying and tailoring useful parts of existing software. 

​	With Java, **the temptation to start from scratch is no longer appealing**. Java’s object-oriented structure forces you to develop more useful, more **tailorable（可裁剪）**, and much simpler software the first time around. 



**Java Is Safer and More Reliable** 

​	Java is safer to use than C++ because it keeps you from doing the things that you do badly, while making it easier to do the things that you do well. Java won’t automatically convert data types. You have to **explicitly（显示）** convert from one class to another. C++, under the most **undesirable（不受欢迎、不良的）** conditions, will automatically convert one type to another. It has all the flexibility of assembly code. Java doesn’t assume that you know what you are doing. It makes sure that you do. C++ pointers don’t exist in Java. You can no longer access objects indirectly or by chance. You don’t need to. You declare objects and reference those objects directly. Complex pointer arithmetic is avoided. If you need an indexed set of objects, you can use an array of objects. The concept of “the address of an object” is eliminated from the programming model, and another assembly language dinosaur is laid to rest. As a result, it becomes much easier to do things correctly in Java. Java’s reliability extends beyond the language level to the compiler and the runtime system. Compile-time checks identify many programming errors that go undetected in other programming languages. These checks go beyond syntactic checking to ensure that statements are semantically correct. 

​	Runtime checks are also more extensive and effective. Remember your teacher or mom telling you to “Check your work twice to make sure it’s right”? The Java linker understands class types and performs compiler-level type checking, adding **redundancy（冗余）** to reliability. It also performs bounds checking and eliminates indirect object access, even under error conditions. 



**Java Is Secure** 

​	If you gave a **skilled（熟练）** hacker a program written in C or C++ and told him to find any security **flaws（缺陷）**, there are half a dozen things that he would immediately look for: gaining access to the operating system, causing an unexpected return of control, overwriting critical memory areas, acquiring the ability to **spoof（欺骗）** or modify other programs, browsing for security information, and gaining unauthorized access to the file system. Why is C or C++ more vulnerable than Java? When a programmer develops software, he or she usually focuses on how to get the software to work correctly and efficiently. C and C++ do not constrain the programmer from meeting these goals and provide a number of flexible features that enable the programmer to meet his end. The hacker is also able to take advantage of these features and use them in ways that weren’t originally intended, causing the undesirable consequences identified in the previous paragraph. **In short, C and C++ provide a great offense, but no defense.** Java, on the other hand, is defensive by nature. Every time a Java-enabled browser downloads a compiled Java class, such as an applet, it runs the risk of running Trojan horse code. Because of this **ever-present（经常存在）** threat, it subjects the code to a series of checks that ensure that it is correct and secure. The Java runtime system is designed to enforce a security policy that prevents execution of **malicious（恶意的）** code. It does this by remembering how objects are stored in memory and enforcing correct and secure access to those objects according to its security rules. It performs bytecode verification by passing compiled classes through a simple theorem prover that either proves that the code is secure or prevents the code from being loaded and executed. The class is Java’s basic execution unit and security is implemented at the class level. The Java runtime system also **segregates（使隔离）** software according to its origin. Classes from the local system are processed separately from those of other systems. This prevents remote systems from replacing local system software with code that is less trustworthy. 

Java-enabled browsers, such as HotJava , allow the user to control the accesses that Java software may make of the local system. When a Java applet needs permission to access local resources, such as files, a security dialog box is presented to the user, requesting explicit user permission. This “Mother may I?” approach ensures that the user always has the final say in the security of his system. 



**Java Is Multithreaded** 

​	Java, like Ada, and unlike other languages, provides built-in language support for multithreading. Multithreading allows more than one thread of execution to take place within a single program. This allows your program to do many things at once: make the Duke dance, play his favorite tune, and interact with the user, seemingly all at the same time. Multithreading is an important asset because it allows the programmer to write programs as independent threads, rather than as a **convoluted（复杂的）** **gaggle（一群）** of **intertwined（缠绕）** activities. Multithreading also allows Java to use idle CPU time to perform necessary garbage collection and general system maintenance, enabling these functions to be performed with less impact on program performance. Writing multithreaded programs is like dating several people concurrently. Everything works fine until the threads start to interact with each other in unexpected ways. Java provides the support necessary to make multithreading work safely and correctly. Java supports multithreading by providing synchronization capabilities that ensure that threads share information and execution time in a way that is thread safe. 



**Java Is Interpreted and Portable**

​	 While it is true that compiled code will almost always run more quickly than interpreted code, it is also true that interpreted code can usually be developed and fielded more inexpensively, more quickly, and in a more flexible manner. It is also usually much more portable. Java, in order to be a truly platform-independent programming language, must be interpreted. It does not run as fast as compiled native code, but it doesn’t run much slower, either. For the cases where execution in native machine code is absolutely essential, work is **underway（在进行中）** to translate Java bytecode into machine code as it is loaded. The advantages of being interpreted **outweigh（重要）** any performance impacts. Because Java is interpreted, it is much more portable. If an operating system can run the Java interpreter and support the Java API, then it can faithfully run all Java programs. Interpreted programs are much more easily kept up-to-date. You don’t have to recompile them for every change. In Java, recompilation is automatic. The interpreter detects the fact that a program’s bytecode file is out-of-date with respect to its source code file and recompiles it as it is loaded. Because of Java’s interpreted nature, linking is also more powerful and flexible. Java’s runtime system supports dynamic linking between local class files and those that are downloaded from across the Internet. This feature provides the basis for Web programming.



**Java Is the Programming Language of the Web** 

​	Java has become the def acto programming language of the Web. It is being licensed by nearly every major software company. It has some **offshoots（分支、衍生物）** and potential competition, such as JavaScript and VBScript , but it remains the first Web programming language and the most powerful language for developing platform-independent software. Java is also evolving beyond the Web and becoming a key component in distributed application development. Some releases of Sun’s products emphasize Java’s importance to distributed object-based software development. Several other vendors have introduced products that enable Java to be integrated into the Common Object Request Broker Architecture (CORBA ), which is the framework for distributed object communication.





## 07-12:

**Computer Program** 

**I. INTRODUCTION** 

​	A computer program is a set of instructions that directs a computer to perform some processing function or combination of functions. For the instructions to be carried out, a computer must execute a program, that is, the computer reads the program, and then follows the steps encoded in the program in a precise order until completion. A program can be executed many different times, with each execution **yielding（产生、屈服）** a potentially different result depending upon the options and data that the user gives the computer. 

​	Programs **fall into（陷入、分成）** two major classes: application programs and operating systems. An application program is one that carries out some function directly for a user, such as word processing or game playing. An operating system is a program that manages the computer and the various resources and devices connected to it, such as RAM (random access memory), hard drives, monitors, keyboards, printers, and modems, so that they may be used by other programs. Examples of operating systems are DOS, Windows 95, OS/2, and UNIX. 



**II. PROGRAM DEVELOPMENT**

​	 Software designers create new programs by using special applications programs, often called utility programs or development programs. A programmer uses another type of program called a text editor to write the new program in a special notation called a programming language. With the text editor, the programmer creates a text file, which is an ordered list of instructions, also called the program source file. The **individual（单独的）** instructions that make up the program source file are called source code. At this point, a special applications program translates the source code into machine language, or object code—a format that the operating system will recognize as a proper program and be able to execute. 

​	Three types of applications programs translate from source code to object code: compilers, interpreters, and assemblers. The three operate differently and on different types of programming languages, but they serve the same purpose of translating from a programming language into machine language. 

​	A compiler translates text files written in a high-level programming language—such as FORTRAN, C, or Pascal—from the source code to the object code all at once. This differs from the approach taken by interpreted languages such as BASIC, in which a program is translated into object code statement by statement as each instruction is executed. The advantage to interpreted languages is that they can begin executing the program immediately instead of having to wait for all of the source code to be compiled. Changes can also be made to the program fairly quickly without having to wait for it to be compiled again. The disadvantage of interpreted languages is that they are slow to execute, since the entire program must be translated one instruction at a time, each time the program is run. On the other hand, compiled languages are compiled only once and thus can be executed by the computer much more quickly than interpreted languages. For this reason, compiled languages are more common and are almost always used in professional and scientific applications. 

​	Another type of translator is the assembler, which is used for programs or parts of programs written in assembly language. Assembly language is another programming language, but it is much more similar to machine language than other types of high-level languages. In assembly language, a single statement can usually be translated into a single instruction of machine language. Today, assembly language is rarely used to write an entire program, but is instead most often used when the programmer needs to directly control some aspect of the computer’s function. Programs are often written as a set of smaller pieces, with each piece representing some aspect of the overall application program. After each piece has been compiled separately, a program called a linker combines all of the translated pieces into a single executable program. 

​	Programs seldom work correctly the first time, so a program called a debugger is often used to help find problems called bugs. Debugging programs usually detect an event in the executing program and point the programmer back to the origin of the event in the program code. Recent programming systems, such as Java, use a combination of approaches to create and execute programs. A compiler takes a Java source program and translates it into an intermediate form. Such intermediate programs are then transferred over the Internet into computers where an interpreter program then executes the intermediate form as an application program. 



**III. PROGRAM ELEMENTS**

​	Most programs are built from just a few kinds of steps that are repeated many times in different contexts and in different combinations throughout the program. The most common step performs some computation, and then proceeds to the next step in the program, in the order specified by the programmer. Programs often need to repeat a short series of steps many times, for instance in looking through a list of game scores and finding the highest score. Such **repetitive（多次重复的）** sequences of code are called loops. 

​	One of the capabilities that make computers so useful is their ability to make conditional decisions and perform different instructions based on the values of data being processed. If-then-else statements implement this function by testing some piece of data and then selecting one of two sequences of instructions on the basis of the result. One of the instructions in these alternatives may be a goto statement that directs the computer to select its next instruction from a different part of the program. For example, a program might compare two numbers and branch to a different part of the program depending on the result of the comparison: 

​	If x is greater than y then goto instruction #10 else continue 

​	Programs often use a specific sequence of steps more than once. Such a sequence of steps can be grouped together into a **subroutine（子程序）**, which can then be called, or accessed, as needed in different parts of the main program. Each time a subroutine is called, the computer remembers where it was in the program when the call was made, so that it can return there upon completion of the subroutine. Preceding each call, a program can specify that different data be used by the subroutine, allowing a very general piece of code to be written once and used in multiple ways. 

​	Most programs use several varieties of subroutines. The most common of these are functions, procedures, library routines, system routines, and device drivers. Functions are short subroutines that compute some value, such as computations of angles, which the computer cannot compute with a single basic instruction. Procedures perform a more complex function, such as sorting a set of names. Library routines are subroutines that are written for use by many different programs. System routines are similar to library routines but are actually found in the operating system. They provide some service for the application programs, such as printing a line of text. Device drivers are system routines that are added to an operating system to allow the computer to communicate with a new device, such as a scanner, modem, or printer. Device drivers often have features that can be executed directly as applications programs. This allows the user to directly control the device, which is useful if, for instance, a color printer needs to be realigned to attain the best printing quality after changing an ink cartridge. 



**IV. PROGRAM FUNCTION** 

​	Modern computers usually store programs on some form of magnetic storage media that can be accessed randomly by the computer, such as the hard drive disk permanently located in the computer, or a portable floppy disk. Additional information on such disks, called directories, indicates the names of the various programs on the disk, when they were written to the disk, and where the program begins on the disk media. When a user directs the computer to execute a particular application program, the operating system looks through these directories, locates the program, and reads a copy into RAM. The operating system then directs the CPU (central processing unit) to start executing the instructions at the beginning of the program. Instructions at the beginning of the program prepare the computer to process information by locating free memory locations in RAM to hold working data, retrieving copies of the standard options and defaults the user has indicated from a disk, and drawing initial displays on the monitor. The application program requests a copy of any information the user enters by making a call to a system routine. The operating system converts any data so entered into a standard internal form. The application then uses this information to decide what to do next—for example, perform some desired processing function such as reformatting a page of text, or obtain some additional information from another file on a disk. In either case, calls to other system routines are used to actually carry out the display of the results or the accessing of the file from the disk. When the application reaches completion or is prompted to quit, it makes further system calls to make sure that all data that needs to be saved has been written back to disk. It then makes a final system call to the operating system indicating that it is finished. The operating system then frees up the RAM and any devices that the application was using and awaits a command from the user to start another program. 



**V. HISTORY** 

​	People have been storing sequences of instructions in the form of a program for several centuries. Music boxes of the 18th century and player pianos of the late 19th and early 20th centuries played musical programs stored as series of metal pins, or holes in paper, with each line (of pins or holes) representing when a note was to be played, and the pin or hole indicating what note was to be played at that time. More elaborate control of physical devices became common in the early 1800s with French inventor Joseph Marie Jacquard’s invention of the punch-card controlled weaving loom. In the process of weaving a particular pattern, various parts of the loom had to be mechanically positioned. To automate this process, Jacquard used a single paper card to represent each positioning of the loom, with holes in the card to indicate which loom actions should be done. An entire tapestry could be encoded onto a deck of such cards, with the same deck yielding the same tapestry design each time it was used. Programs of over 24,000 cards were developed and used. 

​	The world’s first programmable machine was designed—although never fully built—by the English mathematician and inventor, Charles Babbage. This machine, called the Analytical Engine, used punch cards similar to those used in the Jacquard loom to select the specific arithmetic operation to apply at each step. Inserting a different set of cards changed the computations the machine performed. This machine had **counterparts（相当的人、同行）** for almost everything found in modern computers, although it was mechanical rather than electrical. Construction of the Analytical Engine was never completed because the technology required to build it did not exist at the time. The first card deck programs for the Analytical Engine were developed by British mathematician Augusta Ada Byron, daughter of the poet Lord Byron . For this reason she is recognized as the world’s first programmer. The modern concept of an internally stored computer program was first proposed by Hungarian-American mathematician John von Neumann in 1945. Von Neumann’s idea was to use the computer’s memory to store the program as well as the data. In this way, programs can be viewed as data and can be processed like data by other programs. This idea greatly simplifies the role of program storage and execution in computers. 



**VI. THE FUTURE** 

​	The field of computer science has grown rapidly since the 1950s due to the increase in their use. Computer programs have **undergone（经历）** many changes during this time in response to user need and advances in technology. Newer ideas in computing such as parallel computing, distributed computing, and artificial intelligence, have radically altered the traditional concepts that once determined program form and function. 

​	Computer scientists working in the field of parallel computing, in which multiple CPUs cooperate on the same problem at the same time, have introduced a number of new program models. In parallel computing parts of a problem are worked on simultaneously by different processors, and this speeds up the solution of the problem. Many challenges face scientists and engineers who design programs for parallel processing computers, because of the extreme complexity of the systems and the difficulty involved in making them operate as effectively as possible. Another type of parallel computing called distributed computing uses CPUs from many interconnected computers to solve problems. Often the computers used to process information in a distributed computing application are connected over the Internet. Internet applications are becoming a particularly useful form of distributed computing, especially with programming languages such as Java. In such applications, a user logs on  to a Web site and downloads a Java program onto their computer. When the Java program is run, it communicates with other programs at its home Web site, and may also communicate with other programs running on different computers or Web sites. 

​	Research into artificial intelligence (AI) has led to several other new styles of programming. Logic programs, for example, do not consist of individual instructions for the computer to follow blindly, but instead consist of sets of rules: if x happens then do y. A special program called an inference engine uses these rules to “reason” its way to a conclusion when presented with a new problem. Applications of logic programs include automatic monitoring of complex systems, and proving mathematical theorems. A **radically（根本的）** different approach to computing in which there is no program in the conventional sense is called a neural network. A neural network is a group of highly interconnected simple processing elements, designed to mimic the brain. Instead of having a program direct the information processing in the way that a traditional computer does, a neural network processes information depending upon the way that its processing elements are connected. Programming a neural network is accomplished by presenting it with known patterns of input and output data and adjusting the relative importance of the interconnections between the processing elements until the desired pattern matching is accomplished. Neural networks are usually simulated on traditional computers, but unlike traditional computer programs, neural networks are able to learn from their experience. 



## 07-13:

**Why Choose Visual Basic as a Web Programming Tool?**

​	Welcome to Web programming with Visual Basic. As you can probably tell by the title, the topic here is the integration of Visual Basic and the World Wide Web. 



**Why the World Wide Web?** 

​	You may ask, “Besides all the **hype（炒作）**, what good is the Web?” The answer is simple: the Web allows for the distribution of information over a wide area, to a wide audience at a low cost (compared to a WAN ). This network of networks enables users from across the world to access data on any computer whose administrator has deemed that the data should be made public using the Web. 

​	This opens up a lot of possibilities for both providing and gathering information. Couple the Web with the other features of the Internet (e-mail, network news, file repositories), and it’s easy to see all the potential applications of the Web. 

​	Here are a few ideas to get your mind going. First, it can provide a Web-based order entry form. This gives a remote salesman using a Web browser on a notebook computer the ability to place orders minutes after a deal is made. Another potential application is to provide a Visual Basic search engine that scans Web-based databases of résumés for keywords. Finally, it enables you to provide a custom Web browser to your customers. The browser allows access only to your Web site and even provides the ability to personalize the information on your Web server to match the customer. 

​	The applications are as wide open as the Web itself, and I’m sure that as more people jump on the Web **bandwagon（流行）** , more and more applications will spring up. 



**Why Choose Visual Basic as a Web Programming Tool?**

​	An important question at the start of any software design project is the choice of a language or languages to use. When you think about designing applications that use Web-based information, the question still applies: “Why should I use Visual Basic?” Visual Basic makes sense for the following reasons:

​	 Database **Connectivity**—By using ODBC or RDO , you can easily wrap database accessibility into a Visual Basic Web application. The question is no longer what can be done via the current set of Web tools but what can be done using Visual Basic. 

​	Up-to-date custom controls—The market for third party custom controls in Visual Basic is huge. At least 10 different companies currently make OCXs or VBXs for Internet programming. This is **reassuring（使安心的）** because a change in an Internet specification used somewhere in your application doesn’t **mandate（强制）** a change in the application’s code. Instead, it means upgrading a custom control   and then performing the much easier task of verifying that the control works as intended with the application. 

​	OLE—The ability to control and to access data from other applications is a big plus to application development. Not only can a Visual Basic application control several OLE-enabled Web browsers, but you can also relay information from the Web to an OLE-enabled application. 

​	The Windows user interface—The usability of a Windows application far **exceeds（超过）** the current set of HTML tags that allow for textboxes, comboboxes, and buttons. 



**Combining Visual Basic and the Web** 

​	The merging of Visual Basic and the ability to access real-time, distributed information using the Internet produces an interesting and very powerful tool. In the constant **flux（不断变化）** of the Internet, Visual Basic becomes a very practical choice for Web application development thanks to Visual Basic’s rapid application development aspect. 

​	Visual Basic can be used to create both client-side and server-side Web applications. A Web browser such as Microsoft’s Internet Explorer is one example of a client-side application. It is used to “surf” the Web—browsing the Web pages at a Web site and moving to other pages or to a completely different Web site by using the hyperlinks provided on most Web pages. Another example of a client-side application is an application that retrieves stock **quotes（引用、报价）** from a quote provider’s Web sites and provides the quotes to the user in some fashion. This application is not a Web browser but does access Web-based information. 

​	Server-side applications run alongside a Web server, such as Microsoft’s Internet Information Server. The server-side application is executed under the direction of the Web server, typically in response to a request made by a client-side application such as a Web browser. Server-side applications typically serve as gateways between a user’s Web browser and information stored on the Web server that is not typically accessible using a Web browser. Such information can include database tables, information-providing machines attached to the server, and even OLE-enabled applications to which the server has access. 

**Past, Present, and Future** 

​	In the beginning, the Web was **predominantly（主要地）** used by, maintained by, and programmed under the UNIX platform. The reasons for this are simple. First, UNIX was designed **from the ground up（完全地）** to allow computers to easily communicate with one another. Second, UNIX has always been available for a wide variety of hardware platforms. Additionally, the TCP/IP protocol on which the Web is based was initially designed with the UNIX operating system in mind. 

​	For these reasons, integrating the Web with Visual Basic was very impractical, if not outright impossible. Then recently, with the standardized Windows socket (or Winsock for short) interface, things got a lot easier. The Winsock interface is a layer that resides between the Windows operating system and the TCP/IP protocol. By making API calls to the Winsock interface, the Windows programmer can avoid the complexities of the TCP/IP protocol and instead concentrate on developing services and tools that run over TCP/IP networks. 

​	Built atop the Winsock interface is a large group of tools that abstract the messy details of TCP/IP and the Internet protocols. With these tools, Web programming became a very practical solution to most distributed information programming tasks. Many custom controls and other tools exist that the Visual Basic programmer can use to further remove the application code from the complexities of the TCP/IP protocol. 

​	What will the future hold? One thing that I can guarantee about the future is change. The Internet is still a very **cutting-edge（前言）** and young technology. This means that your work as an Internet programmer will be a “work in progress” for a long time to come. Unlike COBOL programming, Web programming will be a skill that requires frequent reading and training to keep up-to-date. 