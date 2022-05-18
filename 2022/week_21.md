## 05-16:

今天阅读一篇文章：https://blogs.scientificamerican.com/guest-blog/programming-as-a-way-of-thinking/

**Programming as a Way of Thinking**
	The power of modern programming languages is that they are expressive, readable, **concise(简明)**, **precise（精确）**, and executable.

​	Programming has changed. In first generation languages like FORTRAN and C, the **burden（责任、义务）** was on programmers to translate high-level concepts into code. With modern programming languages—I’ll use Python as an example—we use functions, objects, modules, and libraries to extend the language, and that **doesn’t just（不只是）** make programs better, it changes what programming is.

​	Programming used to be about translation: expressing ideas in natural language, working with them in math notation, then writing flowcharts and **pseudocode（伪代码）**, and finally writing a program. Translation was necessary because each language offers different capabilities. Natural language is expressive and readable, pseudocode is more precise, math notation is concise, and code is executable.

​	But the price of translation is that we are limited to the subset of ideas we can express effectively in each language. Some ideas that are easy to express computationally are awkward to write in math notation, and the symbolic manipulations we do in math are impossible in most programming languages.


​	The power of modern programming languages is that they are expressive, readable, concise, precise, and executable. That means we can eliminate middleman languages and use one language to explore, learn, teach, and think.


​	As an example, Figure 1 shows the breadth first search (BFS) algorithm expressed in the pseudocode used in a popular textbook. The authors designed this language to be more concise and readable than most programming languages at the time, which was 1989.

​	Figure 2 shows the same algorithm in Python. It is a few lines shorter than the pseudocode, and because it uses more words than symbols, I think it’s more readable. Also, unlike pseudocode, we can run it, display the results, and debug it.


​	**Running programs is the whole point of programming, of course, but there is more to it. The ability to execute code makes programming a tool for thinking and exploring. When we express ideas as programs, we make them testable; when we debug programs, we are also debugging our brains.**

​	Languages like Python are also ideal for learning and teaching. For example, I wrote a book recently about digital signal processing (DSP). I used Python to write a simple library and Jupyter (which is a software development environment) to **compose（组成）** online notebooks that combine text, code, and results, including images and sound clips.


​	As I developed the book, I wrote code to test my understanding and explain it to students at the same time. Students can run the code to develop a mental model, make changes to test their predictions, and extend my code for their projects.

​	Most textbooks and classes use math to teach signal processing, with students working primarily with paper and pencil. With this approach, the only option is to go “bottom up”, starting with the arithmetic of complex numbers, which is not the most exciting topic, and taking weeks and many pages to get to relevant applications.

​	With a computational approach, we can go “top down”, starting with libraries that implement the most important algorithms, like Fast Fourier Transform. Students can use the algorithms first and learn how they work later. They can see the most important ideas, like spectral decomposition, without being blinded by details. They can work on real applications, on the first day, that provide the motivation to go deeper. And they can have a lot more fun.To demonstrate, I wrote a Jupyter notebook called “Cacophony for the whole family.” If you click that link, you can see the code and listen to the examples. It uses the library I wrote to simulate the sound of a grade school band, with instruments out of tune and some children randomly playing the wrong note. It’s meant to be silly (and a little bit mean), but it also demonstrates aspects of how we perceive sound and **interpret（解释）** the pitch of a complex signal.


​	The languages I am calling modern are not particularly new; in fact, Python is more than 25 years old. But they are not yet widely taught in high schools and colleges. And even where they are adopted, they are often used in a style that does not take advantage of their power.

​	Modern programming languages are qualitatively different from their predecessors, but we are only beginning to realize the implications of that difference.





## 05-17:

（今天是BBC的一篇新闻，请忽略新闻的真实性）

**McDonald's has said it will permanently（永久的） leave Russia after more than 30 years and has started to sell its restaurants.**

​	The move comes after it temporarily closed its 850 outlets in March.The fast food **giant（巨大、巨头）** said it made the decision because of the "**humanitarian（人道主义）** crisis" and "unpredictable operating environment" caused by the Ukraine war.

​	The opening of McDonald's first restaurant in Moscow in 1990 came to **symbolise（象征）** a **thaw（融化）** in Cold War tensions.

​	A year later, the Soviet Union **collapsed（倒塌、奔溃）** and Russia opened up its economy to companies from the West. More than three decades later, however, it is one of a growing number of corporations **pulling out（拔出、退出）**.

​	"This is a **complicated（复杂）** issue that's without precedent and with **profound consequences（深远的结果）**," said McDonald's chief executive Chris Kempczinski in a message to staff and suppliers.Some might argue that providing access to food and continuing to employ tens of thousands of ordinary citizens, is surely the right thing to do," he added. "But it is impossible to ignore the humanitarian crisis caused by the war in Ukraine. And it is impossible to imagine the Golden Arches **representing（代表）** the same hope and promise that led us to enter the Russian market 32 years ago."

​	McDonald’s, Coca-Cola, Starbucks **halt（停止）** Russia sales，McDonald's and Coca-Cola **boycott（抵制）** **calls（呼声）** grow
McDonald's said it would sell all its sites to a local buyer and would begin the process of "de-arching" the restaurants which involves removing its name, branding and menu. It will retain its **trademarks（商标）** in Russia.

​	The chain said its **priorities（优先）** included **seeking（寻求）** to ensure its 62,000 employees in Russia continued to be paid until any sale was completed and that they had "future employment with any **potential（潜在）** buyer".

​	McDonald's said it would write off a charge of up to $1.4bn (£1.1bn) to cover the exit from its investment.

​	It really is the end of an era. I was in the queue when the first Russian McDonald's opened on Moscow's Pushkin Square in January 1990 - way back in the USSR.

​	There were so many people outside the restaurant, it took three hours to get inside. But what a sense of excitement.Those American burgers, fries and pies were a symbol of Moscow embracing the West. Hot food to help end a Cold War.

​	These are very different times. Russia and the West have lost their **appetite（胃口）** for one another.Russia's attack on Ukraine has sparked international condemnation and **sanctions（制裁）**, turning Moscow into a **pariah（贱民）**.

​	Meanwhile, the Kremlin - as it always does - points the finger back, accusing the West of **plotting（密谋）** Russia's downfall.

​	Back in March lots of international companies announced they were pausing operations in Russia, hoping the situation would resolve itself and they could then reopen.

​	But McDonald's decision to sell up and pull out shows the fast food giant recognises things will not return to normal and that what the Kremlin calls its "special military operation" in Ukraine has changed things long term.

​	Big Macs are only the beginning. I predict we're going to see a lot more global brands leaving Russia.







## 05-18:

(今天内容来自BBC，请忽略真实性）

**Shanghai lockdown: The hard life of a homeless deliveryman**

​	Weeks into a strict **lockdown（封锁）**, most of Shanghai's 25 million population continue to rely on delivery **riders（骑手）** to bring them food and supplies. But this largely **invisible（不可见、忽略）** workforce of 20,000 faces a lack of **shelter（庇护、居所）** and safety. Two delivery riders tell the BBC their stories.

​	I've been so busy. So many people need supplies. I make deliveries all day long, then when it's approaching midnight, I look for a place to sleep.

​	I left my apartment on 8 April and haven't been back since. The Shanghai government allows delivery riders to leave and enter their residential **compounds（大院）**. But the compounds insist on enforcing their own policies, and most don't allow riders to return to their own homes. There are hotels that are open, but not many are open to us.

​	There was a tent in front of my compound. You know, those blue ones set up for Covid testing. When I left home, the compound managers asked me to help them buy supplies and in exchange they offered me the blue tent to sleep at night. I left all my stuff in there.

​	But one day the tent was gone. I couldn't find my stuff. The managers said it wasn't their business. Security guards there said they didn't know where my stuff went.

​	So I had to look for a new place to sleep. Sleeping under a bridge just comes naturally to us delivery riders - it can block out the wind and rain. I usually fall asleep immediately after lying down - I feel so tired by then!

​	One day I forgot to pay attention to the weather forecast. It was raining heavily and all the space under the bridge had been taken. I found an ATM room to sleep. It was quite a good place, no-one else was around. My only hope was that the police wouldn't **show up（出现）** and kick me out.

​	But after two nights there, around 2am, policemen on **patrol（巡逻）** saw me and **chased（追捕）** me away. They said I should go to a homeless shelter. But I've tried and it's not open. Nobody was there, not even security guards.


​	In the beginning I survived on dry instant noodles. Later a group of delivery riders found a restaurant that opened secretly and now we go there to buy **takeaways（外卖）**. The police usually just ignore it. We do need a place to eat, right? Some shops also have an outdoor space where there are electrical sockets. We **sneak（悄悄）** over to charge our phones.

​	There was a story going round that a delivery rider died on the streets after getting into a crash. Of course I worry that will happen to me too. But I've been very careful. I always go very slow. If I get into an accident in a remote area, it would be extremely dangerous. The biggest problem is if your **scooter（电瓶车）** breaks down and there is no place to fix it. You can't work any more.

​	Many people saw news reports saying delivery riders can earn up to 10,000 yuan per day ($1,500; £1,200). Since then many have asked me how to become one. My advice is usually: "Don't become a rider."

​	In Shanghai, the pay we earn as riders is quite all right. But most riders only earn a few hundred yuan a day. And I don't think everyone can **put up（提供）** with such hardship, such living and working conditions.

​	But you know, if we weren't doing this, we wouldn't have any income either while under lockdown. That's stressful.


​	I was born in 1999 in Anhui province. When I graduated from high school, I couldn't get into a good university. The **tuition（学费）** fees were too expensive for my family. I was so young and had no idea what I could do. My mum suggested I join my cousin in Shanghai. At least I wouldn't be left with no place to sleep and no food to eat.

​	So I came to Shanghai and worked with my cousin to sell computers. That lasted about two years. Business went down during Covid so I started to look for a new job. I had no place to live back then. I found a shared rental with another rider. It seemed like he was earning a lot. I said: "Brother, could you help me become a rider, too?" So about half a year ago I became one.

​	People told me Shanghai is a developed city, better than my hometown. Now even my family is asking me to go home. They've all heard about the situation here. It's unimaginable that people can starve in Shanghai nowadays.

​	But it's not like I'm starving or anything. I'm from the countryside, I slept in a cowshed when I was a child. I'll be fine.


​	I used to earn on average 4.5 yuan per order. But I don't take these orders anymore, nobody does, it's too low. These days I take orders privately from my clients, through **chat groups（群组）**. I can earn around 1,000 yuan a day.

​	I see larger residential compounds doing group buys of food, but smaller compounds with just a **dozen（一打）** residents have nothing. It's so hard to get people to deliver things to them, it's also hard to order supplies in the first place. Many elderly people also don't know how to do group buys.

​	Orders with small quantities of food won't get delivered now. Fruit shops won't sell individual pieces of fruit any more - you have to buy in bulk now. If someone wants 20 yuan worth of vegetables, I'll end up spending half a day looking for that and get nothing, as only bulk vegetable packages are available and each costs over 100 yuan.

​	Now we have no food and no water, and sleep on the streets. I know at least 40 riders in the same situation as me. There are delivery riders who work for companies which provide hotel rooms for them. But there are those who take online orders from customers, like us, and the local government has done nothing to help us find a place to stay.

​	My residential compound won't let me back in, they say it's likely I'll bring the virus back. I can't go home even if I test negative for Covid. I've been going to hospitals to get tested every day. I'm afraid of getting Covid - all the riders are afraid of it.

​	So I just find a place to sleep outside. My feet **stink（恶臭）** so bad you can smell them from a distance! I'll shower eventually, maybe after the lockdown lifts.

​	What's the point of resting at home anyway? The first week of the lockdown, I only got two cabbages. The second week I only received a box of medicine. Who can survive on that? What do I eat? It's better to be outside - at least I can still find some food.

​	Delivering food is better than working in a factory. I've worked in a few in Shenzhen, earning only 200 yuan per day, working 12 hours a day. Delivery riders have better income and more freedom. How much you earn depends on how much effort you put in.

​	My family has been asking me to come back. But how can I get out now? People even got chased back into the city after driving out to the highway.

​	I'm just waiting for the lockdown to be lifted. I'll leave then. I don't know how much longer I can **hold on（坚持）** for.

I'm so done with Shanghai. Once I leave, I'll never come back.