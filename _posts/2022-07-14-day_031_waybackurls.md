---
title:  "Day 31 - waybackurls - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool waybackurls and how it works."
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
3 . What is waybackurls?
<br>
4 . Why use waybackurls?
<br>
5 . How to use waybackurls?
<br>
6 . Summary

---

## This post is designed to introduce you to the tool waybackurls.

![](https://raw.githubusercontent.com/marco-lancini/waybackurls/master/.github/goscan_logo.png)

# <span style="color:red">***Disclaimer***</span> : **Please only use waybackurls for professional and educational reasons. Do not use this tool for nefarious or malicious reasons.**

---

### 1. **Introduction**

Welcome to the **thirty-first** blog post of 100 tools in 100 days.<br> 

Find **waybackurls** [here](https://github.com/tomnomnom/waybackurls).

Tom Hudson created waybackurls, and a bunch of other cool tools you will see in future posts. 

Find Tom Hudson here:

[GitHub](https://github.com/tomnomnom)

[LinkedIn](https://www.linkedin.com/in/tom-hudson-01816822/)

[Slightly Outdated Website](https://tomnomnom.com/)


---

### 2. **My Setup**

For running the waybackurls tool, I used Kali Linux in a VMware Workstation 16 Player virtualized environment.

---

### 3. **What is waybackurls?**

waybackurls is a tool for grabbing URLs from the Internet Archives Way Back Machine. You can find the Way Back Machine [here](https://archive.org/web/).


---

### 4. **Why use waybackurls?**

Finding old domains is usually a form of reconnaissance for any penetration tester. Using waybackurls a tester could grab all of the URLs from waybackmachine with a simple command. 

The tester could output the URLs into a file where further sorting and analysis could be performed to find information from less current sections of the website. 

---

### 5. **How to use waybackurls?**

waybackurls is written in the Go language and uses the go install feature for downloading and installing.

If you do not have Go installed or do not have your variables set up for running go binaries perform Step 0 first.

    Step 0 (a):
    Run the following command to install Go:

    sudo apt install -y golang

<br>

    Step 0 (b):
    Next, update your .zshrc file (the file used for Kali, if you are not 
    using .zshrc then update .bashrc). Type the following:

    sudo nano ~/.zshrc

    Press the down arrow to your export section and add the following:

    export GOROOT=/usr/lib/go
    export GOPATH=$HOME/go
    export PATH=$GOPATH/bin:$GOROOT/bin:$PATH

    Press Ctrl+X
    Type: Y
    Press: Enter
<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/waybackurls/waybackurls0b.PNG)

    Step 0 (c):
    Update your source file for your current shell by typing the following into your terminal:

    source ~/.zshrc

<br>

    Step 1:
    To verify GO was installed, in terminal type:

    go version

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/waybackurls/waybackurls2.PNG)

    Step 2:
    Install waybackurls with the following command:

    go install github.com/tomnomnom/waybackurls@latest

<br>

You should be able to use the command `waybackurls` at this point. 
If you cannot, a temporary fix is to run the binary from its path which is:
`/home/YOURUSERNAME/go/bin/waybackurls`

    Step 3:
    For this demonstration, I am going to use the domain: neopets.com and 
    output the URLs into a file named neopets. Here is the command:

    waybackurls neopets.com > neopets

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/waybackurls/waybackurls3.PNG)

waybackurls was able to pull 14798 URLs into the file neopets!
That is a lot of URLs to analyze. 

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/waybackurls/waybackurls4.PNG)

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/waybackurls/neopets.gif)

With this information, a tester or analyst could use other various Linux commands to filter out information, or they could input this file into a data analysis tool to look for specific items of interest.


### 6. **Summary**

waybackurls is a simple URL grabber for the Way Back Machine written in the Go Language by Tom Hudson. Check out Tom's GitHub [here](https://github.com/tomnomnom).

A penetration tester may use waybackurls to find information during reconnaissance that may help during the test.

An analyst may use waybackurls to interact with less updated versions of a website to find security issues. 

I hope you enjoyed this blog post.

Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
