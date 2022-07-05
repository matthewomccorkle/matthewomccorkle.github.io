---
title:  "Day 24 - Searchsploit - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool Searchsploit and how it works."
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
3 . What is Searchsploit?
<br>
4 . Why use Searchsploit?
<br>
5 . How to use Searchsploit?
<br>
6 . Summary

---

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/searchsploit/searchsploit1.PNG)

## This post is designed to introduce you to the tool Searchsploit.

# <span style="color:red">***Disclaimer***</span>: **Please only use Searchsploit for professional and educational reasons. Do not use this tool for nefarious or malicious reasons.**

---

### 1. **Introduction**

Welcome to the **twenty-fourth** blog post of 100 tools in 100 days.<br> 


Find **ExploitDB** [here](https://www.exploit-db.com/).

Find **Searchsploit** [here](https://www.exploit-db.com/searchsploit).

---

### 2. **My Setup**

For running the Searchsploit tool, I used Kali Linux in a VMware Workstation 16 Player virtualized environment.

---

### 3. **What is Searchsploit?**

Searchsploit is an archive search tool that searches https://www.exploit-db.com/.

Exploit-db.com is a website that hosts a database of known exploits that exist for information systems. 

---

### 4. **Why use Searchsploit?**

Searchsploit allows a user quick searching capabilities of the exploit-db.com database right from the command line. 

You can download the exploits directly to your device to use against devices or create payloads during penetration testing.

---

### 5. **How to use Searchsploit?**

    Step 1:
    First you need to update searchsploit by running the following command:

    searchsploit -u

<br>

    Step 2:
    To search for a specific exploit you use the following command:

    searchsploit <key words>

<br>

I searched for a `tomcat 3.` exploit in my example below:

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/searchsploit/searchsploit3.PNG)


    Step 3:
    Now that I found the exploit I want to work with I can use searchspolit again to directly copy it!

    I run the following command to grab the Python file for
    AJP 'Ghostcat File Read/Inclusion'

    searchsplot -m 48143

<br>

This command copied the 48143.py file directly to the directory I was working in.

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/searchsploit/searchsploit4.PNG)

Now I could use that Python file to exploit Apache Tomcat.

Not all exploits work right out of the box, and most require you to read about the exploit and tweak your settings to make the exploit work. 

### 6. **Summary**

Searchsploit is an archive database search tool used in the terminal to search exploit-db.com and to make copies of the exploits that are uploaded to the database.

Many of the exploits on Exploitdb do require further research to get working so it is important that you read about the exploit and determine how it functions. 


Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
