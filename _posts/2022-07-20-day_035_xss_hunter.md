---
title:  "Day 35 - XSS Hunter - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool XSS Hunter and how it works."
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
3 . What is XSS Hunter?
<br>
4 . Why use XSS Hunter?
<br>
5 . How to use XSS Hunter?
<br>
6 . Summary

---

## This post is designed to introduce you to the tool XSS Hunter.

![](https://raw.githubusercontent.com/mandatoryprogrammer/mandatoryprogrammer/main/cyberpunk.gif)

# <span style="color:red">***Disclaimer***</span> : **Please only use XSS Hunter for professional and educational reasons. Do not use this tool for nefarious or malicious reasons.**

---

### 1. **Introduction**

Welcome to the **thirty-fifth** blog post of 100 tools in 100 days.<br> 

Find **XSS Hunter** @ xsshunter.com [here](https://xsshunter.com/).

Find **XSS Hunter Express** @ GitHub [here](https://github.com/mandatoryprogrammer/xsshunter-express).

Find **Matthew Bryant** @ GitHub [here](https://github.com/mandatoryprogrammer).

Connect with **Matthew Bryant** @ Twitter [here](https://twitter.com/iammandatory?lang=en).

---

### 2. **My Setup**

I used the web version of the XSS Hunter tool located at [xsshunter.com](https://xsshunter.com/).

For my vulnerable host, I am using the Metasploitable 2 instance running in a VMWare Workstation 16 Player virtualized environment. 

---

### 3. **What is XSS Hunter?**

XSS Hunter is a web based automatic XSS payload generator and tester. 

---

### 4. **Why use XSS Hunter?**

The Open Web Application Security Project (OWASP) lists cross-site scripting in the top ten security issues on the web as #3 [source](https://owasp.org/www-project-top-ten/).

Security researchers, penetration testers, developers, bug bounty hunters, etc. often look for cross-site scripting vulnerabilities on web apps. 

XSS Hunter allows for quick and easy payload generation using a custom domain aligned with your XSS Hunter account. Every time you use an XSS hunter payload is triggered, the web application captures a screenshot of the vulnerable site and other information to document the vulnerability.

Additionally, a user can set up XSS Hunter Express on their own device and host their own site with payloads for use with XSS Hunter.

---

### 5. **How to use XSS Hunter?**

For my example I am using the XSS Hunter web version to submit an XSS payload to my Metasploitable 2 Damn Vulnerable Web Application (DVWA), I have turned security down to low on DVWA to ensure the XSS attempt works for this example. 

Sign up for your XSS Hunter account here: [https://xsshunter.com/signup](https://xsshunter.com/signup)


    Step 1:

    Navigate to the Payloads section of the website and choose a payload to test.

    I chose the basic XSS payload as I know that it will work on the DVWA. 

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/xss_hunter/xsshunter1.PNG)

    Step 2:
    Submit the payload into the input you are testing for cross-site scripting.

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/xss_hunter/xsshunter2.PNG)

    Step 3:
    On the XSS Hunter website, you will see the XSS Fires load the detected 
    vulnerability and create a report for understanding. 

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/xss_hunter/xsshunter3.PNG)

    Step 4:
    The report can be viewed for details that show how the XSS occurred and some best practices to safeguard from it. 

    Additionally, the website allows the user to generate a report in Markdown which is extremely convenient for many application uses. 

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/xss_hunter/xsshunter4.PNG)

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/xss_hunter/xsshunter5.PNG)

### 6. **Summary**

If you are a security researcher, defender, or tester you should consider using the entire suite of XSS Hunter to produce custom payloads for your testing purposes. 

XSS Hunter allows for organization of XSS successful attempts and generates reports for evidence and understanding. 

I hope you enjoyed this blog post.

Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
