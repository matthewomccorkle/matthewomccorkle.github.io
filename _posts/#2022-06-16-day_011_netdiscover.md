---
title:  "Day 11 - Netdiscover - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool Netdiscover and how it works."
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
3 . What is Netdiscover?
<br>
4 . Why use Netdiscover?
<br>
5 . How to use Netdiscover?
<br>
6 . Summary

---

## This post is designed to introduce you to the tool Netdiscover.

![](https://www.kali.org/tools/netdiscover/images/netdiscover-logo.svg)

---

### 1. **Introduction**

Welcome to the **eleventh** blog post of 100 tools in 100 days.<br> 


Find **Netdiscover** [here](https://github.com/netdiscover-scanner/netdiscover).

Additionally, Netdiscover comes as one of the tools in Kali Linux.

---

### 2. **My Setup**

For running the Netdiscover tool, I used Kali Linux in a VMware Workstation 16 Player virtualized environment.

Additionally, to detect other devices I ran a Metasploitable2 instance in a VMware Workstation 16 Player virtualized environment. 

---

### 3. **What is Netdiscover?**

Netdiscover is a network enumeration tool which allows a user to quickly discover hosts and MAC addresses quickly on networks.

Netdiscover is quite simple to use with few additional options and therefore makes it a simple and lightweight host detection device. 

Netdiscover allows ARP scanning as well as stealth mode without sending ARP packets. 

---

### 4. **Why use Netdiscover?**

I would use Netdiscover in the event I want to identify hosts and associated MAC addresses quickly. 

Netdiscover is extremely fast and simple to use, I would use Netdiscover when I only need hosts / MAC addresses and not further scan details. If I needed a deeper and different scan I would ofcourse default to using Nmap, which will be in a future blog post!

---

### 5. **How to use Netdiscover?**

**Note**: You may need to run Netdiscover with root permissions (sudo).

    Step 1:
    Netdiscover is really simple to use.

    In your terminal type:

    netdiscover -r <IPaddress/cidr>

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/netdiscover/netdiscover1.PNG)

<br>

Netdiscover is fast, my scan only has 1 host which is the metasploitable 2 environment. 

Overall my scan took less than 5 seconds to complete.

Below are the results:

![]()




---

### 6. **Summary**



Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
