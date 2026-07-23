# PicoCTF: Old Sessions

**Category:** Web Exploitation  
**Difficulty:** Easy  
**Date Solved:** [2026-07-23]  

---

## 🎯 Objective
The objective of this challenge is to identify a session leakage vulnerability on the web application and hijack the administrator's session to retrieve the hidden flag.

## 🔍 Reconnaissance
Upon navigating to the provided challenge URL (`http://dolphin-cove.picoctf.net:60115/login`), we are presented with the homepage of a small social media platform called "The New Twitter." 

* **Initial Observations:** While exploring the application and reading through the comments section, an interesting message from a user stood out: *"Hey I found a strange page at `/sessions`"*.
* **Tools Used:** `curl`, Python `requests`

> firstly ive login in thriugh testing account 
 >then explored the webpafe through console & view page source 
 > in comments one user commented , /session on current web url is strange 
 > then i visited the url 
 >  then i saw admin COOKIES are leaking in that url 
 > then i replace my current cookirew sessions with the admin cookie 
 > after replacing my got access to the admin panel 
