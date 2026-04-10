
# Client-Server Basics (TryHackMe Lab)

## Overview
This lab introduced the fundamentals of how computers communicate over the internet using the client-server model.

---

## Client-Server Model
- A **client** sends a request  
- A **server** processes the request and sends back a response  
- The client always initiates communication  

### Simple Analogy 🍕
Ordering pizza:
- You = Client  
- Pizza shop = Server  
- You send an order → Shop prepares and sends it back  

---

## HTTP(S) Basics
HTTP(S) is the protocol used for communication on the web.

### Key Points:
- It is **stateless** → every request is treated as new  
- The server does not remember previous requests  
- Websites use **cookies and sessions** to maintain user state  

---

## HTTP Methods
These define what action the client wants to perform:

- GET → Retrieve data  
- POST → Send data  
- PUT → Update data  
- DELETE → Remove data  
- PATCH → Modify data  
- HEAD → Get headers only  
- OPTIONS → Check supported methods  
- CONNECT → Establish connection  
- TRACE → Debug request  

---

## Other Important Concepts

### DNS (Domain Name System)
- Translates domain names into IP addresses  
- Example: google.com → IP address  

### Ports
- Identify specific services on a server  
- Different services run on different ports  

### Protocols
- Rules that define how communication happens between client and server  

---

## Key Takeaway 💡
Understanding how client-server communication works is essential for both **networking** and **cybersecurity**.  
Even simple web browsing involves multiple processes working together behind the scenes.

---

## Reflection 🚀
This lab made it easier to understand what happens when we visit a website.  
It’s a strong foundation for learning more about networking and security.
