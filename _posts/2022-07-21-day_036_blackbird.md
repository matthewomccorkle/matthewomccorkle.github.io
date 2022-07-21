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

Blackbird can be used to gather as many pieces of open source data on an organization. Many organizations use social media and their posts may offer insight to a penetration tester during testing. 

Additionally, Blackbird can be used by HR personnel and organizations to conduct research on employees' social media use outside of work. 

Finally, a security researcher for an organization may use Blackbird to determine if social media accounts tied to an organization are hosting information that may lead to an entry point for malicious actors.

---

### 5. **How to use Blackbird?**

Blackbird works in the terminal as command line and as a self hosted web server with a GUI and export option. I will show both uses of Blackbird in the below demonstrations.

For my sample username, I am searching for `analyst` to keep both results consistent. 

    Step 1:
    First, you need to download and install Blackbird.
    In your terminal enter the following commands:

    git clone https://github.com/p1ngul1n0/blackbird

    cd blackbird

    pip install -r requirements.txt

<br>

    Step 2:
    To view the help page for Blackbird enter the following command while 
    inside the blackbird directory from step 1:

    python3 blackbird.py --help

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/blackbird/blackbird0.PNG)

# <span style="color:red">**Warning:**</span> some of the sites tested are NSFW. Please proceed with caution as the screenshots show URLs inappropriate for work websites. 

    Step 3 (CLI):
    Command line use:
    To use Blackbird in the command line enter the following command:

    python blackbird.py -u username

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/blackbird/blackbird6.PNG)

    Step 4 (WEB):
    Web GUI use:
    To use Blackbird as a self hosted website enter the following command:

    python blackbird.py --web

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/blackbird/blackbird1.PNG)

    Step 5 (WEB):
    On your browser navigate to the web server address displayed in step 4.

    http://127.0.0.1:5000

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/blackbird/blackbird2.PNG)

    Step 6 (WEB):
    Web GUI use is extremely easy. 
    Type the username you want to search for and click the arrow button to 
    the right of the input field to perform the search. 

    Once the search is complete you will see a website with results.

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/blackbird/blackbird3.PNG)

    Step 7 (WEB):
    From the web results, you can export the results as a PDF file by clicking
    export as, choosing PDF and saving the file.

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/blackbird/blackbird4.PNG)

<br>

The PDF allows for easy viewing of results, captured metadata, and possible captured profile photos.

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/blackbird/blackbird5.PNG)

### 6. **Summary**

Blackbird is an open source intelligence tool for searching usernames at 144 popular websites.

Blackbird uses 1,000 different user agents to prevent the blocking of requests.

Blackbird functions on HTTP request codes to determine if a username is matched to a profile on the site tested. 

The information is easily exported as an easy to view PDF report.  

I hope you enjoyed this blog post.

Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
