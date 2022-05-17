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