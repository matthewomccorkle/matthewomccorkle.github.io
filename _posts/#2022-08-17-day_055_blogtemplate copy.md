---
title:  "Day 55 - Sherlock - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool Sherlock and how it works."
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
3 . What is Sherlock?
<br>
4 . Why use Sherlock?
<br>
5 . How to use Sherlock?
<br>
6 . Summary

---

## This post is designed to introduce you to the tool Sherlock.

![](https://user-images.githubusercontent.com/27065646/53551960-ae4dff80-3b3a-11e9-9075-cef786c69364.png)

# <span style="color:red">***Disclaimer***</span> : **Please only use Sherlock for professional and educational reasons. Do not use this tool for nefarious or malicious reasons.**

---

### 1. **Introduction**

Welcome to the **fifty-fifth** blog post of 100 tools in 100 days.<br> 

Find **Sherlock** @ GitHub [here](https://github.com/sherlock-project/sherlock).

Sherlock was created by Siddharth Dushantha and you can find his respective sites below:

[GitHub](https://github.com/sdushantha)

[LinkedIn](https://www.linkedin.com/in/siddharth-dushantha/)

[Medium](https://sdushantha.medium.com/)


---

### 2. **My Setup**

For running the Sherlock tool, I used Kali Linux in a VMware Workstation 16 Player virtualized environment.

---

### 3. **What is Sherlock?**

Sherlock is another social media username collector, similar to [Blackbird](https://matthewomccorkle.github.io/day_036_blackbird/) and [Maigret](https://matthewomccorkle.github.io/day_045_maigret/).

---

### 4. **Why use Sherlock?**

Sherlock may be a viable option if you wanted to compare findings amongst your other username search tools. Additionally, Sherlock's site list is regularly updated with the latest file updated 27 days ago. 

---

### 5. **How to use Sherlock?**

    Step 1:
    Create a python virtual environment by entering the following:

    python3 -m venv sherlock

<br>

![]()

    Step 2:
    Load the python3 virtual environment by entering:

    source /sherlock/bin/activate

<br>

![]()

    Step 3:
    Clone the Sherlock repository by entering the following command:

    git clone https://github.com/sherlock-project/sherlock.git

<br>

![]()

    Step 4:
    Change your directory into the downloaded repository by entering the following command:

    cd sherlock

<br>

    Step 5:
    Install Sherlock using the following command:

    python3 -m pip install -r requirements.txt

<br>

![]()

    Step 6:
    Verify Sherlock installed by entering the following command:

    python3 sherlock --help

<br>

![]()

    Step 7:
    Search for a username using the following command:

    python3 sherlock <USERNAME>

<br>

![]()

    Step 8:
    Sherlock also can output files, display only found names, and create CSV 
    files for further analysis by entering the following options:

    python3 sherlock <USERNAME> -o <FILENAME> --csv --print-found --verbose

<br>

![]()


### 6. **Summary**

Hopefully Sherlock can be an option for finding usernames during your OSINT / exploitation attempts. This tool offers ease of use, a simple output feature and a CSV output option for further analysis. 

I hope you enjoyed this blog post.

Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
