---
title:  "Day 52 - CrackMapExec - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool CrackMapExec and how it works."
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
3 . What is CrackMapExec?
<br>
4 . Why use CrackMapExec?
<br>
5 . How to use CrackMapExec?
<br>
6 . Summary

---

## This post is designed to introduce you to the tool CrackMapExec.

![](PLACEHOLDER_TOOL_PHOTO)

# <span style="color:red">***Disclaimer***</span> : **Please only use CrackMapExec for professional and educational reasons. Do not use this tool for nefarious or malicious reasons.**

---

### 1. **Introduction**

Welcome to the **fifty-second** blog post of 100 tools in 100 days.<br> 

Find **CrackMapExec** @:

GitHub [here](https://github.com/Porchetta-Industries/CrackMapExec).

Porchetta Industries [here](https://porchetta.industries/).

Wiki [here](https://wiki.porchetta.industries/)

CrackMapExec was created by:

[https://github.com/byt3bl33d3r](https://github.com/byt3bl33d3r)

[https://github.com/mpgn](https://github.com/mpgn)


---

### 2. **My Setup**

For running the CrackMapExec tool, I used Kali Linux in a VMware Workstation 16 Player virtualized environment.

For my vulnerable host I am using OpenVPN to connect to the TryHackMe room 'Ra' located here: [https://tryhackme.com/room/ra](https://tryhackme.com/room/ra).

---

### 3. **What is CrackMapExec?**

"CrackMapExec (a.k.a CME) is a post-exploitation tool that helps automate assessing the security of large Active Directory networks. Built with stealth in mind, CME follows the concept of "Living off the Land": abusing built-in Active Directory features/protocols to achieve it's functionality and allowing it to evade most endpoint protection/IDS/IPS solutions." - [Porchetta Industries](https://wiki.porchetta.industries/#:~:text=CrackMapExec%20(a.k,IDS/IPS%20solutions.)

---

### 4. **Why use CrackMapExec?**

CrackMapExec offers an automated suite for security researchers to perform assessments of the security features, privileges, and lack of on active directory or similar networks. 

Today's example will show how to enumerate and discover information about an SMB share on the 'Ra' hard box on TryHackMe. I have already discovered the username and password for this machine (spoiler alert if you have not completed Ra yet).

---

### 5. **How to use CrackMapExec?**

Installing CrackMapExec requires Poetry. The Kali version of CrackMapExec does not function properly and therefore you will need to replace it. 


Poetry Install:

    Step 1 (Install-Poetry):
    Enter the following command in your terminal:

    curl -sSL install.python-poetry.org | python -

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/crackmapexec/crack1.png)

    Step 2 (Install-Poetry):
    Verify poetry installed properly by entering the following command:

    poetry --version

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/crackmapexec/crack2.png)

    Step 3 (Remove-CrackMapExec):
    Uninstall CrackMapExec from Kali by entering the following command:

    sudo apt remove crackmapexec

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/crackmapexec/crack3.png)

    Step 4 (Install-CrackMapExec):
    Enter the following command to clone the files for CrackMapExec:

    git clone https://github.com/Porchetta-Industries/CrackMapExec

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/crackmapexec/crack4.png)

    Step 5 (Install-CrackMapExec):
    Enter the following command to change directory and install CrackMapExec:

    cd CrackMapExec && poetry install

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/crackmapexec/crack5.png)

    Step 6:
    CrackMapExec has a general help option and a specific help option depending on the protocol used. 

    To view general help enter the following command:

    poetry run crackmapexec -h

    To view a specific protocol help specify it like this:

    poetry run crackmapexec smb -h

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/crackmapexec/crack6.png)

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/crackmapexec/crack7.png)

    Step 7:
    First I am going to check if SMB is available on the designated host.
    I know that a Nmap scan likely would have told me that it is indeed 
    available, so this step this far into the process is not necessary.

    Enter the following command:

    poetry run crackmapexec smb <host>

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/crackmapexec/crack8.png)

    Step 8:
    As mentioned in section 4 of this post, I have a username and password that I want to test for validity to connect to the SMB service.

    Add the username and password to the command in step 7 as follows:

    poetry run crackmapexec smb <HOST> -u USERNAME -p PASSWORD

<br>

A teal [+] identifies a successfully authenticated username and password. 

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/crackmapexec/crack9.png)

Since we can authenticate to the SMB let's use CrackMapExec to run some special options such as those listed in the Mapping/Enumeration section of CrackMapExec.

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/crackmapexec/crack10.png)

    Step 9:
    Enter the following command to determine what shares are available on a host:

    poetry run crackmapexec smb <HOST> -u USERNAME -p PASSWORD --shares

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/crackmapexec/crack11.png)

    Step 10:
    Enter the following command to enumerate domain users:

    poetry run crackmapexec smb <HOST> -u USERNAME -p PASSWORD --users

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/crackmapexec/crack12.png)

    Step 11:
    Enter the following command to find and list groups and numbers of members:

    poetry run crackmapexec smb <HOST> -u USERNAME -p PASSWORD --groups

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/crackmapexec/crack13.png)

    Step 12:
    Enter the following command to see what users belong to a group found in step 11:

`poetry run crackmapexec smb <HOST> -u USERNAME -p PASSWORD --group <GROUPNAME>`

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/crackmapexec/crack14.png)

    Step 13:
    Enter the following command to see what the password policy is on the domain:

    poetry run crackmapexec smb <HOST> -u USERNAME -p PASSWORD --pass-pol

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/crackmapexec/crack15.png)

### 6. **Summary**

A security researcher could use CrackMapExec to perform analysis on SMB, LDAP, MSSQL, RDP, SSH, and WINRM services on domain networks. 

CrackMapExec could assist the researcher with finding opportunities for privilege escalation and pivoting within the environment. 

I hope you enjoyed this blog post.

Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
