## 05-23:

今儿想Google下有Java的基础下，如何去学习Go,下面这个好像也没说啥，就当简单的阅读。

https://dev.to/rubyshiv/how-to-get-started-with-golang-as-a-java-developer-1icd

**How to Get Started with GoLang as a Java Developer**


​	For quite some time, I have wanted to learn GO. The programs that I used to read, appeared to be simple enough to understand.

​	As Java developers, we are quite used to lengthy syntaxes. We don’t forget the “;” and our file name and public classes have the same name. We also take care of the visibility and access modifiers even for a simple Hello World program.

​	I just started learning GO and find it much **relatable(有关系的)** to Java in terms of the package and import declaration and the method /function syntax. With no classes to define and semicolons to add, I find GO much quicker to develop, at least for a simple application like “Hello World”.

​	Let’s try to implement a simple Hello World program in GO using a text editor and a Code Editor.



**Step 1: First things first, let’s download and install Go on our local machine.**

​	 Installation steps for all the different OS’s are given in the official guide at https://go.dev/doc/install. I have installed the below-given version of golang, (use go version command to check that)

​	

**Step 2: Create the project structure**

​	A GO project must have 3 directories — bin, pkg, and src. Under the src folder, we will create our application folders and files.

bin folder stores all the binaries generated from the application and the downloaded dependencies. pkg is an **intermediate（中间产物）** folder that holds the compiled objects from src directory.



**Step 3: Create project folder under src**

​	All the code that’s part of our application will go under the src folder. Let’s create a folder under the src directory which will follow the naming **conventions（会议、惯例）** similar to the one we use in java applications — com/something/something.

​	In this article we are just creating a single package under the src package and named it main, it could be any other name as well. Create a file with *.go extension. The first thing in a go file must be the package declaration, followed by the imports under two simple brackets “(“ and “)”. Next, write the “main()” function that would use the fmt package to call “Println” function. “main()” function must be declared in the main package else the compiler would complain. Here’s the complete code to this hello world program



**Step 4 (Optional): Use a Code Editor**

​	I’m quite used to using STS and Eclipse for Java programming so at first, I tried to install the go plugin to STS and create a Hello World program. My experience with Go on STS/ Eclipse was really bad, now it could be because I don't know how to configure a Go project correctly on that IDE but overall the experience was not good and the error messages didn’t make it easy to figure out the root cause. So I did some research on the best tools to use with Go. Turns out there are more code editors than IDE as such and the best IDE is GoLand by JetBrains, the same folks who developed IntelliJ. A few of the popular code editors are vim, govim, and VS Code. I have never tried VS Code before and always wanted to try it so I decided to try VS Code for GO programming.

​	Firstly, I installed the go plugin for VS Code,Go Extension for VS CodeThen wrote the same program shared in Step 3, using the Terminal tab in VS Code, executed the GO program.



**Conclusion**
	I like the fact that GO is a simple language, especially coming from a Java background.**A hello world is not even the tip of the iceberg but it’s a start.** While learning human languages we tend to compare the new language to the one we already know, it makes learning easier through **comparison(比较)**. I’m trying to follow the same approach to see how to program the specific actions that I usually carry out using Java in GO.





## 05-24:

**Have you ever broken up with someone over a single character flaw?**
	Not me, but my bestfriend. We’ve known each other for 12 years, she’s probably the most beautiful, intelligent girl I’ve ever met, but somehow her love life is always **kinda(有点)** rough.

​	So she met this guy through a friend 2 years ago, **senior（大四）** year in college. She got an intern job in a huge company, while studying. She’s under a lot pressure, and this guy didn’t even show a little bit empathy, all he said to her was: ”quit your job, move to my hometown; we’ll live together with my mom and be a housewife.” They’ve only been dating for 2 months and that’s all he said. At first she thought he’s joking, but he said it to her over and over, he told my friend that’s his “big plan” for their future; he really meant it.

​	I know a lot girls want to be a house wife, to be taking care of their family 24/7, I respect that completely, but that should be based on your own will and with an equal and respectful partner. That **dude（家伙）** just took it for granted, he just naturally assumed every girl’s dream is to be married, have kids, do all the house work, so he can be “the man”. Since he didn’t show respect at all and wouldn’t shut up, my friend quickly broke with him, he didn’t even understand why and called her selfish. What a **jerk（急推、粗蠢）**.

​	2 years later, my friend has graduated with straight A grades, some savings, and last months she got an unconditional offer from The University of Sydney; she will be a graduated student next year March. I’m so proud of her.



## 05-25:

**Programmers, what's the funniest outsider's view of your job you've ever heard?**
	Many moons ago my ex wife was in the room while I was working on developing some new capability of a C++ application.I had many browser windows open with various sites displayed showing sample code, documentation, other people’s approaches etc. She **gasped（喘气）** and said, “Dan, what are you doing?”. I was **confused（迷惑）** and told her I was working on some new functionality. “But aren’t you cheating?” she asked, **wide eyed（吃惊）**. “Eh?” was my even more confused response. “You’re looking at those websites, shouldn’t you **figure（理解、想象）** it out yourself?” My **jaw dropped（目瞪口呆）.** I mean where do you begin? She’s a smart woman but at that point in her life the idea of **leveraging（杠杆）** other people’s work in such a way was **foreign（外国的、陌生的）**. “Well, it’s documentation, some people have done it certain ways and many people share those ways and that way everyone wins… in a way… like it’s just the way it’s done.” “Hmmmhmmm… cheating” she said.



**What is one thing non coders don't understand about coding?**
	You’ll never be able to fully explain the true value of **concentration(专注)**. If you write code at home, or in a “noisy” office, prepare to be interrupted by people who may be well-meaning, but simply cannot **appreciate（感激、明白）** what the “big deal” is when they interrupt you…

下面是张有趣的图：

![img](week_22.assets/main-qimg-c44ba52da778811f9a30e9b21f073f04-pjlq.jpeg)





## **05-26:**

**Why does C++ turn out to be a nightmare for beginner programmers?**

​	Here’s a big surprise; people whose favorite language is not C++ think C++ is a terrible language.

​	I want to summarize some of the complaints about C++ in this thread and respond from the viewpoint of a person **comfortable（熟悉）** with C++. But first let me say a word about why people like to use C++. C++ produces fast code, for situations where fast code is important. If you don’t need to go fast, try python. It’s great. It has a zillion libraries to do the hard stuff. And guess what, those libraries are written in C++. Doh! C++ lets you have performance when you need it, and fancy error checking when you want it. You don’t get that in other languages.

Borland C++ in the 1980s was harder to begin using than interpreted BASIC.
	Well duh! And how many people are writing commercial applications today in interpreted BASIC? It’s 2021 now, and In 2021 you can use any of several on-line C++ compilers to learn C++. It’s actually almost as simple as interpreted BASIC. No code to install, no IDE to learn, just type it into the browser, and when the last syntax error is fixed, it runs automatically. Brilliant.



C++ has **cryptic（神秘）** compile-time error messages.
	This is true if you are doing something advanced like partial template instantiation. Unfortunately, this makes it true sometimes when you are instantiating one of the standard container classes or algorithms. Perhaps you would feel like C++ was a better language if it didn’t come with standard algorithms and containers. You’d like C then. Or FORTRAN.
The error messages produced for most C++ errors are as readable as those for Java or C#. Is that a recommendation? I can’t say.



C++ doesn’t produce good run-time error messages.
	Really? Depends on whether you ask it to or not. Yes, if you want the best speed, you might use raw arrays, and you get undefined behavior if you index an item outside the declared bounds of the array. But you can also use std::vector and the at() member function and get terrific error messages at some extra run-time cost. Java only gives you the choice to go slow.



C++ isn’t mainstream anymore like Java and C# are.

​	Really? The TIOBE index of the top 20 most popular programming languages puts C++ in fourth place, right between Java and C#.



C++ has added a lot of features in the last 10 years.
	This is either a strength of a weakness depending as you want better solutions to your performance problems or well-remembered workarounds to weak old features. Even as a fan of C++, **the last 10 years has been a roller-coaster of new things to learn.** On balance though, I can’t think of a new feature I’d want to live without once I got used to using it. Java and C# have also evolved significantly in the last 10 years.



Managing memory is hard!
	True, but garbage collection is s. l. o. w. If slow doesn’t matter, I’d suggest using another language, like python maybe.



C++ requires a lot of boilerplate.
	That’s only true if the defaults don’t work for you. In java, it just sucks for you if the defaults don’t work, because there is not another option. Once again, C++ offers a **tradeoff（权衡）** between fast and easy that other languages don’t provide.



C++ has pointers, which are **icky（讨厌的）**.
	This is the one complaint that seems to have any validity to me. If I were designing a language today, I wouldn’t put pointers in. But C++ was designed by your grandparents, when the compiler and the operating system had to fit into 128Kbytes. Pointers let dumb compilers produce smart code. Now C++ is stuck with ‘em. They’re not that hard.



C++ has different syntax than FORTRAN…so it’s confusing for a beginner who just learned FORTRAN.
	Wow. Just wow.





## 05-27

**The butterflies we may never see again in Britain**


​	If you want to catch sight of many of Britain's butterflies, you'll need to be quick. A report by Butterfly **Conservation（保护）** warns that 24 of 58 species may soon disappear from our shores.Five more species are threatened with dying out than when the **charity（慈善机构）** last compiled a Red List, 11 years ago. Humans are driving the loss of butterflies by destroying wildlife rich habitats, says Head of Science for Butterfly Conservation Dr Richard Fox. "They've literally been destroyed, been **ploughed up（翻耕）**, covered in fertilisers and used to grow crops or for housing," he told BBC News. But there is some hope. Several species have been brought back from the **brink（边缘）** by intense conservation work. Here are the butterflies we may never see again in Britain - and three that have been saved.



**Wood White**
	This small, slow-flying butterfly used to live across most of southern England and Wales. Now endangered, it's mostly found in the Midlands.

![Wood White](week_22.assets/_124911965_gettyimages-639240536.jpg)



**Swallowtails**
	This spectacular rare butterfly has become more at risk since 2011. It's native to the Norfolk Broads where it feeds on flowers including thistles.



**Adonis Blues**
	Now re-categorised as more threatened, this creature lives in southern England and is usually seen in April and late July. In areas where the Adonis Blues thrives, it can be seen in the hundreds.

![Adonis Blues](week_22.assets/_124913525_adonisblue-male_vulnerable_iainhleach.jpg)



**Large Heath**
	This is one of the butterflies affected by climate change, says Butterfly Conservation. All four of the UK's butterfly species that prefer to live in northerly areas, with cooler and **damper（风门、阻尼器、潮湿）** climates, are endangered.



**Scotch Argus**
	The effects of climate change are also visible with the decline of this species. In 2011, scientists didn't consider it under threat. Now it's listed as **vulnerable（脆落的）**.



**The butterflies we have saved**
	Now, some good news. Conservation work has helped bring back some species from the brink.It has focussed on protecting butterflies from the effects of changing land management and climate change, explains Dr Fox.



**Large Blue**
	This dusky-blue butterfly was extinct in Britain in 1979, but it can now be spotted fluttering its wings largely in Somerset. Described as "**fussy（爱挑剔）**" by Dr Fox, the Large Blue needs to feed on the **thyme（百里香）** plant and a specific type of ant. By creating grasslands with the right conditions, conservationists and landowners successfully created thriving colonies of the butterflies.



**Pearl-bordered Fritillary**
	This has become less threatened since 2011. Its caterpillars need an open and warm woodland habitat so they can bask in sunshine and feed on violets. Conservationists have been clearing areas of woodland for the butterfly to live in, mostly on the edges of Dartmoor.



**Duke of Burgundy**
	Now found mostly in southern England, this butterfly's **caterpillar（毛毛虫）** feeds on cowslips and primroses. Conservationists have worked hard to create the right balance of **vegetation（植物）** so it can thrive.





## 05-28:

**What is one ridiculous reason for which you got kicked out of class?**
	“I want everyone to write down ONE WORD - just one - that describes what they personally think of that poem.” The teacher starts **handing out(分发)** sticky notes.

​	“Write down your word,” she says. “Then stick it on the board.” 

​	“Miss?” I raise my hand. “Is any word okay?”

​	“Any word **as long as（只要）** it’s an honest reflection of what you thought of the poem.”

​	“Are you sure?” I say. “Nothing’s off limits?”

​	“Write whatever you want,” she says.

​	I really hated the poem.I was surprised that I was allowed to write anything but I was also happy I’d get to write down the word on my mind. I wrote: SHIT And stuck it on the board amongst all the other words: “pretty”, “inspirational”, “thought-provoking.”

​	The teacher saw it immediately.

​	“GET OUT! GET OUT GET OUT GET OUT! NOWWWWW!!!!!”

​	“But, Miss, you said I could write —”

​	“OUT!!!!!!”

​	Later that day in the Headmaster’s office… “Sounds like a valid response to a poem.” He shrugged. “If you thought it was shit, what’s wrong with saying it’s shit?”





## 05-29:

**What is a good application?**

​	I recently applied for a position at my current corporation and one of the questions I was asked was “what is a good application?” .I never thought of it before. Therefore, it was a really good exercise to formalize my own vision of a good software application. It was a technical position so my answer was from a developer point of view. Since the time I gave my answer, I have thought about it again and here is my vision of a good application.

 

**A simple application**

​	When I design applications, I always think « **the simpler, the better** ». Developers should only focus on the requirements and just the requirements. 

​	I really hate: 

- over-design (with over use of design patterns)

- over-optimization

- over-development“flexible” architectures

  

​	Nothing beats something simple than can easily be mastered. Most of the time, the over-complex architectures designed for potential future needs will never be used at 100% (or even 50%) because:

- the needs have changed,
- the expectations were too high and/or too far away (who can predict what will happen in 5 years?) ,
- the budget of the project has decreased a lot,
- the corporate strategy has changed.

​	That’s why I prefer something simple that will require a big refactoring if the architecture is not enough for the future requirements.

​	For example, why would you need a Big Data cluster for an application that has just started and therefore deals with very little data? As a Big Data developer, most candidates I have interviewed were working on Big Data projects dealing with a (very) few millions of data. When I asked them why they were using Big Data, some told me “because there are a lot of data” and others “because in the future the application could deal with more data”.  A few years ago, I was working on a large bank and we were dealing with hundreds of millions of data with “only” relational databases. Between a mastered relational database and a buggy Hadoop cluster (buggy because of the little knowledge of people, the complexity of a distributed platform, and the evolving technology itself) the choice is simple. For example, Criteo (a retargeting ads startup) started with a Microsoft SQL server. They only switched to Hadoop during summer 2011 and they now have the biggest Hadoop cluster in Europe.

​	For me, more complex means:

- more expensive (because it’s more difficult to understand and therefore it takes more time)
- more bugs (again, because it’s more difficult to understand and therefore to test)
- more difficult to monitor (again, because it’s more difficult to understand)

​	Of course, if the future needs are 100% sure (for example, when designing the future referential of a very big corporation which will be fully used in 3 years), designing a complex architecture is worth it.

 

**A readable code**

​	A key of a good application is a readable code. Since an application will be written and read by many developers, it’s important that they don’t spend too much time understanding **legacy（遗产）** code.

​	In object programming, this means having a code with short functions (with little cyclomatic complexity) and classes with few responsibilities. I’m a big fan of loose coupling which increases the isolation of the components and therefore helps to share the work among developers.

​	Another key point is the code coherency. On big projects, hundreds of developers modify the source code. If anyone codes as he likes, the code quickly becomes a total nightmare with many styles of codes. It’s like reading a book written sometimes in English, sometimes in French, sometimes in German, sometimes in Russian … The development team must converge to a unique code **convention（习俗）** and the code must be owned by anyone. I really like self-explained code: instead of writing tones of comments, using explicit names for functions, classes and variables is most of the time enough. Of course, it’s still necessary to write documentation (I prefer to directly write it in the class and the function).

​	One of the best examples I have read is the Spring Framework: it has more than a million lines of code but the few parts I read (on Spring Core, Spring Batch and Spring Data) where coherent and the naming conventions were very comprehensive (but some people don’t like the verbosity of the code conventions used by Spring). Moreover, the Spring documentation is awesome. One bad example is a very famous C library: libavcodec. This library is used by most applications to deal with compression, decompression and on the fly transcoding of audio and video streams. The work done by this library is very impressive but, when you’re a beginner and try to understand it, it’s a total nightmare. I spent approximately 15 hours to understand some parts of it in order to make an audio streaming server on my free time but I dropped it: there was not enough documentation and the code conventions were not explicit enough (for me) to be quickly understood without documentation.

 

**A tested code**

​	When I started working, a coworker told me about unit and integration tests and I was thinking “man, why would I need tests, most of the time my code works at the first time”. To be honest, a part of me still thinks the same … But my vision has changed a lot.

​	When I code I always think: “is it unit testable?”.  It’s a very good exercise because it forces me to always (when I have enough time) apply loose coupling. Moreover, having integration and acceptance tests allows you to refractor code and modify someone else’s code without the fear of modifying the behavior of the application.

​	But ok, let’s say you have unit tests, integration and acceptance tests with a very good code coverage and on top of that the tests are automated (with Jenkins for instance).  But are the tests relevant? I’ll give you two bad (and real) examples:

​	In a previous project, people where faking most of the tests just to increase the code coverage so that it looks like a very good project. They didn’t have the time to write real tests and having high code coverage was mandatory.
In another project, I made an audit of someone else’s code and saw that the guy was not testing the behavior of the code but the behavior of the mocks used in its tests.In both scenarios the code coverage was high but the application wasn’t really tested.

​	Relevant tests are only possible if the development team really understands the client’s needs and the concepts behind testing. Of course, it also requires having enough time.

 

**An exploitable application**

​	So great, you have a good application, but: Is it working well? Will it still be the case in 3 months? Are you being hacked? Have you been hacked? Are you sure? In order to answer you need to be able to monitor your application.

​	To do so, you must have a good logging system with different levels of loging so that you can “switch” your production application in a more verbose mode if you really don’t understand a bug.

​	Moreover, you need to log what matters when a problem happens. I’ve dealt many times with crashes in production and sometimes the only thing I got was “ERROR”. Great, but what caused this error? What were the variables and the use case just before this crash? I had hard times understanding some root causes (and it made me want to kill the developer who made this piece of ####)

​	Another aspect is to write technical and functional indicators to monitor the application behavior. For instance the memory usage, the number of current process, the number of customers/contracts/whatever created on daily basis… These indicators might help you to detect an abnormal behavior. Maybe the memory and CPU are overused because you’re being hacked. Maybe there are too many customers created since the last installation because you have a new bug that duplicates creations. Here is an example of a bad exploitable application: On a previous project (on a big corporation), we discovered we were being hacked after 2 weeks of hacking just because the hackers became too greedy and our clustered servers collapsed under the load. With a good monitoring system, we could have detected the intrusion much faster.

​	All these logs and indicators needs to be stored somewhere. Again I like simple things. For a simple application, using just flat-files is enough. But, if your application has many servers, using a centralized logging solution is useful (like logstash/kibana/elastic search). I worked on a project with more than 30 servers in production and no centralized system, let me tell you that reading each log to see if everything is ok was a huge waste of time.

 

**Customer satisfaction：**

​	**I’ve seen many developers who were only driven by technologies**.  But an application is not about technologies, it’s about answering the needs of a client.

​	I love technologies (especially the new and shiny ones), but sometimes I choose an “old” technology I don’t like because it fits exactly the client’s needs.

​	Moreover, most of the time knowing the specificities of a language is useless but understanding the business domain you’re working on is useful. I have never understood developers who don’t care about the business domains and only care about technologies (often only a few technologies). For example, on a project in a bank (the project dealing with hundreds of millions of data) that dealt with Basel II norms (which are European norms created to avoid bank bankruptcy), many developers in this project had never read an article about Basel II nor had tried to understand the basics of these norms. They could have worked on a nuclear plant or web crawler it would have been the same: they were only implementing what they were asked without understanding the use of their developments (even a little bit).

​	For me this point is the most important. Even if your code is a total nightmare, if what you deliver makes the client happy, that what matters. And to do that, you need to understand the business domain of the client. Customer satisfaction should always be the top priority.

 

A few words

​	You’ve just read my vision of a good application which is very close to the AGILE philosophy. I didn’t spoke about ergonomics or usability because there are many types of applications (user-interfaces, batches, web-services …).It’s a very subjective and therefore controversial subject. So, what do YOU think is a good application?

