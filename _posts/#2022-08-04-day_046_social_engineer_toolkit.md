---
title:  "Day 46 - Social-Engineer Toolkit - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool Social-Engineer Toolkit and how it works."
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
3 . What is Social-Engineer Toolkit?
<br>
4 . Why use Social-Engineer Toolkit?
<br>
5 . How to use Social-Engineer Toolkit?
<br>
6 . Summary

---

## This post is designed to introduce you to the tool Social-Engineer Toolkit (SET).

# <span style="color:red">***Disclaimer***</span>: **Please only use Social-Engineer Toolkit for professional and educational reasons. Do not use this tool for nefarious or malicious reasons.**

---

### 1. **Introduction**

Welcome to the **forty-sixth** blog post of 100 tools in 100 days.<br> 


Find **Social-Engineer Toolkit** @ GitHub [here](https://github.com/trustedsec/social-engineer-toolkit).

Find TrustedSec website [here](https://www.trustedsec.com/).

Find the SET User Manual @ GitHub [here](https://github.com/trustedsec/social-engineer-toolkit/blob/master/readme/User_Manual.pdf).

SET was originally created by David Kennedy , the Founder of TrustedSec, and you can find him at:

[LinkedIn](https://www.linkedin.com/in/davidkennedy4/)

[GitHub](https://github.com/HackingDave?tab=repositories)

---

### 2. **My Setup**

For running the Social-Engineer Toolkit tool, I used Kali Linux in a VMware Workstation 16 Player virtualized environment.

For my victim device I am using Ubuntu in a VMware Workstation 16 Player virtualized environment. 

---

### 3. **What is Social-Engineer Toolkit?**

Social-Engineer Toolkit is a framework that allows a penetration tester to create custom attacks (mostly social engineering attacks) to use during a penetration test specifically targeting a person or organization. 

Note: this tool is dangerous and should only be used for research in your home lab or by penetration testers with explicit permission. 

---

### 4. **Why use Social-Engineer Toolkit?**

If you are a penetration tester and have flexible rules of engagement, then SET is a great tool for crafting initial malicious social attacks against employees of the organization. 




---

### 5. **How to use Social-Engineer Toolkit?**

Using SET is as difficult as using Metasploit. You do have to know how the options function, however, it is also very easy to understand. Plus, if you ever get stuck you can always refer to the user manual located [here](https://github.com/trustedsec/social-engineer-toolkit/blob/master/readme/User_Manual.pdf).

    Step 1:
    In Kali linux hit the Applications icon and go to number 
    13 - Social Engineering Tools and select SET.

    You will need to enter your password if you are using sudo, 
    if you are root this should not apply. 

<br>

![]()

SET loads into a terminal window and creates its own shell that functions very similarly to the Linux shell. It even offers tab auto-complete. 

    Step 2:
    We have multiple options on the main menu, today we are going to focus on the Social-Engineering Attacks option 1.

    type 1 and press enter

<br>

![]()

**Note:** If at any time you need to go back to the main menu and there is no option, use Ctrl+C.

### Web Attack -> Credential Harvester Example

This example will show you how to perform a credential harvester attack by presenting a fake clone of Google's login page to the victim. 

    Step 3a:
    Enter option 2 to select Website Attack Vectors.

<br>

![]()

    Step 3b:
    Enter option 3 to select Credential Harvester Attack Method.

<br>

![]()

    Step 3c:
    For simplicity of this example choose option 1 for Web Templates.

<br>

![]()

    Step 3d:
    This is where you would enter an IP address for listening to capture 
    credentials and hosting the page. Since I am working in a close virtual environment I used my Kali NAT address (default) by hitting enter.

<br>

![]()

    Step 3e:
    I chose option 2, Google template for ease of use for this example.

<br>

![]()

At this point the website is being hosted at the address chosen in step 3d which for me is `kali.ip.address:80`.

    Step 3f (victim):
    On the victim machine you would want to send this hosted page IP address in the form of a phishing email, fake website, 'Click here you won $1,000' style link. Below is what the victim would see if they clicked the fake link.

<br>

![]()

    Step 3g (victim):
    I entered a test username and test password and clicked sign in on the fake Google page. 

<br>

![]()

    Step 3h: 
    On the attack machine the captured data is logged in the SET shell and also can be saved to a XML report page for retrieval at a later time. 

<br>

![]()



### 

### 6. **Summary**



Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
