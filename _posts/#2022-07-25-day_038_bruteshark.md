---
title:  "Day 38 - BruteShark - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool BruteShark and how it works."
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
3 . What is BruteShark?
<br>
4 . Why use BruteShark?
<br>
5 . How to use BruteShark?
<br>
6 . Summary

---

## This post is designed to introduce you to the tool BruteShark.

![](https://raw.githubusercontent.com/odedshimon/BruteShark/master/readme_media/BruteSharkBanner.png)

# <span style="color:red">***Disclaimer***</span> : **Please only use BruteShark for professional and educational reasons. Do not use this tool for nefarious or malicious reasons.**

---

### 1. **Introduction**

Welcome to the **thirty-eighth** blog post of 100 tools in 100 days.<br> 

Find **BruteShark** @ GitHub [here](https://github.com/odedshimon/BruteShark).

**BruteShark** was created by Oded Shimon find him on [LinkedIn](https://www.linkedin.com/in/oded-shimon-6ba6721a8/)!

Find Oded Shimon's blog posts on [Medium](https://medium.com/@contact.oded.shimon).
---

### 2. **My Setup**

For running the BruteShark tool, I used Kali Linux in a VMware Workstation 16 Player virtualized environment.

For the sample PCAP files I used the ones provided by Oded on the BruteShark GitHub [here](https://github.com/odedshimon/BruteShark/tree/master/Pcap_Examples).

You can download them using the command:

    svn checkout https://github.com/odedshimon/BruteShark/trunk/Pcap_Examples


---

### 3. **What is BruteShark?**

Directly from Oded Shimon's description:

"BruteShark is a Network Forensic Analysis Tool (NFAT) that performs deep processing and inspection of network traffic (mainly PCAP files, but it also capable of directly live capturing from a network interface). It includes: password extracting, building a network map, reconstruct TCP sessions, extract hashes of encrypted passwords and even convert them to a Hashcat format in order to perform an offline Brute Force attack." -[Oded Shimon](https://github.com/odedshimon/BruteShark#:~:text=BruteShark%20is%20a,Brute%20Force%20attack).

So in other words we can extract files, credentials, build network diagrams, and reconstruct sessions from PCAP files and live capture of network traffic. 

Today I will use only the example PCAP files to perform a file extraction, credential extraction, and network diagram creation. 
 

---

### 4. **Why use BruteShark?**

BruteShark allows a network administrator to analyze traffic for malicious activity, insecure communication methods, weak passwords, and find vulnerabilities in the networking configuration.

A penetration tester may use BruteShark to capture network traffic for offline extraction of credentials, build a network diagram, and extracting files that may leak information. 

---

### 5. **How to use BruteShark?**
Although Kali does offer a version of BruteShark I believe it is outdated so we are going to download the executable directly from Oded Shimon and run the executable manually.


    Step 1:
    Download sample PCAP files from BruteShark GitHub using 
    the following command:

    svn checkout https://github.com/odedshimon/BruteShark/trunk/Pcap_Examples

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/bruteshark/bruteshark1.PNG)

    Step 2:
    Download BruteShark using wget.

`wget https://github.com/odedshimon/BruteShark/releases/latest/download/BruteSharkCli`

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/bruteshark/bruteshark2.PNG)

    Step 3:
    Change permissions to the executable file to make it executable.

    chmod +x BruteSharkCLI

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/bruteshark/bruteshark3.PNG)

    Step 4:
    Checkout the BruteShark help page by entering the following command:

    ./BruteSharkCli --help 

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/bruteshark/bruteshark4.PNG)

    Step 5 (File Extraction):
    I am using the PDF PCAP example: HTTP - PDF file download.pcap
    

    Enter the following command to extract the PDF:

    ./BruteSharkCli -i Pcap_Examples/HTTP\ -\ PDF\ file\ download.pcap -m FileExtracting -o pdf  

<br>

This command output the PDF file into the folder /pdf/Files/ where I could then view and interact with the PDF.

![]()

    Step 6 (Kerberos Hashed Credential Extraction):
    I am using the Kerberos PCAP example: Kerberos-816.pcap

    Enter the following command to extract the Kerberos hashes credentials:

    ./BruteSharkCli -i Pcap_Examples/Kerberos-816.pcap -m Credentials -o kerberos

<br>

This command output the hashes into the folder kerberos/Hashes where I could later crack them offline.

![]()

### 6. **Summary**



I hope you enjoyed this blog post.

Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
