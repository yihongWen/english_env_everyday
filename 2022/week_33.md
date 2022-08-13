## **08-08:**

**Through a Hacker’s Eyes** 

​	If you ask **system professionals** why network security measures are necessary, most will answer, “To protect against hackers.” Hackers spend a great deal of time and energy exploring systems and networks, searching for ways of **penetrating(渗透)** system defenses, often utilizing the access they gain to disastrous effect. **News accounts（新闻报道）** of hacker exploits are routine, with many government, corporate, and organizational systems on the list of sites taken **out of commission（不能使用）** for days, even weeks. Although one still sees hackers celebrated as evil geniuses, that **perception（看法）** is changing as the list of victims grows longer and the damage associated with the attacks becomes more **indiscriminate（任意的、无差别的）**. If you are charged with protecting a system, understanding the approach **intruders（入侵者）** take as they carry out an attack can sometimes be helpful. This knowledge is valuable for a number of reasons.

- It enables you to spot certain activity patterns as they happen, recognizing the elements of an attack. 
- It enables you to look at your systems **proactively（抢先、主动地）** before the attacker gets to them, correcting **vulnerabilities（缺陷）** that would be found by any attacker searching your site.
- It gives you the insight necessary to make good decisions about protection strategies. Numerous products are marketed for the purpose of protecting systems. Some are a better fit for your environment than others.
- It enables you to make wiser decisions in managing your systems and your users. Security management is a constant balancing act between accommodating needs for access and honoring needs for protection. A knowledge of the threat from one attempting to attack your system gives you a better sense of the impact of **tightening（变紧）** or loosening security **stances（姿态）**. 



**Identifying a Victim** 

​	The first step in a system hack is to decide which system to attack. Two major attack motivations become apparent at this stage of the attack. The first motivation is entertainment or challenge, and the victim selection is almost random. Here the attacker (or a group of cooperating attackers) might use vulnerability scanners to search part of the IP address space, recording hosts that have security vulnerabilities. The second motivation for selecting a hacking target is **self-aggrandizement（名利方面的自我扩展）** or other **tangible（明确的、真是的）** **incentives（激励、奖励）** (including **intellectual property（知识产权）** theft and discovery of sensitive information). Here the targeting of the victim is much more focused, with the attacker gaining knowledge of the victim system through research and information collection. This is usually followed by a more deliberate search and **seizure（夺取）** of the desired information. The motivation for targeting your site can include the following:

- You may be in business competition with the hacker or an entity that has employed that hacker.
- The hacker may have some personal interest in your site, for example, a relative who is an employee of your firm, or a fascination with a product your organization produces.
- Your site may have an odd or amusing domain name.
- Your site may have received **press coverage（新闻报道）**. 
- Your organization may be involved in a political or **ideological（意识形态）** matter of interest to the hacker.



**Casing the Joint（探路）**

​	Once the target of the hack is identified, the hacker determines the goal of the attack. In cases where a particular site has been identified as the target, this determination is likely to include collecting information about the system. The information can come from the **InterNIC（网络信息中心）** and other public sources and can include items such as the system platforms (both hardware and operating system), personnel involved in the management of the system, telephone numbers, MX3 records, registered servers, and other information. If the attacker hasn’t done it already, he or she may run a vulnerability assessment tool against the site, recording the results.

**Gaining Access**

​	With the victim selected and sufficient information gathered to identify possible approaches to attacking the site, the attention of the attacker is likely to shift to gaining access to a site system. In many cases the vulnerability assessment tool run as part of casing the site has identified a vulnerability that allows the attacker to **log on（登录）**. In cases where no vulnerabilities were found, the hacker has several options. 

​	The attacker could utilize **social engineering** techniques for gaining entry. This approach consists of steps such as making telephone calls to users, pretending to be system maintenance or network management personnel, asking for passwords or information. Another option is to introduce a Trojan horse into the system, accomplished by **duping（欺骗）** an **unwitting（不知情）** authorized user into installing the Trojan horse by including it on a disk or network download containing data or software, or by sending it as an email attachment. 

​	Should these measures fail, the next step depends on the determination and expertise levels of the attacker. If both are high, he or she is likely to undertake a more systematic, **rigorous（严格、严密）**, analysis of the target system. For instance, the hacker might review all the system documentation, searching    for known problems. If the operating system or applications source code is available, she or he might search it for vulnerabilities. If the attacker has a system on which to test possible attacks, he or she might construct several test attacks, checking to see whether any were indeed successful. 

​	Once an avenue into the system is isolated, the final item in the strategy is to determine the **timing（发生某事的时间）** of the attack. Many attackers time attacks for late night or early morning when they believe that no one is likely to be using the system. As globalization of organizations with time zone differences has increased the possibility that someone will be utilizing the system at almost any time, day or night, **off-hour（不执勤）** timing might not be as feasible as before. In any event, some attackers target attacks for peak hours so that their activity will blend into the “noise floor” of other system activity.

**Executing the Attack** 

​	After the strategy is set, it’s time to actually execute the attack. Some attackers, utilizing intrusion scripts and other process optimizations, are able to launch a targeted attack and then cover their tracks in a matter of minutes, even seconds. Others, who wish to take a more leisurely approach, might watch the system activities, waiting until the system has no other users logged on to proceed. On UNIX systems in which the finger daemon is enabled, executing a finger command with the name of the targeted system (“finger@targetedhost.com”) returns a list of current users who are logged on the system. When the attacker determines that the coast is clear, she or he will actually use an intrusion script or “borrowed” user IDs and passwords to log on to the machine. Depending on the privilege level of the account, the attacker might be in the system with user privilege. In this case, the attacker may utilize additional hacker tools to try to gain superuser privilege, which will provide **carte blanche（全权）** access to the entire system.

**A. Installing a Back Door：** The first thing that some hackers do after they have entered the machine as superusers is install back doors, system utilities equipped with custom vulnerabilities that allow the hacker to access the machine at a later time. More expert hackers import precompiled system Trojan horses with back doors, devised so that the file statistics do not differ from the original system binaries. Furthermore, the transfer of these Trojan horses may be done with remote commands that are not logged by the system. Part of this step can include installing “Trojaned” versions of critical system binaries that log information about system processes and network connections. These binaries are altered to hide the presence of the attacker. 

**B. Covering Tracks：** **Obscuring（模糊）** the evidence associated with the attack is a critical part of most attack strategies. Attackers have two separate sets of concerns:

- Covering those tracks that might lead a victim or investigator back to the attacker
- Eliminating evidence internal to the system indicating that the attack occurred 

**C. Publicizing the Result**

​	For some hackers, especially those operating as part of a group, the final step in an attack is publicizing the exploit to others. This step is more likely to occur if

- Your site has high name recognition (such as a popular e-commerce site, a major newspaper, or a government agency).
- The attacker is a **juvenile（青少年）**, or otherwise not subject to criminal **prosecution（起诉）** for the offense. This publicity and resulting **notoriety（臭名昭著）** are often considered part of the motivation for the hack. If the hacker is a professional who was **compensated（补偿）** for taking intellectual property or other sensitive information from your site, you will probably never see this stage of the attack.

**D. Studying Predator（捕食者） and Prey（猎物）：** As you encounter and deal with intrusions in your environment, you may see many variations on the themes presented in this article. My point in presenting this information is that your ability to understand the goals of intrusion detection and the suitability of various monitoring and detection strategies depends on your understanding of the threats you hope to counter. Although the ability to hack a system doesn’t necessarily indicate a similar ability to protect the system, those who can best protect the system do understand how an attacker approaches the system. **Only by studying the approaches taken by your adversary can you shift the balance of power in your favor.** Knowledge is the key to changing your role in this relationship from prey to predator. 