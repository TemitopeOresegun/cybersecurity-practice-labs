# Offensive Security Intro - TryHackMe

## Overview
Completed an **Offensive Security** lab on TryHackMe.  
This lab focused on practical attack techniques used in penetration testing and how vulnerabilities in web applications can be discovered and exploited.

Offensive Security, also known as **Red Teaming**, involves simulating attacks to test the security of systems and identify weaknesses before real attackers can exploit them.

---

## Key Concepts Learned
- Introduction to **Offensive Security principles**  
- Enumeration techniques for discovering hidden resources  
- Using the `dirb` tool to find hidden directories and pages  
- Identifying sensitive information such as account numbers  
- Exploiting a vulnerable admin page in a simulated banking environment  

---

## Lab Activity
A simulated **fake bank application** was presented as the target system. The goal was to investigate the application and exploit weaknesses to achieve the lab objective.

### Steps Performed
1. Identified the **target bank account number** within the application  
2. Used the `dirb` command to enumerate hidden directories  
3. Discovered a hidden **/admin page**  
4. Accessed and exploited the admin functionality  
5. Successfully **transferred money** into the simulated bank account  

---

### Dirb Directory Enumeration

![Dirb scan revealing hidden /admin directory](screenshots/dirb-scan.png)

*Using dirb to enumerate hidden directories in the fake bank web application and discovering the /admin page.*

---

## Skills Gained
- Web enumeration and reconnaissance  
- Identifying hidden resources and sensitive data  
- Exploiting insecure admin pages  
- Understanding offensive security workflow and techniques  

---

## Lab Completion
Successfully completed the lab and Flag captured successfully ✅
