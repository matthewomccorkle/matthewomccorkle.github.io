---
title:  "Day 36 - Blackbird - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool Blackbird and how it works."
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
3 . What is Blackbird?
<br>
4 . Why use Blackbird?
<br>
5 . How to use Blackbird?
<br>
6 . Summary

---

## This post is designed to introduce you to the tool Blackbird.

![](https://raw.githubusercontent.com/p1ngul1n0/badges/main/badges/20.png)

# <span style="color:red">***Disclaimer***</span> : **Please only use Blackbird for professional and educational reasons. Do not use this tool for nefarious or malicious reasons.**

---

### 1. **Introduction**

Welcome to the **thirty-sixth** blog post of 100 tools in 100 days.<br> 

Find **Blackbird** @ GitHub [here](https://github.com/p1ngul1n0/blackbird).

---

### 2. **My Setup**

For running the Blackbird tool, I used Kali Linux in a VMware Workstation 16 Player virtualized environment.

---

### 3. **What is Blackbird?**

Blackbird is an open source intelligence tool used to check for usernames on 144 websites. 

---

### 4. **Why use Blackbird?**

Blackbird can be used to gather as many pieces of open source data on an organization. Many organization use social media and what they post on social media may offer insight to a penetration tester during testing. 

Additionally, Blackbird can be used by HR personnel and organizations to conduct research on employees social media use outside of the work. 

Finally, a security researcher for an organization may use Blackbird to determine if social media accounts tied to an organization are hosting information that may make entry for malicious actors easier. 

---

### 5. **How to use Blackbird?**

Blackbird works in the terminal as command line only and as a self hosted web server with a GUI and export option. I will show both uses of Blackbird in the below demonstrations.

For my sample username I am searching for `analyst` to keep both results consistent. 

    Step 1:
    First you need to download and install Blackbird.
    In your terminal enter the following commands:

    git clone https://github.com/p1ngul1n0/blackbird

    cd blackbird

    pip install -r requirements.txt

<br>

    Step 2:
    Command line use:
    To use Blackbird in the command line enter the following command while inside the blackbird directory:

    python blackbird.py -u username

<br>

![]()


### 6. **Summary**

 

I hope you enjoyed this blog post.

Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
