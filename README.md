**Advanced Web Attack and Exploitation**

**INTRO**

Advanced Web Attack and Exploitations (AWAE). It is an exploit development course based on the Web. it was developed by Offensive Security. The course was only offline at the BlackHat conference for a couple of years, then eventually Offensive Security brings it online. See the syllabus to get more details. [https://www.offensive-security.com/documentation/awae-syllabus.pdf](https://www.offensive-security.com/documentation/awae-syllabus.pdf)

**Am I ready for AWAE?**

Well, this question become increasingly asked by a lot of folks. For me I wasn&#39;t hesitant to sign up; however, to be honest, nobody will give you the right answer except you !! whether you have  **10 years experience**  in the industry or  **fresh graduate**. Here are the things that you may consider to have it before applying for AWAE.  **Otherwise, the course will be heavy**.

- You should be good with well-known web vulnerabilities (LFI, SQLI ..etc)
- Experience in black box testing would be helpful as a mindset.
- Being able to read and understand complex open source projects written by either the following languages (  **PHP, NodeJS, Java, C#**  )
- A solid understanding of these topics  **inheritance, polymorphism**  ..etc ( OOB)
- Being able to focus for long periods on programming &amp; writing exploits.
- Master one interpreter language to automate thing is plus ( Python, Ruby ..etc)

**ENROLLING**

You will be provided materials and a VPN file to access the labs. The materials are divided into 2 parts. A pdf file and videos. The pdf document will explain everything in detail.  **Exercises**  will be constantly at the end of each module as well as  **ExtraMile**. Keep in mind, extra miles are optional but don&#39;t skip any of them.

**EXAM !!**

As always Offsec prepares something unbelievable. The good news is, if you understand the material and you did the exercises and extra miles, then don&#39;t worry about the requirement to pass the exam met except to  **try harder** , and never give up.  **The exam**  has 2 applications and each of them will ask you to bypass the authentication and get RCE. so be prepared and ready !!. Here is my advice for who scheduled the exam.

- It&#39;s better to give yourself a break before the exam date and enjoy yourself with your family.
- Don&#39;t apply black-box testing on input ( it won&#39;t work ).
- Start confidently and challenge yourself to get the whole points, not only the (  **pass**  requirements )
- If you spot the issue and it leads to complicated things stop!!!!! turn around!! (back later if you didn&#39;t find a unique issue)
- Debugging is the key! (  **just remember that**  ) =\&gt; ( print(&quot;reach line 24 :D , pass first condition :D boom!!&quot;))
- Prepare your plan for  **authentication bypass** , for instance (it could be  **login issue, access controller or session prediction, weak token ..etc**  ), I recommended using your list and preparing it before the exam date.
- Don&#39;t read the instructions too much :D, they won&#39;t hide the answers between the words.

**WRAP UP**

Advanced Web Attack and Exploitation is a rewarding course and recommended to anyone who wants to delve into web bug henting. Although the course deal with white box &amp; code review. In addition, the material will guide you on a different technique to use in vulnerability discovery as well as debugging. In the end, you will be able to develop an exploit and chain it with multiple vulnerabilities to gain remote code execution.

**Advanced Windows Exploitation 2022**

**Intro**

Exploit development getting much harder these days, and finding a bug is just the game get start it, chaining vulnerabilities and bypass mitigations is the art of the game. This is a 5-day long class that covers Advanced Windows Exploitation, custom shellcode, VMware guest-to-host, Microsoft Edge type confusion, Kernel overwrites callback, Unsensitized user-mode callback, and a variety of other topics. The textbook is extremely technical, educational, and interesting.

**My journey?**

My journey with Offsec started in 2017 when I was in college which got OSCP, OSCE, and OSWE in 2020. The ultimate goal to get those is to enhance my cybersecurity career expertise.

**AWE in Riyadh**

What&#39;s new in AWE?

AWE revamped in 2021 which removed Flash exploit and replaced it with VMware Guest-To-Host and kernel native driver[win32kfull.sys]

**Day 1,2**

First of all, thanks to the instructors Morten and Alexandru for all your help and valuable information. Day 1 of the class starts you off with 3 hours of a dive into custom shellcode in x64. The rest of the day is spent on VMware. It provides you the opportunity to become familiar with VMware guest-to-host vulnerabilities and where to look at in the featured hunting.

We successfully trigger the bug by opening a backdoor via custom assembly code and performing a full exploit in C/C++.

(The technical aspect of this module wasn&#39;t hard though, the bug was easy to trigger and exploit wasn&#39;t much complicated)

**Day 3**

Moving on to day 3 of the course. We had a good morning with Microsoft edge (Chakra engines ) by exploiting CVE-2019-1539. It wasn&#39;t hard for me since already exploited this CVE back in 2019( https://github.com/0x43434343/CVE-2019-0539/). However, my approach was using ArrayBuffer to get R/W, but they used the DataView object instead. In addition, my method to bypass CFG was to overwrite ret address; however, that won&#39;t defeat modern intel architecture with CET enable ( Shadow Stack). Their approach was new to me which used data-only attacks. (It is another story)

**Day 4,5**

Lastly, it is all about kernel exploitation. I enjoy this part since it was a new subject to me. My experience in kernel exploitation was only with the HEVD project, so digging deep and understanding how windows kernel can be abused is the ultimate goal of this module. They started with easy stuff which third party anti-virus (overwrite callback) then used another vulnerability to leak the Kernel base address, it was a good starting point. They switched to a more complicated bug in a native driver( win32kfull.sys ). The bug was inspired me, and interested in those who willing to understand how kernel callback works and how it can be abused by attackers in some cases. We successfully exploited this bug by hooking user32 API and switching allocation from address mode to offset mode, which gave us an arbitrary write primitive. We proceed to get read primitive by corrupting the TagWnd structure. After that, we continued to bypass all mitigations such as KASLR, SMEP, SMAP, and Page table randomization.

**Exercises and extra mile**

It won&#39;t be hard except the last extra mile. Personally, some extra miles, I challenged myself to find another way to solve it, that&#39;s will let me explore windows internal and kernel structure.

**Exam [** 04/02/2022]

The exam consists of 100 multiple choices with True-False questions. So, to pass the exam, you need to memorize everything with a few leaks from Google.

**True story [Friday]**

I finished my job at 6:00 PM and went to take a nap for 2 hours before the exam. I woke and prepared my Coffee and watched standup comedy to get relax because I know something will not be good waiting for me. I started at midnight and finished the first challenge after 17 hours. I went to bed and slept for 7 hours, then I woke up and started the second challenge and finished it the next day. The exam is kind of hard and no matter how much you prepare; you need to think smarter and harder. All the skills you need to pass the exam are taught in the course.



**Last words**

Having completed all exercises and extra miles has positively impacted my research skills as a security researcher. The more you think about solving problems in many ways, the more you gain knowledge. The course was not entry-level. I highly recommend taking old CVE (browser or kernel) and writing a full exploit. When you take it this way, you will be stuck with a few issues such as ROP, fake object, corrupt object, and a bunch of questions in your head that needs to be answered. Lastly, this will be my last destination with offensive security. Always, stay hungry and stay foolish.

Fahad Alharbi (02/19/2022 ).
 @pwn\_rev

والسلام خير ختام ..

хорошего дня

祝你有美好的一天

haben Sie einen guten Tag

passe une bonne journée

que tenga un buen día
