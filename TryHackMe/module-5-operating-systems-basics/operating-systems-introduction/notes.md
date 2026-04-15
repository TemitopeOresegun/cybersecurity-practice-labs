
# 🖥️ Operating Systems: Introduction

## 📌 Overview
An Operating System (OS) is the core software that manages communication between the user, applications, and computer hardware. It acts as the central controller that ensures everything runs smoothly and efficiently.

---

## 🧠 What is an Operating System?

An OS sits between:
- 👤 User  
- 📦 Applications  
- ⚙️ Hardware  

It coordinates all activities on the system, acting as a bridge that allows applications to interact with hardware safely and efficiently.

---

## ✈️ Simple Analogy (Airport System)

Think of a computer like an airport:

| Component        | Role |
|-----------------|------|
| Hardware        | Runways, planes, radar systems |
| Applications    | Airlines and passengers |
| Operating System| Air traffic control system |

➡️ The OS ensures everything runs smoothly without collisions or conflicts.

---

## 🔐 System Privilege Layers

Modern operating systems separate access levels for stability and security.

### 🧩 Kernel Space
- Core part of the OS
- Full access to hardware (CPU, memory, devices)
- Handles critical operations

### 👤 User Space
- Where applications run
- Limited access to system resources
- Must request access via system calls

### 🔁 System Calls
Applications communicate with the kernel through system calls to:
- Read/write files
- Access hardware
- Use network resources

---

## ⚙️ Core Responsibilities of an OS

### 1. 🧵 Process Management
- Creates and manages processes
- Allocates CPU time
- Enables multitasking

**Example:** Running a browser, music player, and terminal at the same time.

---

### 2. 🧠 Memory Management
- Allocates RAM to processes
- Prevents processes from interfering with each other
- Uses virtual memory when RAM is full

---

### 3. 📂 File System Management
- Organizes files and directories
- Handles file permissions and metadata

**Example:**
- Creating folders
- Saving files
- Setting read/write permissions

---

### 4. 👥 User Management
- Handles authentication (login systems)
- Manages user permissions and access levels

---

### 5. 🔌 Device Management
- Uses drivers to communicate with hardware
- Provides abstraction for applications

**Example:** Plugging in a USB device and it works automatically

---

## 🛡️ Operating System Security

The OS provides built-in security mechanisms:

- 🔑 **Authentication** – Verifies user identity (passwords, biometrics)
- 🔒 **Permissions** – Controls access to files and resources
- 📦 **Isolation** – Keeps processes separate
- 🧱 **System Protection** – Prevents unauthorized changes to critical files

---

## 🖱️ OS Interfaces

### 🪟 Graphical User Interface (GUI)
- Visual interaction (icons, windows, menus)
- User-friendly

**Example:** File explorer, settings panel

---

### ⌨️ Command Line Interface (CLI)
- Text-based interaction
- More powerful and precise

**Example commands:**
```bash
ls      # list files
cd      # change directory
pwd     # show current directory

## 🌍 Types of Operating Systems

### 💻 Desktop OS
- Used for personal computers  
- Examples: Windows, macOS, Linux  

### 🖥️ Server OS
- Used in data centers and enterprise environments  
- Focus on stability, performance, and multi-user support  

### 📱 Mobile OS
- Designed for smartphones and tablets  
- Examples: Android, iOS  

### ⚙️ Embedded OS
- Used in routers, smart TVs, IoT devices  
- Lightweight and specialized for specific tasks  

### ☁️ Cloud / Virtual OS
- Used in virtual machines and cloud environments  
- Scalable, lightweight, and optimized for deployment  

---

## 🐧 Linux and Distributions

Linux is not a single operating system but a family of distributions:

- Ubuntu  
- Debian  
- Fedora  
- CentOS  

Each distribution is designed for different use cases such as desktop, server, or security-focused environments.

---

## 🔍 Hands-On Lab Insights (TryHackMe)

### 🧪 Environment
- Ubuntu-based virtual machine  
- Accessed using both GUI and CLI  

### 📊 Activities Performed
- Viewed system information using **"About This Computer"**  
- Explored the Linux file system structure  
- Navigated the Home directory  

---

## 📂 Linux File System (Basic)

| Path   | Description |
|--------|------------|
| `/`    | Root directory (base of the file system) |
| `/home`| User directories |
| `/etc` | Configuration files |
| `/var` | Logs and variable data |
| `/bin` | Essential system binaries |

---

## 💡 Key Takeaways

- The OS is the foundation of all computing systems  
- Privilege separation is critical for security and stability  
- Understanding OS behavior is essential for cybersecurity  
- Practical experience (logs, processes, alerts) becomes clearer with OS knowledge  

---

## 🔗 Real-World Relevance (SOC Perspective)

While working in SOC-style environments:

- OS knowledge helps interpret logs and alerts  
- Understanding processes improves threat detection  
- File system knowledge aids investigations  
- Privilege levels help identify suspicious behavior  

---

## 🏁 Conclusion

An Operating System is more than just software — it is the control layer that governs everything happening on a computer.


