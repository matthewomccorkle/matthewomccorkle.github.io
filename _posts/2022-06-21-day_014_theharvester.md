---
title:  "Day 14 - theHarvester - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool theHarvester and how it works."
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
3 . What is theHarvester?
<br>
4 . Why use theHarvester?
<br>
5 . How to use theHarvester?
<br>
6 . Summary

---

## This post is designed to introduce you to the tool theHarvester.

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/theharvester/theharvester1.png)

# <span style="color:red">***Disclaimer***</span>: **Please only use theHarvester for professional and educational reasons. Do not use this tool for nefarious or malicious reasons.**

---

### 1. **Introduction**

Welcome to the **fourteenth** blog post of 100 tools in 100 days.<br> 


Find **theHarvester** [here](https://github.com/laramies/theHarvester).

---

### 2. **My Setup**

For running the theHarvester tool, I used Kali Linux in a VMware Workstation 16 Player virtualized environment.

---

### 3. **What is theHarvester?**

First, we need to describe open-source intelligence (OSINT)to understand theHarvester.

You may recall from the last post #12 that used a tool named Instaloader to grab content from Instagram.

Technically, the content that is easily available to the public is considered open-source intelligence. Anyone can access the information.

theHarvester takes advantage of the massive amount of open-source intelligence that exists on the internet and finds specific information that a user is searching for.

**Imagine** a Google for the results of Google that looks for specific bits of information. 

As of writing this post, theHarvester has 40 passive search data sources that it can use to find open-source intelligence. 

Some of the sources do require API keys to function appropriately, so check out the GitHub for information on which sources contain additional requirements. 

---

### 4. **Why use theHarvester?**

For personal research, you could use theHarvester to find all LinkedIn users who have affiliated themselves with an organization. 

With this information, you could then reach out to approriate connections that may work in the same field as yourself. 

For penetration testing, you could use theHarvester to build the open-source data points while conducting your passive reconnaissance on a taret.

theHarvester can also be used for finding DNS, IP addresses, subdomains, etc. 

For my example, I am using the harvester to collect data that matches the domain neopets.com.

---

### <span style="color:red">***Warning***</span>: 
**theHarvester** may cause an overload of requests to Google, if this happens you will see the message: "Google is blocking your IP and the workaround, returning". 

There are only two ways of fixing this (that I found), waiting some time until Google is no longer blocking theHarvester from functioning, or resetting your ISP modem to retrieve a new IP address. 

Some individuals online claim you can just bounce IP addresses using a VPN, I have not tried this method. 

*Note:* this does not block your IP from using Google temporarily, it just blocks those requests from theHarvester.

See below screenshot for the Google block:

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/theharvester/theharvester5.png)

### 5. **How to use theHarvester?**

    Step 1:
    run theHarvester using the command below:

    theHarvester -d neopets.com -l 300 -b google,bing,yahoo,duckduckgo

    This will return results from google, bing, yahoo and, duckduckgo search engines. 

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/theharvester/theharvester2.png)

As we can see from these results, someone at NeoPets is a Notorious B.I.G. fan!

Additionally, we found some additional subdomains and their IP addresses as well. 

    Step 2:
    Next, I will look for LinkedIn users that have something 
    about neopets.com in their profile.
    
    I ran the following command:

    theHarvester -d neopets.com -l 1000 -b linkedin 

    This command searched LinkedIn using Google for up to the first 1000 
    results where neopets.com was in the user's profile. 

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/theharvester/theharvester4.png)

For the users safety I have blocked out their names. However, you can see that the LinkedIn search returned 298 users that also had neopets.com in their profile. 

**Note:** As with any OSINT results, you should always scrub the results by verifying they are real and applicable to the research you are conducting.

---

### 6. **Summary**

theHarvester is a search tool for finding DNS, subdomains, IP addresses, users, email addresses, and many other open-source intelligence data pieces. 

This tool is excellent for performing reconnaissance during a penetration test.

Additionally, you can use this tool to see what information is on the internet from your organization. 

As always, respect the privacy of those you find through these methods and only use this tool for educational or professional purposes. 

Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
