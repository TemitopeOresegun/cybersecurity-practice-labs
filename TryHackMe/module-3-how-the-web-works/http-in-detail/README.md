# 🌐 HTTP in Detail – TryHackMe

## 📌 Overview
This project explores the **HyperText Transfer Protocol (HTTP)** and **HTTPS**, focusing on how communication happens between clients (browsers) and web servers.

It covers request/response structure, methods, status codes, headers, cookies, and practical interaction with web applications.

---

## 🧠 Key Concepts Covered

- HTTP vs HTTPS (secure vs insecure communication)  
- URL structure and components  
- HTTP request and response lifecycle  
- HTTP methods (GET, POST, PUT, DELETE)  
- Status codes and their meanings  
- Headers and cookies  
- Practical request manipulation  

---

## 🔐 HTTP vs HTTPS

- **HTTP** → Not secure (data sent in plain text)  
- **HTTPS** → Secure (encrypted using TLS/SSL)  

### ⚠️ Key Insight:
Browsers display a **“Not Secure” warning or crossed padlock** when a site uses HTTP or has certificate issues.

---

## 🔗 URL Structure

A URL consists of:

scheme://user@host:port/path?query#fragment

### Components:
- **Scheme** → Protocol (http, https)  
- **User** → Optional authentication info  
- **Host** → Domain name  
- **Port** → Communication port  
- **Path** → Resource location  
- **Query String** → Parameters  
- **Fragment** → Page section  

---

## 📤 HTTP Requests

Example:

GET / HTTP/1.1
Host: tryhackme.com
User-Agent: Mozilla/5.0
Referer: https://tryhackme.com

---

## 📥 HTTP Responses

Example:

HTTP/1.1 200 OK
Server: nginx
Content-Type: text/html

<html>...</html> ```

## 🧰 HTTP Methods

GET → Retrieve data
POST → Send data
PUT → Update/create data
DELETE → Remove data

---

## 📊 Status Codes

Code	Meaning
200	OK
201	Created
301	Permanent Redirect
302	Temporary Redirect
400	Bad Request
401	Unauthorized
403	Forbidden
404	Not Found
500	Server Error
503	Service Unavailable

---

## 🧾 Headers & Cookies
Request Headers:
Host
User-Agent
Cookie
Response Headers:
Set-Cookie
Content-Type
Cache-Control

Cookies are commonly used for authentication and session management.

---

## 🧪 Practical Skills Gained
Sending GET, POST, PUT, DELETE requests
Modifying parameters (e.g., id, username)
Understanding request/response flow
Identifying insecure HTTP usage

---

### 🔹 Practical Lab Completion
![Lab Completion](screenshots/http-in-detail.png)


## 🚀 Why This Matters

Essential for web development
Critical for cybersecurity & penetration testing
Helps in debugging web applications
Used in tools like Burp Suite

## 🏁 Conclusion

HTTP is the foundation of web communication. Mastering it is essential for understanding how the web works and identifying security vulnerabilities.

