---
title:  "Day 12 - Instaloader - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool Instaloader and how it works."
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
3 . What is Instaloader?
<br>
4 . Why use Instaloader?
<br>
5 . How to use Instaloader?
<br>
6 . Summary

---

## This post is designed to introduce you to the tool Instaloader.

![](https://raw.githubusercontent.com/instaloader/instaloader/master/docs/logo_heading.png)

---

### 1. **Introduction**

Welcome to the **twelfth** blog post of 100 tools in 100 days.<br> 


Instaloader is created and maintained by Alexander Graf. If you want to support Alexander please follow this [link](https://github.com/sponsors/aandergr).

Find **Instaloader** [here](https://github.com/instaloader/instaloader).

Connect with Alexander Graf here.

---

### 2. **My Setup**

For running the Instaloader tool, I used Kali Linux in a VMware Workstation 16 Player virtualized environment.

---

### 3. **What is Instaloader?**

What if I told you that you could download all of the data from a profile on Instagram with a simple tool? 

When I say all of the data I mean everything. Photos, videos, profile contents, stories, your own feed, saved posts, you get the idea, everything!

That is exactly what Instaloader does for you!

It is customizable to the point that you can tell Instaloader to download only public posts that have certain hashtags.

You could even tell Instaloader to download all posts from a location id that Instagram uses.

The possibilities for the information you can retrieve are nearly unlimited. 

# <span style="color:red">***Disclaimer***</span>: **Please only use Instaloader for professional and educational reasons. Do not use this tool for nefarious or malicious reasons.**

---

### 4. **Why use Instaloader?**

Instaloader is an excellent way to download all of your personal post history for archival purposes.

Instaloader is a great tool for OSINT collection from a penetration testers' perspective. 

You can filter down the exact information variables you need. 

You can schedule a Cronjob to automatically run Instaloader to create your own Instagram archive. 

I want to pause here for a brief moment. Individuals will probably think that this is a tool that crosses the line for personal privacy. I want to remind those individuals that this only works on public profiles and private profiles that follow a user. So if an individual is worried about privacy, just know this tool does exist and what you place on the internet is not private despite the "privacy options" a social media solution may provide. 

---

### 5. **How to use Instaloader?**

    Step 1:
    Install instaloader if it is not already on your Linux machine.

    Note: You will need Python and pip to install instaloader.

<br>

Install pip following these directions: https://pip.pypa.io/en/stable/installation/

    Run the following command as root:

    pip3 install instaloader
    
<br>

    Step 2:
    Find a username you want to archive data from. I am using the official 
    Instagram's Instagram page located at:
    https://www.instagram.com/instagram/

    They have a username of:

    instagram

<br>

    Step 3:
    Use instaloader to collect the images, videos, metadata, geotags, comments, etc.

    I wanted to collect the basic information that I could from the 
    Instagram's instagram page. 

    I ran the following command:

    instaloader profile instagram

    Note: I ran it originally with the geotags option, but I am not logged 
    in so that did not work. 
<br>

**Whoa!** I was honestly a bit surprised at just how easy it is to grab the information from public instagrams. If I logged in I would have access to even more information retrieval.

Below you can see I downloaded 11 posts from the instagram page.

The information included: all of the posts media, the posts captions, and the json associated with each post day.

Note how many requests instaloader was going to complete 7164, the same amount of posts on the instagram page. In a matter of minutes, I could have downloaded every aspect of Instagram's instagram page and had that information as my own archive. 

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/instaloader/instaloader1.PNG)

Below you can see the top 6 most recent instagram posts on the instagram.

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/instaloader/instaloader2.PNG)

To confirm that those 6 posts' media and captions were downloaded I have a screenshot below of the folder containing the downloads from my request below.

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/instaloader/instaloader4.PNG)

Finally, I wanted to look at the first post on Instagram and see if it grabbed the photo, video, and caption, and Instaloader did! Below are all three files opened.

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/instaloader/instaloader3.PNG)

---

### 6. **Summary**

The greatest takeaway from this tool is this:

If you have information online and it is not private it is accessible by anyone. 

If your information is private, even then it could still be accessible. 

In summary, practice safe internet use and sanitize what you post and talk about online. 


Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
