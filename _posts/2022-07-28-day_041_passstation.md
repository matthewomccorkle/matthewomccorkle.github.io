---
title:  "Day 41 - Pass Station - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool Pass Station and how it works."
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
3 . What is Pass Station?
<br>
4 . Why use Pass Station?
<br>
5 . How to use Pass Station?
<br>
6 . Summary

---

## This post is designed to introduce you to the tool Pass Station.

![](https://sec-it.github.io/pass-station/_media/logo.png)

# <span style="color:red">***Disclaimer***</span> : **Please only use Pass Station for professional and educational reasons. Do not use this tool for nefarious or malicious reasons.**

---

### 1. **Introduction**

Welcome to the **forty-first** blog post of 100 tools in 100 days.<br> 

Find **Pass Station** @ GitHub [here](https://github.com/sec-it/pass-station).

---

### 2. **My Setup**

For running the Pass Station tool, I used Kali Linux in a VMware Workstation 16 Player virtualized environment.

---

### 3. **What is Pass Station?**

 Pass Station is a command line tool that searches and displays default credentials for thousands of products and vendors.

---

### 4. **Why use Pass Station?**

During penetration testing a tester may find multiple services and hardware on the attack surface of the environment they are testing. 

Many organizations and administrators often glance over default credentials set for accessing those services and hardware, thus leaving the defaults as is. 

Pass Station offers a quick and searchable database of thousands of default credential combinations for many services and pieces of equipment. 

Using a command line tool allows the tester to quickly discover and test for the found default credentials from the database that Pass Station provides. 


---

### 5. **How to use Pass Station?**

    Step 1:
    Installing Pass Station is easy in Kali Linux, simply enter the 
    following command in your terminal to install:

    gem install pass-station

<br>

    Step 2:
    Open up the Pass Station help page by entering the following 
    command in your terminal:

    pass-station -help

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/passstation/pass1.PNG)

    Step 3:
    Using Pass Station is easy, in this example I will look 
    for default credentials for Tomcat:

    pass-station search tomcat

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/passstation/pass2.PNG)

Some limitations of Pass Station are that outputting the results to a wordlist is not an easy command from the way it currently works.

However, you could narrow down search parameters to only find default usernames, output that data as a CSV, use the translate command in Linux to remove commas, and the vendor ID, and the first X lines of the file which has Pass Station information which could then output a single username per line file like a wordlist. 



### 6. **Summary**

Pass Station is a fast command line based search tool that finds default credentials from many services and product vendors. 

This may be an easier tool during penetration testing than say using Google to narrow down results that apply to your situation. 

I hope you enjoyed this blog post.

Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
