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