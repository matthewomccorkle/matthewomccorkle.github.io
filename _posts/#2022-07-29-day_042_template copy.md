---
title:  "Day 42 - tmpmail - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool tmpmail and how it works."
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
3 . What is tmpmail?
<br>
4 . Why use tmpmail?
<br>
5 . How to use tmpmail?
<br>
6 . Summary

---

## This post is designed to introduce you to the tool tmpmail.

![](https://raw.githubusercontent.com/sdushantha/tmpmail/master/images/logo.png)

# <span style="color:red">***Disclaimer***</span> : **Please only use tmpmail for professional and educational reasons. Do not use this tool for nefarious or malicious reasons.**

---

### 1. **Introduction**

Welcome to the **forty-second** blog post of 100 tools in 100 days.<br> 

Find **tmpmail** @ GitHub [here](https://github.com/sdushantha/tmpmail).

tmpmail was created by Siddharth Dushantha and you can find his respective sites below:

[GitHub](https://github.com/sdushantha)

[LinkedIn](https://www.linkedin.com/in/siddharth-dushantha/)

[Medium](https://sdushantha.medium.com/)

---

### 2. **My Setup**

For running the tmpmail tool, I used Kali Linux in a VMware Workstation 16 Player virtualized environment.

---

### 3. **What is tmpmail?**

 tmpmail is a command line based temporary email tool which allows the generation of a random or defined email address for temporary use. 

---

### 4. **Why use tmpmail?**

During website testing often a security researcher has to test login features and design for vulnerabilities. tmpmail offers a quick command line option for creating random email addresses to use for this process.

Penetration testers may test various functions of a target and require temporary email addresses just for testing.

tmpmail currently uses 9 different temporary email providers for generating email accounts:

- 1secmail.com
- 1secmail.org
- 1secmail.net
- wwjmp.com
- esiix.com
- oosln.com
- vddaz.com
- bheps.com
- dcctb.com

---

### 5. **How to use tmpmail?**

Installing tmpmail is easy but does require 2 additional dependencies and some extra steps to place the executable in your bin folder.

First we will get tmpmail downloaded and moved to your bin folder and then I will show you how to get the two required dependencies.

Note: I am using Kali Linux so my commands may differ from yours if you are using an alternative operating system or distribution. 

    Step 1:
    First, download the file and give it executable permissions:

    curl -L "https://raw.githubusercontent.com/sdushantha/tmpmail/master/tmpmail" > tmpmail && chmod +x tmpmail

<br>

![]()

    Step 2:
    Next move the executable from its downloaded location to your $PATH, for me that is /usr/bin/.

<br>

![]()

    Step 3:
    Next ensure you can run tmpmail as a command by entering the following command:

    tmpmail -h

    If you see the missing dependencies continue to step 4 or move on to step 5.

<br>

![]()

    Step 4:
    Install the missing dependencies by entering the following command:

    sudo apt-get install xclip w3m

<br>

![]()

    Step 5:
    Now run the tmpmail help command again to see if tmpmail is full functioning:

    tmpmail -h

<br>

![]()

    Step 6:
    The first step in using tmpmail is generating a temporary email, enter the following command (I created a random one):

    tmpmail -g

<br>

![]()

    Step 7:
    Next I tested the random address and sent it an email from a test account I setup for this series.

<br>

![]()

    Step 8:
    To view the inbox enter the following command:

    tmpmail

<br>

![]()

    Step 9:
    To view the most recent email enter the following command:

    tmpmail -r

<br>

![]()

    Step 10:
    To view a specific email enter the email identification number after the 
    command tmpmail (the email idenitification number is the number that 
    appears in the tmpmail command left of each email listed):

    tmpmail 123456789

<br>

![]()

    Step 11:
    To view a specific email in your browser of choice (must know browser name) enter the following command:

    tmpmail -b browsernamehere 123456789

<br>

![]()

Finally, I wanted to test if the tool could render or retrieve attachments from the temporary mail services and it does. Using the same command in step 11 I opened an email with atatchment and I could then download the attachment as needed.

![]()


### 6. **Summary**

tmpmail is a great command line tool for accessing temporary email addresses quickly.

tmpmail allows a tester or security researcher to have temporary email addresses at their fingertips without ever leaving the terminal.

I hope you enjoyed this blog post.

Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
