---
layout: post
title: My OSCP Experience .
img: OSCP.png # Add image post (optional)
date: 2020-07-05 11:35:00 AM
description: OSCP Experience,OSCP in india,OSCP as a college Student,OSCP Resources,Noob to OSCP
tag: [Cyber Security,Offensive security,OSCP,Hacking,OSCP IN INDIA,Penetration Testing,OSCP Internship]
---

<span style="color:green">
This is my first blog, so please excuse me for any sort of errors.<br />
 </span>

<span style="color:green">
Today I am going to describe how I got my OSCP Certification in the month of October 2019, compromising five out of five boxes.
The OSCP journey began when I was in the first year of college. I started practising on Hackthebox after college hours. I was hardly able to get 4-5 hours of time to utilise for cyber security stuff after my college hours. Then I continued practising on HacktheBox and Vulnhub until I was very sure that I could qualify for OSCP. Because I was from a lower middle class family and the OSCP exam is very costly (at least to me ), I wanted to pass on the very first attempt. After two years, when I began my third year of engineering, I decided to give it a go. Meanwhile, I had done most of the recommended boxes for OSCP at</span> [Vulnhub](http://vulnhub.com)  <span style="color:green">  and on </span> [Hackthebox](http://www.hackhtebox.eu). <span style="color:green"> I had done many boxes, but initially I started doing them with the help of walkthroughs. Then slowly, I could do that myself with little or no hints. </span>

# Preparation Time
<span style="color:green">
I signed up for the OSCP course (30 days LAB Access) in May because I had a vacation in my college at the time, which was ideal for OSCP labs. Also, I signed up only for 30 days, although you can take it for 30, 60, or 90 days. After a few days, on June 9th, 2019, I received my Penetration Testing Course Material(PWK). The excitement was at its peak. I quickly downloaded them and started doing the labs. On the very first day of my OSCP Lab , I was able to root five Linux boxes. Most of these boxes were easy to medium in difficulty. Linux was my strong point,so I decided to go with Linux and kept Windows to be done at last(Please don't do this if you are not comfortable with Windows). From the second to the fifth day of lab, I was able to root five boxes every day. During this time, I got stuck at one or two machines for a while, but I went to the OSCP forum for help, and the comments from other people there were enough to guide me in the right direction.

<span style="color:green">
Now I am really confident about Linux boxes . So after 6-7 days of OSCP Lab, I went straight to Windows boxes, which was my weak point. Initially, I struggled with them, but after trying a bit, I was able to solve most of them. If you really want to pass the exam, you have to be sure that it's windows boxes that will be more prevalent during the exam. After compromising around 30-33 boxes, I thought of doing Humble because I had heard that Humble, Pain, and Sufferance were the most difficult boxes. So I started doing HUMBLE that day and I did that in around 16-19 hours with a few minor breaks in between. Then I decided to quit the OSCP labs. It was my own decision and I never suggested you do so. At that point in time, I joined Hackthebox VIP Labs, which would allow me to practise on retired machines. Because Windows was my weak point, I spent a lot of time watching and learning with the IPPSEC channel. Also, OSCP demands you master 32-bit Windows Buffer Overflow. Be sure that you will get one 25-point box from that topic during the exam. I used Cyber Mentors' Buffer Overflow series. Along the way, I read several other blogs, took notes to read as much as I could, and scheduled the exam for after a few days.
</span>

# Exam Time
<span style="color:green">
My exam day is June the 26th, 2019. I was a bit nervous and waited for the exam to begin at around 10 o'clock that day. I started my exam and I decided to start with a Linux box. I quickly got root shell on a 10 point box. So was the next one for me, which was the Buffer Overloop, which is the easiest one for almost all OSCP folks and worth the points,so was the next one for me.I was struggling with Badchars (make sure you practise them a lot). I was making a few minor mistakes because of which I had to waste 2-3 hours. But finally, I got the shell on the box. I kept my full NMAP scans running in the background so that I don't have to wait for them after I finish working on any machine. Then I tried a Windows box and got stuck for 5-6 hours (true story). But I was able to only get the user shell on the box. Still, I needed more points to pass. Then I got the only USER shell on another 25 point box and I could not root that. But I was able to get a user shell on another 20 point box. I now knew that I was in a safe zone and I got the pass amrks.I ended the exam and just relaxed because I could not sleep that night.
 </span>
<span style="color:green">
Here comes the part you will yell at me or you simply don't believe. OSCP requires you to have a well documented report. Although I took many screenshots during the exam, I did not miss a single one. But I was having my exam at a friend's room simply because I could not have done it in that hostel. I went to my room and slept at night without doing anything. And trust me, I woke up the next day at around 9'o clock and the report was to be submitted only within two hours. I was completely taken aback. That night of comfortable sleep took everything from mine. And I didn't submit my report.
 </span>
<span style="color:green">
I know this might sound silly, but honestly, I had no exposure to report writing skills as I was in college where cyber security and report writing were totally new. But after preparing the report, I submitted it after the actual hours and my report was rejected.
I was feeling guilty about myself. But that gave me a lesson.
</span>

# Lesson's Learned
<span style="color:green">
Now it was my time to learn how to be sincere as I was lazy.
I have to prepare many sample reports, including previous lab walkthroughs, to make myself comfortable with the reporting issue.
 </span>

# Exam Time Again
<span style="color:green">
This time I was really not that nervous because I knew I could most likely do that. I took my second attempt (after passing my first one LOL) and I started with a 25 point buffer overflow box. It took me a few hours to get in and I was done with that. Next, I was able to get root on a 10 point box. The next one was a 25 point window box. I got user shell very quick but it took me around 2-3 hours to get Administrator shell. This was the most difficult box for me as I had never done any previous boxes, either on Hackthebox or on OSCP lab machines. It was tough. The next one was another window box with 20 points. I was able to get an administrator shell very quickly. Finally, there was a linux box of 20points on which I used my only metasploit (allowed only once during OSCP, as you all know). Now I've done all the five boxes. But this time I took all the screenshots and reviewed them. Not only that, but I ran through all of the machines again to ensure that I didn't overlook anything. A couple of hours were left to finish the exam, but I ended it quickly. and went straight to preparing my report without any delay. I didn't sleep at all, nor did I eat anything until I was done with the report and submitted it successfully.
</span>
# Result 
<span style="color:green">
It hardly took 3-5 days and I was greeted with this email. <br />
<img src="{{site.baseurl}}/assets/img/email.png">
<br />
</span>
# Exam Tips and Resources

<span style="color:green">
1.Practice as many boxes as you can. OSCP won't ask you for anything fancy other than what you have been taught in labs. But exam machines can be a bit more difficult to use than your labs.
2.The report should be very well documented and please take it very seriously or else you may have to suffer..<br />
3.Practice privilege escalation in it's best way , most importantly for windows.<br />
4.Make sure you don't miss any screenshots throughout your exam.<br/>
5.OSCP is not that hard, but it's also not very easy. It's fully practical and gives you real and practical experience of Penetration Testing.So it demands that you know the basics of exploitation. So there is no reason to be scared or feel nervous during the exam..<br />
</span>
<h3>
<span style="color:red"> OSCP Reference - These are more than enough to be an OSCP holder (in my opinion.)</span>
 <h3>
 <p>
 <span style="color:SlateBlue">
 <br> 1. <a href="https://www.youtube.com/channel/UCa6eh7gCkpPo5XXUDfygQQA">Ippsec YouTube Channel</a> 
 <br> Ippsec's channel  was  what i used during 90% of my prepartion.
  <br>2.<a href="https://0xdf.gitlab.io/">0xdf Blog</a> 
  <br>3.<a href="https://www.youtube.com/watch?v=qSnPayW6F7U&list=PLLKT__MCUeix3O0DPbmuaRuR_4Hxo4m3G">Cyber Mentor BOF Series</a>
 <br> 4.Other Resources 
  <br>https://github.com/wwong99/pentest-notes/blob/master/oscp_resources/OSCP-Survival-Guide.md 
 <br> https://github.com/xxooxxooxx/xxooxxooxx.github.io/wiki/OSCP-Survival-Guide 
 <br> https://medium.com/@hakluke/haklukes-ultimate-oscp-guide-part-3-practical-hacking-tips-and-tricks-c38486f5fc97
  <br>https://awesomeopensource.com/project/SecWiki/linux-kernel-exploits 
 <br> https://github.com/lucyoa/kernel-exploits 
 <br> https://github.com/xapax/security/blob/master/privilege_escalation_-_linux.md 
 <br> https://blackwintersecurity.com/ 
 <br> https://www.jpsecnetworks.com/week-7-oscp-preparation-buffer-overflow/ 
 <br> https://github.com/abatchy17/WindowsExploits 
 <br> https://github.com/SecWiki/windows-kernel-exploits/tree/master/MS08-025 
 <br> https://sevrosecurity.com/checklists/windows-priv-esc/ 
 <br> https://github.com/21y4d/Windows_BufferOverflowx32 
 <br> https://www.absolomb.com/2018-01-26-Windows-Privilege-Escalation-Guide/ 
 <br> https://securism.wordpress.com/oscp-notes-privilege-escalation-windows/ 
 <br> https://infamoussyn.wordpress.com/2014/07/11/gaining-a-root-shell-using-mysql-user-defined-functions-and-setuid-binaries/ 
 <br> https://hackingandsecurity.blogspot.com/2017/09/oscp-tricks.html 
 <br> https://daya.blog/2018/01/06/oscp-ref/ 
 <br> https://github.com/rewardone/OSCPRepo/tree/master/scripts/recon_enum 
 <br> https://scund00r.com/all/oscp/2018/02/25/passing-oscp.html 
 <br> http://futureoscp.blogspot.com/2017/10/usefull-oscp-material.html 
 <br> https://github.com/Optixal/OSCP-PWK-Notes-Public 
 </span>
  </p>
 
 
 
 
 
 
 

