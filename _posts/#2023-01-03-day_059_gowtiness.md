---
title:  "Day 59 - gowitness - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool gowitness and how it works."
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
3 . What is gowitness?
<br>
4 . Why use gowitness?
<br>
5 . How to use gowitness?
<br>
6 . Summary

---

## This post is designed to introduce you to the tool gowitness.

![](https://github.githubassets.com/images/icons/emoji/unicode/1f50d.png)

# <span style="color:red">***Disclaimer***</span> : **Please only use gowitness for professional and educational reasons. Do not use this tool for nefarious or malicious reasons.**

---

### 1. **Introduction**

Welcome to the **fifty-ninth** blog post of 100 tools in 100 days.<br> 

Find **gowitness** @ GitHub [here](https://github.com/sensepost/gowitness).

gowitness was created by SensePost an ethical hacking team at Orange Cyberdefense find them at:

[sensepost.com](https://sensepost.com/)
[twitter](https://twitter.com/sensepost)
[GitHub](https://github.com/sensepost)


---

### 2. **My Setup**

For running the gowitness tool, I used Kali Linux in a VMware Workstation 16 Player virtualized environment.

---

### 3. **What is gowitness?**

Gowitness is a website screenshot tool that was written by the SensePost team at Orange Cyberdefense.  

---

### 4. **Why use gowitness?**

Gowitness can take screenshots, and gather response headers, network logs, security information, and all html from a website, cidr range, nmap file, nessus file and more. 

Gowitness also offers a self hosted database and local website to access this information quickly. 

---

### 5. **How to use gowitness?**

In order to use gowitness you must have Golang installed on your device. Check which version of Golang you have by entering `go version` into your command line. 

<br>

Install gowitness easily using the install option from go.
    
    Step 1:

    go install github.com/sensepost/gowitness@latest

<br>

Verify your installation by checking the gowitness help file:

    Step 2:

    gowitness help

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/gowitness/go1.png)

Next, try using the single option to screenshot a website of your choice. I chose to work with the scanme subdomain from nmap.org. 

    Step 3:

    gowitness single http://scanme.nmap.org

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/gowitness/go2.png)

Now that you have captured the screenshot and data for your website of choice, start the gowitness server to access the web interface for interacting with the data. 

    Step 4:

    gowitness report serve

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/gowitness/go3.png)

Open your browser of choice and navigate to `localhost:7171` and you will see the gowitness report web interface.

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/gowitness/go4.png)

If you click `Table View` you are able to see all of the sites you have scanned and open a report detailing the headers, html data, and security information about the url.

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/gowitness/go5.png)

Below is the data captured by my initial scan:

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/gowitness/go6.png)

Bonus: you can scan individual URLs on demand from the web interface by navigating to `Submit New URL` in the banner options at the top of the page.

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/gowitness/go7.png)

### 6. **Summary**

gowitness is a URL screenshot tool that allows a user to take screenshots of URLs. gowitness captures the headers, security html and additional data from the site specified. 

Advanced uses can input nmap and nessus files as sources for gowitness in order to cover a large amount of sites quickly. 

I hope you enjoyed this blog post.

Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
