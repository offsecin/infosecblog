---
layout: post
title: My OSCP Experience .
img: OSCP.png # Add image post (optional)
date: 2020-07-05 11:35:00 AM
description: OSCP Experience,OSCP in india,OSCP as a college Student,OSCP Resources,Noob to OSCP
tag: [Cyber Security,Offensive security,OSCP,Hacking,OSCP IN INDIA,Penetration Testing,OSCP Internship]
---

<span style="color:green">
This is my first  blog so please excuse me for any sort of errors.<br />
 </span>

<span style="color:green">
Today i am going to describe how i got my OSCP  Certification in the month of october 2019, compromising five out of five boxes.
The OSCP journey began when i was in first year of my college. I started practicing on hackthebox after my college. I was hardly able to get 4-5 hours of time to utilize that for cyber security stuffs after my college hours. Then i continued practicing on HacktheBox and Vulnhub untill i was very sure that i could qualify OSCP. Beacuse i was from a  lower middle class family ,And the OSCP exam is very costly (at least to me ), so i wanted to pass in the very first attempt.Now after two years when i began my third year of engineering i decided to give it a go,meanwhile i had done most of the recommended boxes for OSCP at</span> [Vulnhub](http://vulnhub.com)  <span style="color:green">  and on </span> [Hackthebox](http://www.hackhtebox.eu). <span style="color:green"> I had done many boxes but initially i started doing them with the help of  walkthrough's. Then slowly i could do that myself with little or no  hints. </span>

# Preparation Time
<span style="color:green">
It was the   month of may when i signed up for the OSCP course (30 days LAB Access), because i had  vacation in  my college, a perfect time which could be used for OSCP labs. Also i signed up only for 30 days, although you can take for 30,60 or 90 days.After few days on 9th june 2019 i received my Penetration Testing Course Material(PWK). The excitement was at it's peak.I quickly downloaded them and started doing the labs. On the very first day of my OSCP Lab , i was able to root five linux boxe's. Most of these boxes were easy to medium  in diffculty. Linux was my strong point,so i decided to go with linux and kept windows to be done at last(Please dont do this if you are not comfortable with windows). Simlarly from second to fifth  day of lab, i was able to root five boxes everyday. During this time i got stucked  at one or two machines  for a while but i went to OSCP forum for the help and the comments from other peoples there was enough to guide  me in the right direction.

<span style="color:green">
Now i was really confident about linux boxes . So  after 6-7 days of OSCP Lab i went  straight to  Windows boxes which was my weak point. Initially i struggled for them but after trying a bit  i was able to solve most of them. If you really want to pass exam you have to be sure that it's windows boxes that will be more prevailent during the exam. After compromising around 30-33 boxes i decided to quit the OSCP labs. It was my own decision and never suggests you to do so.Along the way i heard that Humble,Pain and Sufferance were the most difficult boxes.So i stared humble during that day in did that in around 16-20 hours with few minor breaks in between.At that point of time i decided to join Hackthebox VIP membership which allows you to practice on retired machines.As windows was my weak point i did many labs watching and learning with IPPSEC channel (ee below). Also OSCP demands you to master 32-bit windows Buffer OverFlow's as you have to be sure that you will get one 25 point from that topic.I used cyber Mentors Buffer Overflow series.Along the way i read several other blogs, took notes to read as much as i could and scheduled the exam.
</span>

# Exam Time
<span style="color:green">
On the 26th of june 2019 it my exam day. I was a bit of nervous and waited for the exam to began at around 10'o clock that day. I started my exam and i decide to start with a linux box, i quickly got root shell on 10 points box. Buffer Overlflow which is easiest one for almost all OSCP folks and worth in terms of points,so was the next one for me.i was struggling for Badchars(Make Sure you Practice them a lot).I was making few minor mistaked which daunted me for 2-3 hours.But finally i got the shell on the box. I kept my Full NMAP scans running in the background so that i don't have to wait for them after i finish working on any machine.Then i started with a windows box and got  stcuked for 5-6 hours(Yes that's true). But i  was able to only got the user shell on the box. Still i needed  more points to pass.Then i got the only the USER shell on another 25 points box and i could not root that.But i was able to get user shell  on another 20 point box.Now i knew that i was in safe zone and i got the pass amrks.I ended the exam and just relaxed myself because i could not sleep that night.
 </span>
<span style="color:green">
Here comes the part you will YELL at me or you simply don't believe.OSCP requires you to have a  well documented  REPORT. Although i took many screenshots during exam, not missed a single one. But i was having my exam at Friend's room simply because i could not have done in that hostel. I came to my room and slept at night without doing anything.And trust me woke up the next day at around 9'o clock and the report was to be submitted only within two hours. I felt like blown away.That night of comfortable sleep took everything of mine. And i didn't submitted my report.
 </span>
<span style="color:green">
I know you will call me a stupid. But after preparing the report i submitted after the actual hours and my report was rejected.
I was feeling guilty at myself.But that gave me a lesson.
</span>

# Lesson's Learned
<span style="color:green">
Now it was my time to learn how to be sincere as i my was lazy or you can call me whatever you wish.
I have to prepare many sample Reports including previous lab walkthroughs to make myself comforatable with Reporting issue.
 </span>

# Exam Time Again
<span style="color:green">
This time i was really not that nervous beacause i knew i could most probably do that. I took my second attempt (after passing my first one LOL) and i started with 25 points  buffer  overflow box. It took  me few hours to get in and i was done with that. Next i was able to get root on 10 points box. Next one was 25 points windows box.I got user shell very quick but it took me around 2-3 hours to get Administrator shell.This was the most difficult box for me as i had never done any previous box either on Hackthebox or on OSCP lab machines.It was tough. Next one was another windows box with 20 points. I was able to get Administrator shell very quickly.Finally there was a linux box of 20points which i used my only metasploit (allowed only once during OSCP as you all knows). Now i did  all the 5 boxes. But this time i took my all the screenshots ,reviewd them. Not only that i did all the machines once again to be sure that i may not miss anything. Couple of hours were left to finish the exam but i ended it quick. And went straight to prepare my report without any delay. I didn't sleep at all, neither i ate anything until i was done with the report and submitting that successfully.
</span>
# Result 
<span style="color:green">
It hardly took  3-5 days and i was greeted with this email. <br />
<img src="{{site.baseurl}}/assets/img/email.png">
<br />
</span>
# Exam Tips and Resources

<span style="color:green">
1.Practice as many boxes as you can. OSCP won't ask you for something fancy other than what you have beem taught in labs. But exam machines can be a bit more diffcult than your labs.
1.Report should be very well documented and please take it very seriously else you may have to suffer.<br />
2.Practice privilege escalation in it's best way , most importantly for windows.<br />
3.Make sure you don't miss any screenshots throughout you exam.
4.OSCP is not that hard but also it's not very easy.It's fully practical and gives you  real and practical experience of Penetration Testing.So it demands you to know the basics of exploitation. So there is no reason to be scared or feel nervous during exam.<br />
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
 
 
 
 
 
 
 

