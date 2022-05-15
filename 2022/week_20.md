## 05-09

**What do programmers and software engineers do once they are more than 50 years old?**
	The ones I know keep working as software developers.I don’t know where the idea comes from that software developers retire early. They basically don’t compared to many/most professions.Software developers rarely make the kind of money to retire early (like bankers might). Software development isn’t a physically demanding job like a police officer, or **tradesman（临售商）**, or maybe a nurse, so we don’t have to retire for that reason.

​	It’s really a fiction that software developers don’t work past 50, and I’ve no idea where it comes from.

​	I think the question is rooted in the assumption of **ageism（年龄偏见主义）** where “old” (50+) software engineers aren’t able to work because they aren’t able to **keep up with the times** and all these new grads can code circles around them.


​	And where does the idea that this is the only profession you get worse at the more experience you have? Nobody thinks “That lawyer is 51, he’s well past it!”.



## 05-10

**Why, when parents argue in front of a young child, does the child seem to favor（喜欢偏向） the aggressor（侵略者，攻击者）? I have seen this happen so many times where the child gravitates（吸引） toward the one doing all the yelling and screaming and can't fathom why.**

1964 I'm 8, my brothers are 6 and 10. After some hours of the the usual screaming and abuse, he comes and gets us all out of bed, lines us up on the couch, and says, “Who do you love best, your mother or me?” I can still see my mother **hovering（hover徘徊）** in the background.One by one, we betray her, telling him we love him best. And the lie worked. It got us back to the relative safety of our beds.We “sided" with him because we were terrified of him.



## 05-11

​	So lately, my 13-year-old son had been **acting a little... entitled（自命不凡）**. Acting like he's too good to shop at Wal-Mart or making **snarky（尖刻的）** comments about kids at school who shop at the goodwill and quite a few other things. I don't tolerate that. Today, he took his own 20.00 to the goodwill to buy clothes to wear the entire week to school. Whatever he found is what he would have to wear. He isn't happy and shed a few tears, but I firmly believe in 15 years, he will look back and laugh at the day his Mom made him shop at goodwill. I want to teach my kids that **money isn't everything,** and if you have to degrade other people because of where they shop, you too will shop there. Side note, I love the goodwill!!



## 05-12

​	**Can someone from a very poor family in African countries become a highly skilled expert in some fields of computer science with only the help of a laptop and internet resources?**

​	Yes. Not only African but everyone who is interested with computer science.

​	Hello,**To be honest**, most of this field doesn't need anything more! I started just like you, a very old laptop and only the internet, now I teach programming and create programming technologies.**Just believe and start i**t, it's not that hard. happy coding!

​	Even people out of Africa, don’t think they have a lot more than just a laptop and internet resources to learn the subject lol. **It’s all depends on how interested one is on the subject**. You can also imagine that not many had the opportunity of a laptop and internet resources just few decades ago, but nonetheless, they still found ways to learn the materials as best as they could. Don’t let the internet play you, learning CS doesn’t depend on your geographical location on earth. If you’re passionate and discipline enough, even if you was located in mars and you had internet and laptop in your possession, I’m sure you’d find a way to make it work. :)



## 05-13:

**As a senior(高级) programmer, what makes you mad（生气抓狂） when you look at a junior（初级） developers code?**
		Very few things make me mad, a Junior is a beginner, it’s the job of more senior developers to help them *become* good developers.That said..There *are* some things that annoy me.                                                                                                                      

- If we’re in round 4 of code review and you’re still not following the coding standards I told you about, I’m going to start losing my patience.
- If you don’t care about your work / Don’t care about improving
- Ignore advice after it’s been proven right (Or ignore people who are continually proven right)
- Use l33tsp34k in your commits/comments 
- Use variable names like “bla”/”somethingsomething”/”xyz” after being told not to (And been told why it’s bad)

While some people just aren’t cut out to be programmers, if you just follow one simple rule you’ll do ok: **Take pride in your work**



**What are the differences between a [`HashMap`](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/HashMap.html) and a [`Hashtable`](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/Hashtable.html) in Java? Which is more efficient for non-threaded applications?**

There are several differences between [`HashMap`](http://java.sun.com/javase/7/docs/api/java/util/HashMap.html) and [`Hashtable`](http://java.sun.com/javase/7/docs/api/java/util/Hashtable.html) in Java:

1. `Hashtable` is [synchronized](https://stackoverflow.com/questions/1085709/what-does-synchronized-mean), whereas `HashMap` is not. This makes `HashMap` better for non-threaded applications, as unsynchronized Objects typically perform better than synchronized ones.
2. `Hashtable` does not allow `null` keys or values. `HashMap` allows one `null` key and any number of `null` values.
3. One of HashMap's subclasses is [`LinkedHashMap`](http://java.sun.com/javase/7/docs/api/java/util/LinkedHashMap.html), so in the event that you'd want predictable iteration order (which is insertion order by default), you could easily swap out the `HashMap` for a `LinkedHashMap`. This wouldn't be as easy if you were using `Hashtable`.

Since synchronization is not an issue for you, I'd recommend `HashMap`. If synchronization becomes an issue, you may also look at [`ConcurrentHashMap`](http://docs.oracle.com/javase/7/docs/api/java/util/concurrent/ConcurrentHashMap.html).



## 05-14:

**Why is my daughter disobeying me? My daughter is 23 and is an engineer. The day she got the degree, she fled and we don’t know her exact address. She blames me for differentiating between her and her brother and some other stupid childhood things.**

​	Why is my daughter disobeying me?She’s 23 and an adult. She no longer is required to…and actually hasn’t been required to for about 5 years.The day she got the degree, she fled and we don’t know her exact address.That’s probably because you still think that she has to obey you. She’s got the degree, and with that employment opportunities. She’s decided to be the mistress of her own fate without being under your control.She blames me for differentiating between her and her brother and some other stupid childhood things.It may seem stupid to you, but not to her. And considering you still expect her to obey you even though she’s an adult tells me she may have a point.



**what operating system concepts should every programmer be aware of? **
I am compiling various lists of competencies that self taught programmers must have.Among all subjects, Operating Systems is the trickiest one, because creating even a toy operating system is a rather non-trivial task. However, at the same time an application developer (who may not have formally learned CS) must at least be aware of and hopefully should have implemented some key concepts to appreciate how an OS works, and to be a better developer.

I have a few specific questions:

- What key concepts of operating systems are important for a self taught programmer to understand so they can be better software developers (albeit working on regular application development)?
- Is it even remotely possible to learn such a subject in byte sized practical pieces ? (Even a subject like compiler construction can be learned in a hands on way, at a rather low level of complexity)



I would suggest reading Andrew S. Tanenbaum ( http://en.wikipedia.org/wiki/Andrew_S._Tanenbaum ) book on Modern Operating Systems (ISBN 978-0-13-600663-3) as everything is there.However from the book index we can identify the minimum key topics:

- Processes

- Memory management

- File systems

- Input/output

  

And the easiest way to start playing with this topics will be to download **MINIX**:http://www.minix3.org/  and study the code. Older versions of this operating system might be easier to understand.Another useful resource is Mike Saunders How to write a simple operating system that shows you how to write and build your first operating system in x86 assembly language:http://mikeos.sourceforge.net/write-your-own-os.html





## 05-15:	

（今天是关于tomcat的官网文档）

**Introduction**
	For **administrators（管理员）** and web developers alike, there are some important bits of information you should **familiarize（熟悉）** yourself with before starting out. This document serves as a brief introduction to some of the concepts and **terminology（术语）** behind the Tomcat container. As well, where to go when you need help.

**Terminology**
	In the course of reading these documents, you will run across a number of terms; some specific to Tomcat, and others defined by the Servlet and JSP specifications.

​	Context - **In a nutshell（简单的说）**, a Context is a web application.That is it. If you find any more terms we need to add to this section, please do let us know.



**Configuring Tomcat**
	This section will **acquaint（使熟悉，了解）** you with the basic information used during the configuration of the container.All of the information in the configuration files is read at startup, meaning that any change to the files necessitates a restart of the container.



**Where to Go for Help**
	While we've done our best to ensure that these documents are clearly written and easy to understand, we may have missed something. Provided below are various web sites and mailing lists in case you get stuck.

​	Keep in mind that some of the issues and solutions vary between the major versions of Tomcat. As you search around the web, there will be some documentation that is not relevant to Tomcat 8, but only to earlier versions.

​	Current document - most documents will list potential hangups. Be sure to fully read the relevant documentation as it will save you much time and effort. There's nothing like scouring the web only to find out that the answer was right in front of you all along!

- Tomcat mailing list archives - numerous sites archive the Tomcat mailing lists. Since the links change over time, clicking here will search Google.
- The TOMCAT-USER mailing list, which you can subscribe to here. If you don't get a reply, then there's a good chance that your question was probably answered in the list archives or one of the FAQs. Although questions about web application development in general are sometimes asked and answered, please focus your questions on Tomcat-specific issues.
- The TOMCAT-DEV mailing list, which you can subscribe to here. This list is reserved for discussions about the development of Tomcat itself. Questions about Tomcat configuration, and the problems you run into while developing and running applications, will normally be more appropriate on the TOMCAT-USER list instead.
  And, if you think something should be in the docs, by all means let us know on the TOMCAT-DEV list.