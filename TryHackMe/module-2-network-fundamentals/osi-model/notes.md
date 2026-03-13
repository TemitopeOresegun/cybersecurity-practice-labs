# OSI Model (Open Systems Interconnection) - TryHackMe Lab Notes

## Overview
This lab introduced the **OSI (Open Systems Interconnection) Model**, which provides a framework that explains how networked devices **send, receive and interpret data across a network**.

The OSI model is used as a **conceptual guide** in networking and cybersecurity to understand how communication occurs between devices and how problems in networks can be identified.

The model is divided into **7 layers**, each responsible for a specific part of the communication process.

---

## The 7 Layers of the OSI Model

### 1. Physical Layer
The **Physical Layer** is the lowest layer of the OSI model.

It is responsible for the **physical transmission of data** between devices using electrical, radio or optical signals.

Data at this level is represented in **binary format (1s and 0s)**.

Examples include:
- Ethernet cables
- Fiber optic cables
- Wireless signals

---

### 2. Data Link Layer
The **Data Link Layer** focuses on **physical addressing** and communication between devices on the same network.

Each device on a network contains a **Network Interface Card (NIC)**, which has a **unique MAC address** used to identify it.

Responsibilities include:
- MAC addressing
- Error detection
- Frame formatting

---

### 3. Network Layer
The **Network Layer** is responsible for **routing data between networks**.

This layer determines the **best path for data to travel** from source to destination.

Routing decisions are based on factors such as:
- Shortest path
- Most reliable route
- Fastest physical connection

Protocols used in this layer include:
- **OSPF (Open Shortest Path First)**
- **RIP (Routing Information Protocol)**

At this layer, communication is handled using **IP addresses**.

---

### 4. Transport Layer
The **Transport Layer** ensures that data is delivered **reliably and in the correct order** between devices.

It controls:
- Data segmentation
- Flow control
- Error recovery

Two major protocols operate at this layer:

**TCP (Transmission Control Protocol)**
- Reliable connection-based communication
- Ensures packets arrive in order
- Slower but more reliable

**UDP (User Datagram Protocol)**
- Faster but less reliable
- No guarantee of packet delivery
- Used for streaming or real-time communication

---

### 5. Session Layer
The **Session Layer** manages **connections between computers**.

Its responsibilities include:
- Creating communication sessions
- Maintaining active connections
- Closing sessions when communication ends or becomes inactive

It also contains **checkpoints**, allowing communication to resume if the connection is interrupted.

Data can only travel during an **active session**.

---

### 6. Presentation Layer
The **Presentation Layer** acts as a **translator for data** between the network and applications.

Its functions include:
- Data formatting
- Data compression
- Data encryption

Security mechanisms such as **HTTPS encryption** occur at this layer.

---

### 7. Application Layer
The **Application Layer** is the **closest layer to the user**.

It provides protocols and services that allow applications to communicate over a network.

Examples include:
- Email clients
- Web browsers
- File transfer applications

Protocols at this layer include:
- **DNS (Domain Name System)** – translates domain names into IP addresses
- HTTP / HTTPS
- FTP

These applications provide a **Graphical User Interface (GUI)** that allows users to interact with data being sent and received.

---

## Encapsulation
The process of sending data through the OSI layers is known as **Encapsulation**.

During encapsulation:
1. Data moves **down the OSI layers** from Application to Physical.
2. Each layer **adds its own header information** to the data.
3. The data is transmitted across the network.
4. The receiving device **removes the headers layer by layer** to retrieve the original data.

This process ensures that data can be properly **transmitted, routed and interpreted** between devices.

---

## Lab Activity
In the TryHackMe lab, an interactive activity was used to reinforce the OSI model concepts.

A **game simulation** required navigating through **doors representing each of the seven OSI layers**.  
The objective was to **enter the doors in the correct order based on the OSI model**.

This activity helped reinforce the **structure and sequence of the OSI layers** in a fun and practical way.

---

## Summary
This lab introduced the **OSI Model and its importance in networking and cybersecurity**.

Key takeaways include:

- The OSI model consists of **7 layers** that define how network communication occurs.
- Each layer performs a **specific function in data transmission**.
- Protocols such as **TCP, UDP, DNS, OSPF, and RIP** operate within different layers.
- **Encapsulation** allows data to pass through these layers during transmission.
- Understanding the OSI model is essential for **network troubleshooting, security analysis and penetration testing**.
