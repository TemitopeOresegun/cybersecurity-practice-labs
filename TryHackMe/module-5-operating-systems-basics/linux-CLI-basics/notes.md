
# 🐧 Linux CLI Basics — TryHackMe Lab Notes

## 📌 Lab Overview

This lab introduces the fundamentals of using the Linux Command Line Interface (CLI).
You learn how to:

* Navigate the filesystem
* Search for files
* Read file contents
* Gather system information

These are essential skills for cybersecurity and system administration.

---

## 🖥️ What is the Terminal?

The terminal is a text-based interface used to interact with a Linux system.

### 💡 Why it’s important:

* Faster than graphical interfaces
* More control over the system
* Required for many security tools

---

## 🧭 1. File System Navigation

### 🔹 Check Current Directory

```bash
pwd
```

**Output Example:**

```
/home/ubuntu
```

---

### 🔹 List Directory Contents

```bash
ls
```

Detailed view:

```bash
ls -l
```

Include hidden files:

```bash
ls -al
```

📌 Hidden files start with a dot (`.`)

---

### 🔹 Change Directory

```bash
cd Documents
```

Go back one level:

```bash
cd ..
```

---

## 🔍 2. Finding Files

### 🔹 Using `find`

```bash
find <starting_point> -name <filename>
```

### ✅ Example:

```bash
find ~ -name mission_brief.txt
```

---

## 📖 3. Reading Files

### 🔹 Display File Content

```bash
cat mission_brief.txt
```

---

## 🖥️ 4. System Information Gathering

### 🔹 Current User

```bash
whoami
```

---

### 🔹 Kernel & System Info

```bash
uname -a
```

---

### 🔹 Disk Usage

```bash
df -h
```

---

## 📂 5. Exploring System Files

### 🔹 Navigate to `/etc`

```bash
cd /etc
ls
```

---

### 🔹 View OS Information

```bash
cat os-release
```

---

## 🧪 6. Mini Challenge — day1_report.txt

### 🎯 Objective:

Locate and read `day1_report.txt`

---

### 🔹 Step 1: Find File

```bash
find ~ -name day1_report.txt
```

---

### 🔹 Step 2: Navigate

```bash
cd /path/to/file
```

---

### 🔹 Step 3: Confirm File

```bash
ls
```

---

### 🔹 Step 4: Read File

```bash
cat day1_report.txt
```

---

---

## 🧠 Key Commands Summary

| Command    | Purpose                |
| ---------- | ---------------------- |
| `pwd`      | Show current directory |
| `ls`       | List files             |
| `ls -l`    | Detailed list          |
| `ls -al`   | Include hidden files   |
| `cd`       | Change directory       |
| `cd ..`    | Move up one level      |
| `find`     | Search for files       |
| `cat`      | Read file contents     |
| `whoami`   | Show current user      |
| `uname -a` | System info            |
| `df -h`    | Disk usage             |

---

## 🚀 Skills Gained

* Navigating Linux directories
* Searching for hidden files
* Reading important files
* Gathering system information
* Using CLI for problem solving

---

## 🏁 Conclusion

The **Linux CLI Basics** lab builds the foundation for:

* Cybersecurity operations
* Penetration testing
* Linux system administration

Mastering these commands is the first step toward advanced topics like:

* File permissions
* Process management
* Networking
* Security tools

---

**✅ Lab Completed: Linux CLI Basics (TryHackMe)**
