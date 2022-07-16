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



## 07-14:

**Using PowerBuilder to Build Cross-Platform Applications**

​	Before you can create an application, you need to identify which platforms the users and developers will have access to. The difficulty in writing a cross-platform application is designing it so that it takes advantage of the different platforms and complies with the standard behavior of the common applications for that environment. 

​	Because your interface should **comply（服从）** with the standards for each environment, you will have to keep these in mind as you build the application. A very simple example is that in Windows, most applications have an Exit menu item under the File menu option. For a Macintosh, there is a Quit menu option under File. These subtle differences must be considered because they will be immediately obvious (and possibly confusing) to the end user. 

​	Because each environment has its own special behavior and coding techniques, you might be tempted to create several different applications and deploy a different version of the same application to each platform. This would defeat the purpose of PowerBuilder’s cross-platform capability. The following sections discuss how to control the fonts used and how to code one application so that it can dynamically **incorporate（包含、合并）** the functionality required for each platform. 



**The Environment Object** 

​	Coding a multiplatform application depends on a PowerBuilder structure that gives you the ability to get information about the platform on which your application is running. The Environment object has variables defined for it. Once an Environment object has been declared, you need to **populate（居住于、充满、输入数据）** the structure with values. This is done using the GetEnvironment() function. GetEnvironment() takes the name of your newly declared Environment object as an argument. The function returns an integer, 1 for success and -1 for failure. Once the function has been successfully called, you will want to evaluate the Environment object’s attributes to determine what processing you want to occur.

​	The next three sections deal with some common situations you might encounter when working in a multiplatform environment. Each section details a script that can be incorporated into a custom class user object for use with all your applications. In these examples, the user object example is implemented with an environment instance variable declared; it is called i_Environment. 



**The Dynamic Library Search Path** 

​	Because one of the complexities of application development on multiple platforms is creating objects that take full advantage of the environment’s functionality and appearance, it is often necessary to create different copies of the same object. As shown in the API user object example, you can use inheritance to assist in building your objects. Unfortunately, this is not always possible. After you have developed your platform-specific objects, you most likely will maintain that platform’s objects in their own library file (in other words, one PBL per platform). 

​	Each library file would be specified in the library search path for your application (for example, common.pbl, windows.pbl, mac.pbl, unix.pbl). PowerBuilder uses the order in the search path to find objects requested by your application. If an object is located in the PBL listed last in the search path, PowerBuilder looks through all the other PBLs before looking in the last one. If you are using platform-specific objects that have the same name as other objects, you will always use the object first found in the library list. Therefore, you would never use any of your platform-specific objects. 

​	This is also fine if you do not use objects in the last PBL very often. If you often do need the objects in the last PBL, your performance will be affected because all library files must be searched first. This would be true for the example if you needed objects from the Mac or UNIX PBLs. Therefore, performance would be fine for those people requiring objects from windows.pbl, but users on different platforms would notice a slight performance degradation. 

​	Most likely you would create a dynamic library (either PBD1 or DLL2 ) for each PBL, and PowerBuilder would maintain the library search path for the dynamic libraries, which would affect the runtime environment as well as development. To **alleviate（减轻）** this problem, you could deploy several different executables, each with a different search path defined. This would not be particularly efficient. A different approach would be to dynamically modify the library search path for your application using the function SetLibraryList() . 

​	To implement this functionality, you could hard-code the dynamic library list into your application, but that would result in a new executable being created if you changed the library list. A better approach would be to create a function in a custom class user object that is instantiated in your application object. The best method of maintaining this list would be to place it in a table in your database and then, based on the user’s environment, read the table and assign the appropriate library order to the application. The idea is that only the table needs to be changed; the code can remain generic. You could also do this by reading in information from an INI file. 



**Menu Modification**

​	One **subtle（不易察觉）** difference between Windows and the Macintosh is that the word for the menu item to leave the application is Exit in Windows and Quit on the Mac. You need to consider the difference in interface design; the code in Listing 5C-1 gives you a base function to work from. The function, wf_SetExitText() 4 , accepts an argument of type m_ancestor, which is the ancestor menu for all menus in your application. 

The code that calls this function should be placed in the window Open event and look something like this: wf_SetExitText(this.menuid) This assumes that the menu associated with the window has been inherited from m_ancestor. 



**Internationalization（国际化）** 

​	In complying with the continually growing need to create an application that can service multiple countries, Powersoft has extended the functionality of PowerBuilder 6.0. These changes include additional support for applications in Arabic and Hebrew, Double Byte Character Set (DBCS1 ), and a Unicode2 version of PowerBuilder. 

​	PowerBuilder will now ship a version using the Double Byte Character Set (DBCS) for Chinese application development. The DBCS supports the Chinese character set, setting it apart from the ANSI3 version of PowerBuilder. The DBCS will also be extended to include Japanese and Korean. 

​	In addition to the DBCS and ANSI versions of PowerBuilder, PowerBuilder 6.0 will be available in a Unicode version (under NT 4.x only). Unicode is being embraced because it surpasses the limitation of ASCII4 to encode only information using the Latin alphabet. Unicode introduces a new character code that gives the ability to encode all characters used for written languages across the world. This is done by using a 16-bit code set versus ASCII, which uses a 7-bit code set. Unicode can, therefore, create codes for 65,000 characters as opposed to 128 characters like ASCII. Each character in the Unicode version is assigned a unique 16-bit character that makes the processing for software much easier to encode. 

​	Applications that are created using the Unicode version of PowerBuilder need to be deployed using the Unicode deployment DLLs on an operating system that is Unicode compliant. The PowerBuilder library files will be saved with the extension .pul for PowerBuilder Unicode Library. 

​	PowerBuilder applications can be migrated from ANSI to Unicode and back. In addition, the PowerScript language also supports two new functions, ToAnsi() and ToUnicode(), to aid in the conversion of characters. 

​	To aid in the process of translating an application from one language to another, Powersoft plans to release a Translation Toolkit that assists you in translating phrases in your application to the necessary languages. Once the translation has been completed using the Toolkit, the application only needs to be compiled and deployed to the appropriate platforms. 



**Summary** 

​	The need for a front-end development that crosses multiple platforms has been answered by PowerBuilder. With support for the Microsoft suite, the Macintosh, and UNIX, PowerBuilder gives developers the ability to use the same product to develop applications that can be run on and take advantage of each platform. With the incorporation of the Environment object, PowerBuilder allows you to modify your application at runtime to access each platform-specific object. 



## **07-15:**

**Distributed Systems**

**INTRODUCTION** 

​	The field of distributed computing has witnessed an explosive expansion during the last decade. As the use of distributed computing systems for large-scale computations is growing, so is the need to increase their reliability. Nevertheless, the probability of failure of an individual processing node in multimode distributed systems is not **negligible（微不足道）**. Hence, it is necessary to develop **mechanisms（机制）** that prevent the waste of computations performed on distributed processing nodes if one of the nodes fails, either due to a hardware transient fault (bus error or segmentation fault) or a permanent fault (power failure or communication network **malfunction（出现故障）**)

​	Advances in communications technology and methods of work introduced at diverse workplace environments naturally led to a greater distribution of information processing. Initially, most distributed systems were **homogeneous（同性质的）**, but now many distributed environments are **heterogeneous（异类的）**. Therefore, the distributed systems design must focus on heterogeneous environments, treating homogeneous systems as special cases in a heterogeneous world. Key issues in distributed systems design include where specific functionality should be located within the information infrastructure. 



**WHAT ARE DISTRIBUTED SYSTEMS?** 

​	A distributed system is a collection of independent computers which appear to the users of the system as a single computer. Nearly all large software systems are by necessity  distributed. For example, enterprise-wide business systems must support multiple users running common applications across different sites. 

​	A distributed system **encompasses（包含）** a variety of applications, their underlying support software, the hardware they run on, and the communication links connecting the distributed hardware. The largest and best-known distributed system is the set of computers, software, and services comprising the World Wide Web, which is so **pervasive（遍布）** that it **coexists（同时存在）** with and connects to most other existing distributed systems. The most common distributed systems are networked client/server systems. Distributed systems share the general properties described below. 

​	**Resource Sharing** 

​		The most common reason for connecting a set of computers into a distributed system is to allow them to share physical and computational resources (printers, files, databases, mail services, stock quotes, and **collaborative（合作的）** applications, for example). Distributed system components that support resource sharing play a similar role as, and are increasingly indistinguishable from, operating systems. 

​	**Multiple Nodes** 

​		Software for the distributed system executes on nodes, or multiple independent computers (not merely multiple processors on the same computer, which is the realm of parallel computing). These nodes can range among personal computers, high-performance workstations, file servers, **mainframes（大型主机）**, and supercomputers. Each can take the role of a client, which requests services by others; a server, which provides computation or resource access to others; or a peer, which does both. A distributed system may be as small as two nodes, provided software connectivity is present. This arrangement is represented in Figure 6A-1. 

​	**Concurrency** 

​		Each of the nodes in a distributed system functions both independently and concurrently with all of the others. More than one process (executing program) per node and more than one thread (concurrently executing task) per process can act as components in a system. Most components are **reactive（响应式的）**, continuously responding to commands from users and messages from other components. Like operating systems, distributed systems are designed to avoid termination and so should always remain at least partially available. 

​	**Heterogeneity** 

​		The nodes participating in a system can consist of diverse computing and communication hardware. The software comprising the system can include diverse programming languages and development tools. Some heterogeneity issues can be addressed with common message formats and low-level protocols that are readily implemented across different platforms (e.g., PCs, servers, and mainframes). Others may require construction of bridges that translate one set of formats and protocols to another. More **thorough（彻底）** system integration can be attained by requiring that all nodes support a common virtual machine that processes platform-independent program instructions. The systems that use the Java programming language follow this approach. 

**Multiple Protocols** 

​	Most distributed message passing differs significantly from the kinds of **invocations（调用）** (such as procedure calls) used within the confines of sequential programs. The most basic form of distributed communication is asynchronous. Similar to letters mailed in a postal system, senders issue messages without relying on receipt of or reply by their recipients. Such basic distributed messages usually take much longer to reach **recipients（收件人）** than do local invocations. They sometimes reach recipients in a different order than they were sent and they may fail to reach them at all. To avoid this, more sophisticated protocols must be constructed. These may include: 

- Procedural messaging, in which senders wait for full replies 
- Semi-synchronous messaging, in which senders wait for an acknowledgment of message receipt before proceeding
- Transactional protocols, in which all messages in a given session or transaction are processed in an all-or-none fashion
- Callback protocols, in which receivers later issue different messages back to their senders 
- Time-out protocols, in which senders only wait for replies for a certain period before proceeding 
- Multicast protocols, in which senders simultaneously issue messages to a group of other nodes These and other protocols are often extended and specialized to enhance reliability, security, and efficiency. 



**Fault Tolerance** 

​	A program running on a single computer is, at best, only as reliable as that computer. Most distributed systems, on the other hand, need to remain at least partially available and functional even if some of their nodes, applications, or communication links fail or **misbehave（mis-行为不端）**. In addition to outright failures, applications may suffer from unacceptably low quality of service due to bandwidth shortages, network contention, software overhead, or other system limitations, so fault-tolerance requirements present some of the most central, yet difficult challenges in the construction of distributed systems. 



**Security** 

​	Only authorized users may access sensitive data or perform critical operations. Security in distributed systems is **intrinsically（本质的）** a multilevel issue, ranging from the basic safety guarantees provided by the hardware and operating systems residing on each node; to message encryption and authentication protocols; to mechanisms supporting issues concerning privacy, appropriateness of content, and individual responsibility. Techniques for addressing **trustworthiness（信用）** include using digital certificates and preventing component code performing potentially dangerous operations such as modifying disk files. 



**Message Passing** 

​	Software on separate computers communicates via structured message-passing disciplines built upon a number of networking protocols (for example, TCP/IP). These, in turn, may run on any of a number of connection technologies (for example, Ethernet and modems). The nodes in most distributed systems are completely connected—any node may send a message to any other node. Delivery is mediated by underlying routing algorithms and related networking support. Messages include commands, requests for services, event notifications, multimedia data, file contents, and even entire programs. **It should be noted that most multiprocessors communicate via shared memory rather than message passing and therefore are not distributed.**



**Openness** 

​	Most sequential programs are considered closed because their configurations never change after execution commences. Most distributed systems are, to some degree, open, because nodes, components, and applications can be added or changed while the system is running. This provides the extensibility necessary to **accommodate（容纳）** expansion, and the ability to evolve and cope with the changing world in which a system resides. Openness requires that each component obey a certain minimal set of policies, conventions, and protocols to ensure interoperability among updated or added components. Historically, the most successful open systems have been those with the most minimal requirements. For example, the simplicity of the Hypertext Transfer Protocol (HTTP ) was a major factor in the success of the World Wide Web. Standards organizations such as International Standards Organization (ISO) and American National Standards Institute (ANSI), along with industrial **consortia（工会）** such as the Object Management Group (OMG2 ), establish the basic format and protocol standards underlying many interoperability guarantees. Individual distributed systems additionally rely on context-specific or domain-dependent policies and mechanisms.



**Isolation** 

​	Each component is logically or physically **autonomous（自治的）**, and it communicates with others only via structured message protocols. In addition, groups of components may be segregated for purposes of functionality, performance, or security. For example, while the connectivity of a corporate distributed system might extend to the entire Internet, its essential functionality could be segregated (often by a firewall) to an intranet operating only within the firewall. It would communicate then with other parts of the system via a restricted secure protocol. 



**Persistence** 

​	At least some data and programs are maintained on persistent media that outlast the execution of a given application. Persistence may be arranged at the level of file systems, database systems, or programming language runtime support mechanisms. 



**Decentralized Control（分散管理）** 

​	No single computer is necessarily responsible for configuration, management, or policy control for the system as a whole. Distributed systems are instead domains joined by protocol of autonomous agents that agree on enough common policies to provide an aggregate functionality. Some aspects of decentralization are desirable, such as fault-tolerance **provisions（规定）**. Others are essential because centralized control cannot accommodate the number of nodes and connections supported by contemporary systems. The tools for administering system-wide policies, however, may be restricted to particular users. 





**ADVANTAGES AND DISADVANTAGES** 

**Advantages of Distributed Systems**

​	Distributed systems have many **inherent（内在）** advantages, especially over centralized systems. Some applications are inherently distributed as well. In general, distributed systems: 

- Yield higher performance 
- Provide higher reliability
-  Allow incremental growth. Distributed computing offers higher rates of return over individual CPUs: 
-  It is both **feasible（可行的）** and easy to construct systems of a large number of CPUs connected by a high-speed network. 
- It answers a need to share data scattered over these CPUs. 
- It provides a way to share expensive peripherals.
-  It allows one user to run a program on many different machines.



**Disadvantages of Distributed Systems** 

​	In spite of their many advantages, distributed systems do create a few disadvantages. Some of these are: 

- The need for new operating systems to support them 
- A reliance on network communications 
- The need for enhanced security 
- Offer no nice classification of operating systems
-  Use loosely and tightly coupled systems 



**CONCLUSIONS** 

​	We want to fully utilize a heterogeneous computing environment where different types of processing resources and interconnection technologies are used effectively and efficiently. Using distributed resources provides the potential of maximizing performance and cost effectiveness for a wide range of scientific and distributed applications. Distributed computing environments comprising networked heterogeneous workstations are becoming the standard configuration in both engineering and scientific environments. However, the lack of a unifying parallel computing model (a parallel equivalent of a von Neumann model) means that the current parallel applications are nonportable. 



## 07-16:

**What Does “Client-Server” Really Mean?**

**Introduction** 

​	As computer professionals, we all must **cope with（处理、应付）** a never-ending stream of new technology. Along with the introduction of each new technology comes a dizzying array of matching terminology. We use (or abuse) the many technical terms to the point that they begin to **take on（具有）** the quality of a “buzzword”, that is, a word or phrase frequently heard but seldom understood. “Client-server” is one term that has **fulfilled（实现、满足）** its potential for becoming an industry buzzword. This is unfortunate; the term “client-server” has a lot of relevance to today’s networks. Part of the difficulty with understanding the term is that it takes on different meanings or **connotations（内涵）**, depending upon who is doing the defining. In a very general sense, the term client-server really **denotes（表现）** a type of relationship between entities. The entities we will discuss, of course, are software applications running on networked computer systems. There are many such types of possible relationships (such as a hierarchy) between multiple entities, but we will only examine two here: “peer-to-peer” and “client-server”. Let’s take a short look at one of those relationships, “peer-to-peer”, that will help us when we look more closely at a client-server relationship. 



**Examining a “Peer-to-Peer” Relationship** 

​	In a peer-to-peer relationship, all entities have equal **standing（长久的、地位）** with one another, and all are equally capable of running the same set of services. In many ways, this relationship is the easiest type to recognize, configure, and manage. This does not mean that it is necessarily the most efficient or cost-effective way of allocating computer resources. 

​	In peer-to-peer configuration, all of the individual systems are configured (more or less) alike. They have relatively equal amounts of resources (e.g., disk, memory, and CPU power), and all resources are equally shared among the various systems in the group. Each machine is completely capable of performing any task that a particular user may desire, without the involvement of, or reliance on, another system’s resources. 

​	Figure 6B-1 depicts a network of computer systems configured in a peer-to-peer manner. Every computer has the same hardware resources—disk, RAM, and CPU—as well as the same software configuration in terms of operating system and applications. Because the machines are all similarly configured, a user who is running a word-processing application uses far less of the local resources than a user that might be doing a **thermal（热的）** analysis of a circuit board. In the first case, there are very probably **underutilized（未充分使用）** resources, such as RAM, CPU cycles, or hardware graphics acceleration. In the second case, the local resources are more likely to be fully utilized, possibly even overutilized. 

​	Underutilization of resources is common in a peer-to-peer network where there are multiple applications types being used. The underutilization of resources on some systems, along with full or overutilization on others can mean that some users are not able to get their tasks completed in the **optimum(最优化)** amount of time, while others may have no difficulties. Here is an example of how **misallocation（错误分配）** of resources in a networked environment can actually cost money. 



**The Client-Server Relationship：**

​	In a client-server relationship, there are at least two types of logical entities involved: the client entity and the server entity. It is important to note at this point that the term client-server may be applied either to hardware (computer system) or to software (applications) running on the hardware. This is one potential point of confusion, as the hardware may be configured differently to run the client software or the server software, but does not necessarily have to be.

​	In the case of software entities, it is possible that both client and server may exist on the same computer system or be split across multiple systems in the network. How the actual tasks that an application performs are split between the client and the server entities will vary, usually determined by the application’s designer.  

​	Unlike the peer-to-peer environment, the client-server relationship is not one of equal capability between client and server entities. The server entity “possesses” and manages a well-defined set of resources on behalf of its client or clients. The client-server model may also be characterized as a “request-response” interaction. To use the resource, the clients must make requests to the server entity. The server responds to, services, or “serves” its client’s requests for the resource that it manages. Since the client-server relationship is a logical one, nothing prevents both the client and the server components of an application from running on the same underlying hardware. 

​	Figure 6B-2 shows an environment that has resources unequally distributed between client and server machines. You can think of the system resources as being water in a set of buckets associated with each system; in this example there are buckets for RAM, CPU cycles, and disk storage. Resources are moved from the client system’s buckets and reapportioned to the resource bucket belonging to a server or group of servers in the network. 

​	In this type of environment, there are usually N clients to each server, with the server providing all of the services associated with its resource to multiple clients. The client-server relationship may be thought of as a many-to-one relationship. The number of clients that a server can handle depends on several factors, including the type of resource being managed, the number of total simultaneous requests, and the request frequency from each client. 

​	One of the defining characteristics of today’s client-server applications is the presence of a network connection between the client and the server, so another important performance factor is the type of connection between the client and the server and its relative “health”. Obviously a poor network connection can influence clients and servers communicating across the network.



**Client-Server Application Configurations and Components** 

​	Within the term client-server, there are many possible application configurations. The configuration of a client-server architecture is determined by where the associated application is broken into separate components. At the most basic level, the application may be split into several different components: the graphical user interface (**presentation（展示）** logic), application logic, and data management logic. 

​	It is possible to insert distribution services between any, all, or none of the three basic components. In the latter case, you end up with the familiar “**monolithic（整体的、巨大、单片）**” application configuration, running on a single system. With distribution services inserted, the result is a client-server application. This is diagrammed in Figure 6B-3. 

​	Sometimes identifying a client-server relationship is difficult because the system being studied is a **hybrid（混合）** design. Under these circumstances, there may be multiple levels of client-server relationships, or a single level where one client may in turn be a server to other clients. There are some commonly encountered client-server configurations which involve more complicated physical distributions of the application components and some more complicated interactions between those components. Some examples are shown in Figure 6B-4. 

​	Combinations involving other relationship models are possible, based on the whims of the application designers. For these reasons, and others, there may not be a clean distinction in hybrid system designs or systems that are in transition between the client-server model and other configurations. We will try to stick to the clearly identifiable cases, and you should avoid designing such complicated relationships if at all possible.  



**Client-Server Distribution Services** 

​	While describing the client-server application architecture, we did not venture beyond the conceptual description of the application being split into components and “glued” together with “distribution services”. Examining the available distribution services in an environment is an important aspect of both good design and analysis. If the necessary services are not available or reliable, client-server applications may quite literally **fall apart（破碎）** . 

​	The term “distribution services” is a very general label. The services used to allow distribution of client-server application components include: remote procedure call **facilities（设施）** (RPC 1 ), directory services, system management services, performance measurement services, load balancing, and a whole host of other potential components. These services may be distributed across multiple systems or reside on a single server. When designing an environment, it is easier to separate the services as if they were running on their own computer systems, only collapsing the relationships between services and the physical server system when the final hardware configuration is determined. 

​	Our **schematic（示意图）** view of the client-server world, then, is the client logic communicating with servers providing data access, transaction processing, and compute power. Interaction between the client and the rest of the environment takes place through some form of communication facility. A set of infrastructure services provides the glue to hold the application architecture together. 

​	A transaction processing function or database server may, in some cases, differentiate a “commercial” client-server application from a “technical” client-server application. The transaction facility may be viewed as providing the business logic necessary to properly direct client behavior, according to a predefined set of rules used to model data flow in a business. In most technical applications, this particular service is usually absent or may be viewed as part of the data service. 

​	The infrastructure services are common functionality needed by all client-server applications and their users for proper operation. Time synchronization between computers systems, software licensing, electronic mail, directory services, user authentication and access (security), software distribution, and especially environmental management are all examples of services needed by almost every application in the client-server environment. Determining what these common services are and ensuring their availability is an important part of the design or assessment of a client-server environment. 



**How Do I Recognize a Client-Server Relationship?** 

​	For those of us that are used to other relationship models, the client-server model and its many **permutations（排列）** may seem strange at first. The natural tendency is to configure everything in peer-to-peer mode, which is easier to grasp conceptually. This is also the way that environments tend to evolve, starting with one machine, adding another, and another, and so on. We may ask, “Just how do I recognize a client-server environment when I see one?” This can be easier than it first seems. When **confronted（面对、面临）** by something that purports to use a client-server model, start by asking the following questions: 

- What is the resource that is being managed? 
-  Who is doing the resource management? 
- Who is using the resource? 



​	With the answers to these questions in hand, try drawing a picture that represents the relationships among the entities being examined. You should see: 

- A clear logical or physical division between the manager and the users of the resource (the server and the clients) 
- Usually, one server to multiple clients 
- A clear division of “intelligence” or “responsibility” with regard to managing the resource, with the client being the least capable of the two entities 

​	For simplicity, we have only considered a single client to single server relationship up to this point. Figure 6C-1 shows a slightly more complicated situation. 

​	The X-windows system, used by Unix and other operating systems to provide remote graphical display capabilities, is a good example of a client-server relationship that takes a little analysis to understand. Users that are new to the X-windows system frequently ask, “Aren’t the programs that are using the X-windows display actually the servers, since they are acting on behalf of the user?” 

​	At first glance, it appears that the client and the server entities are reversed. After identifying the resources being managed, the picture makes a little more sense. It is the user’s graphics display and input devices that are being managed by the X-windows server on behalf of the X-windows clients that are using them. So, with regard to the X-windows services, the programs are indeed clients to the X-windows server and not vice versa. 

​	Note also that the X-windows server itself makes use of the X-windows font server. So, as shown in Figure 6C-1, there are multiple client-server relationships at work. The X-windows clients are using resources “served” by the X-windows server, and the X-windows server is using resources that are “served” by the X-windows font server. 

​	There is another important point to be made here. Because of the flexibility inherent in the example, a **resourceful（足智多谋的）** system administrator is free to move the components to the physical system in the network that best suits the needs. The X-windows font server and the X-windows client are free to run on any physical machine, but the X-windows server is tied to the physical resource, the graphics display, that it is managing. 



**What Is Important About the Client-Server Model?** 

​	**So far（到目前为止）**, we have talked about what the client-server model is, shown conceptual models of the supporting environment, and discussed how to identify some client-server characteristics in a system. But why is the client-server model important? Why does a large portion of the industry focus on this particular way of designing applications? There are several very good reasons to consider client-server design in your computer environment: 

- The per seat cost of a computerized solution may be lower with the client-server model. 
- Specialized hardware may be used to provide resource-intensive services, improving client performance.
- General-purpose hardware may be specifically **tuned to（调优）** perform the specialized service, improving client performance. 
- Measuring (and therefore managing) the usage of a service may be easier if it is localized to specific places in the environment. 
- The clients may be insulated from changes in the server environment. 
- The client-server model provides better **scaling（可伸缩）** than other usage models. 

​	Remember that in a peer-to-peer relationship every system is equally capable of providing a particular service. For optimal performance, this implies that all systems should be configured with the same hardware and software resources. This can lead to overconfiguration of resources in areas like Random Access Memory (RAM), disk space, CPU power, I/O capability, and system expandability. Due to the overconfiguration, each system may cost more than it should, especially if the local resources are underutilized. By designing the environment so that the clients use services provided by suitably configured servers, the server resources may be better utilized and the clients need not be so heavily configured. 

​	Whenever a server must provide access to a specialized resource, there are two common ways to approach the situation: choose a specialized machine type, if the need **warrants（证明）** it, or choose a general-purpose machine that is capable of providing the service if properly tuned. The specialized computer usually provides a unique service, or provides it in a way that no other machine can, often at an extra cost. A general-purpose computer can be moved from place to place and retuned to meet the new service needs. 

​	Providing the proper level of performance to clients of a particular service and measuring the level of that performance can be a challenge. This is especially true if the resources are **scattered（分散）** all over the network as in the peer-to-peer model. With the client-server model, if you know that a particular machine provides only one type of service to its clients, it is far easier to measure the total resource utilization and, therefore, the machine’s ability to provide the service. If more access to the resource being served is required, then the machine may be upgraded or, if possible, additional servers added.

​	Under the client-server model, it is possible to insulate a client from implicit knowledge of where the requested service is located in the network. This is desirable for a number of reasons, but the most important is: if a client cares only that the service is provided, not where it is provided, then the client can be insulated from changes in the service environment. For example, in a client-server environment designed with this rule in mind, if a system manager noticed that additional capacity was necessary for a given service, he would only need to plug another server into the network to provide the additional capacity. Furthermore, if the need for additional capacity was a temporary situation, when the extra capacity was no longer needed the server could be removed without impacting clients of the service.



**Client-Server Model Summary** 

​	In summary, the term “client-server” defines a specific type of relationship between two, or possibly more, logical entities. These entities are usually software in nature and may co-exist on the same computer system hardware or be separated by a network connection. The server-to-client ratio is one to many, as opposed to one-to-one as in a peer-to-peer relationship. There usually is a **disparity（明显差异）** in capability between the client and server entity, with the client requesting use of a resource from the server, which manages the desired resource. 

​	Client-server applications consist of individual components with distribution services inserted between them. Common client-server application components are the presentation logic, the application logic, and the data management logic. While this model is useful in the initial understanding of client-server principles, real-life applications tend to be more complicated and require more analysis to understand the roles that each component plays in the whole. 

​	There are multiple “styles” of client-server applications. The style of client-server application depends on where the application designers inserted distribution services into the application logic. There are advantages and disadvantages to each of the commonly encountered client-server application styles. Finally, there is a basic choice to be made between using general-purpose and special-purpose computer systems to run server software. 

