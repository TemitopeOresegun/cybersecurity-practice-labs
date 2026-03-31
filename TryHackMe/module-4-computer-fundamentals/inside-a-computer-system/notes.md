
```markdown
# 🖥️ Inside a Computer System – TryHackMe Lab Notes

## 📌 Overview
In this lab, we explored the **core components of a computer system** and how a computer **boots up**. These concepts are foundational and will be important as we progress into cybersecurity topics.

---

## 🧩 Core Components of a Computer System

### 1. **CPU (Central Processing Unit)**
- Known as the **brain of the computer**
- Executes instructions from programs
- Performs calculations and decision-making tasks

---

### 2. **RAM (Random Access Memory)**
- Temporary memory used while the system is running
- Stores data that the CPU needs quickly
- Data is lost when the system is powered off (volatile memory)

---

### 3. **Storage (HDD/SSD)**
- Permanent storage for the operating system, files, and applications
- Retains data even when the computer is turned off (non-volatile)
- Examples: Hard Disk Drive (HDD), Solid State Drive (SSD)

---

### 4. **Motherboard**
- The main circuit board that connects all components
- Allows communication between CPU, RAM, storage, and other hardware

---

### 5. **Power Supply Unit (PSU)**
- Converts electricity from the wall into usable power for the computer
- Supplies power to all internal components

---

### 6. **Input/Output Devices**
- Input: Keyboard, mouse (used to interact with the system)
- Output: Monitor, speakers (used to display results)

---

## ⚙️ The Boot Process (Startup Sequence)

The **boot process** is how a computer starts up and loads the operating system.

### 🔄 Steps in the Boot Process:

1. **Power On**
   - Power supply sends electricity to all components

2. **BIOS/UEFI Initialization**
   - Firmware (BIOS or UEFI) starts up
   - Performs POST (Power-On Self-Test) to check hardware

3. **Bootloader Execution**
   - BIOS/UEFI looks for a bootable device (HDD/SSD/USB)
   - Loads the bootloader (e.g., GRUB)

4. **Operating System Loading**
   - Bootloader loads the operating system kernel into RAM

5. **System Initialization**
   - OS starts services and processes
   - User is presented with login screen or desktop

---

## 🔐 Cybersecurity Relevance

- Understanding system components helps in:
  - Identifying hardware-related vulnerabilities
  - Troubleshooting system issues
  - Analyzing malware behavior

- The **boot process is a target for attackers**:
  - Bootkits and rootkits can infect early startup stages
  - Attackers may modify the bootloader or firmware to gain persistence

---

## 💡 Key Takeaways

- Every component in a computer system has a specific role
- Components work together to execute tasks efficiently
- The boot process is critical and can be exploited if not secured
- Strong foundational knowledge is essential for advanced cybersecurity topics

---

## 🧠 Notes to Remember

> You may not fully realize the importance now, but these concepts will become very useful when analyzing attacks, investigating incidents, and understanding how systems are compromised.

---
```
