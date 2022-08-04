---
title:  "Day 46 - Social-Engineering Toolkit - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool Social-Engineering Toolkit and how it works."
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
3 . What is Social-Engineering Toolkit?
<br>
4 . Why use Social-Engineering Toolkit?
<br>
5 . How to use Social-Engineering Toolkit?
<br>
6 . Summary

---

## This post is designed to introduce you to the tool Social-Engineering Toolkit (SET).

# <span style="color:red">***Disclaimer***</span>: **Please only use Social-Engineering Toolkit for professional and educational reasons. Do not use this tool for nefarious or malicious reasons.**

---

### 1. **Introduction**

Welcome to the **forty-sixth** blog post of 100 tools in 100 days.<br> 


Find **Social-Engineering Toolkit** @ GitHub [here](https://github.com/trustedsec/Social-Engineering-toolkit).

Find TrustedSec website [here](https://www.trustedsec.com/).

Find the SET User Manual @ GitHub [here](https://github.com/trustedsec/Social-Engineering-toolkit/blob/master/readme/User_Manual.pdf).

SET was originally created by David Kennedy, the Founder of TrustedSec, and you can find him at:

[LinkedIn](https://www.linkedin.com/in/davidkennedy4/)

[GitHub](https://github.com/HackingDave?tab=repositories)

---

### 2. **My Setup**

For running the Social-Engineering Toolkit tool, I used Kali Linux in a VMware Workstation 16 Player virtualized environment.

For my victim device, I am using Ubuntu in a VMware Workstation 16 Player virtualized environment. 

---

### 3. **What is Social-Engineering Toolkit?**

Social-Engineering Toolkit is a framework that allows a penetration tester to create custom attacks (mostly social engineering attacks) to use during a penetration test specifically targeting a person or organization. 

Note: this tool is dangerous and should only be used for research in your home lab or by penetration testers with explicit permission. 

---

### 4. **Why use Social-Engineering Toolkit?**

If you are a penetration tester and have flexible rules of engagement, then SET is a great tool for crafting initial malicious social attacks against employees of the organization. 




---

### 5. **How to use Social-Engineering Toolkit?**

Using SET is as difficult as using Metasploit. You do have to know how the options function, however, it is also very easy to understand. Plus, if you ever get stuck you can always refer to the user manual located [here](https://github.com/trustedsec/Social-Engineering-toolkit/blob/master/readme/User_Manual.pdf).

    Step 1:
    In Kali Linux click the Applications icon and go to number 
    "13 - Social Engineering Tools" 
    and select:
    "social engineering toolkit (root)".

    You will need to enter your password if you are using sudo, 
    if you are root this should not apply. 

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/socialengineertoolkit/setoolkit1.PNG)

SET loads into a terminal window and creates its own shell that functions very similarly to the Linux shell. It even offers tab auto-complete. 

    Step 2:
    We have multiple options on the main menu, today we are going to focus 
    on the Social-Engineering Attacks option 1.

    type 1 and press enter

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/socialengineertoolkit/setoolkit2.PNG)

**Note:** If at any time you need to go back to the main menu and there is no option, use Ctrl+C.

### Web Attack -> Credential Harvester Example

This example will show you how to perform a credential harvester attack by presenting a fake clone of Google's login page to the victim. 

    Step 3a:
    Enter option 2 to select Website Attack Vectors.

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/socialengineertoolkit/setoolkit3.PNG)

    Step 3b:
    Enter option 3 to select Credential Harvester Attack Method.

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/socialengineertoolkit/setoolkit4.PNG)

    Step 3c:
    For simplicity of this example choose option 1 for Web Templates.

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/socialengineertoolkit/setoolkit5.PNG)

    Step 3d:
    This is where you would enter an IP address for listening to capture 
    credentials and hosting the page. Since I am working in a close virtual 
    environment I used my Kali NAT address (default) by hitting enter.

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/socialengineertoolkit/setoolkit6.PNG)

    Step 3e:
    I chose option 2, Google template for ease of use for this example.

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/socialengineertoolkit/setoolkit7.PNG)

At this point, the website is being hosted at the address chosen in step 3d which for me is `kali.ip.address:80`.

    Step 3f (victim):
    On the attack machine, you would want to send this hosted page IP 
    address in the form of a phishing email, fake website, 'Click here you 
    won $1,000' style link to the victim. 
    Below is what the victim would see if they clicked the fake link.

    I entered a test username and test password and clicked sign in on the 
    fake Google page. 

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/socialengineertoolkit/setoolkit8.PNG)

Once the victim enters their login credentials to the fake website the site redirects them to the real site (although not logged in, obviously).

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/socialengineertoolkit/setoolkit10.PNG)

    Step 3g: 
    On the attack machine, the captured data is logged in the SET shell and 
    also can be saved to an XML report page for retrieval at a later time. 

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/socialengineertoolkit/setoolkit9.PNG)

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/socialengineertoolkit/setoolkit11.PNG)

The XML file report looks like this:

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/socialengineertoolkit/setoolkit12.PNG)


This is one of the many examples of how to use SET to create malicious social-engineering attacks against persons or organizations. 

### 

### 6. **Summary**

The Social-Engineering Toolkit (SET) is a tool for crafting social-engineering attacks against people and organizations. 

The tool functions in a similar way as Metasploit and allows attackers to create web-based attacks, phishing campaigns, mass mailing campaigns, and many other attack vectors. 

Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
