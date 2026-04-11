
# 🖥️ Virtualisation Basics – Notes

## 📌 Overview
Virtualisation allows one physical computer to run multiple virtual computers. It helps reduce cost, improve efficiency, and make systems easier to scale and manage.

---

## 🏗️ Before Virtualisation

**Old Rule:**
> One physical server = one application

### ❌ Problems:
- Expensive (hardware, power, cooling)
- Wasted resources (low CPU usage)
- Slow to deploy new servers
- Hard to scale

---

## 💡 What is Virtualisation?

Virtualisation lets multiple systems share one physical machine safely.

### Key Idea:
- One physical server
- Multiple virtual machines (VMs)
- Each VM acts like a real computer

---

## ⚙️ Hypervisor

A **hypervisor** is software that manages virtual machines.

### 🧠 What it does:
- Creates virtual machines
- Allocates CPU, RAM, and storage
- Keeps VMs isolated
- Starts, stops, and manages VMs

### 🔢 Types of Hypervisors:

#### Type 1 (Bare Metal)
- Runs directly on hardware
- Faster and more efficient
- Used in production and data centers

#### Type 2 (Hosted)
- Runs on top of an OS
- Easier to install
- Used for learning and testing

### 🛠️ Examples:
- VMware Workstation
- Oracle VM VirtualBox

---

## 🖥️ Virtual Machines (VMs)

A **Virtual Machine (VM)** is a virtual computer.

### ✅ Features:
- Has its own OS
- Has CPU, RAM, storage
- Fully isolated from other VMs

### 📌 Use Cases:
- Running different OS (e.g. Kali Linux)
- Testing software safely
- Malware analysis

---

## 📦 Containers

A **container** is a lightweight environment for running applications.

### 🔍 How it works:
- Shares the host OS kernel
- Includes app + dependencies
- No full OS needed

### ✅ Benefits:
- Fast startup
- Lightweight
- Easy to scale
- Consistent across environments

### ⚠️ Limitation:
- Must match host OS (Linux vs Windows)

### 🛠️ Tool:
- Docker

---

## ⚖️ VM vs Container

| Feature        | Virtual Machine 🖥️ | Container 📦 |
|----------------|------------------|-------------|
| OS Included    | Yes              | No |
| Speed          | Slow             | Fast |
| Resource Usage | Heavy            | Light |
| Isolation      | Strong           | Medium |

---

## 🧠 Key Takeaways

- Virtualisation improves efficiency and reduces cost
- Hypervisors manage virtual machines
- VMs provide full isolation and flexibility
- Containers are faster and lightweight
- Both are important in cloud computing and DevOps

---

## 🚀 Why It Matters

Modern platforms use virtualisation and containers to:
- Scale applications easily
- Deploy faster
- Use hardware efficiently

---

## 📚 Summary

- **Virtualisation** → multiple computers on one machine  
- **Hypervisor** → manages virtual machines  
- **VM** → full virtual computer  
- **Container** → lightweight app environment  

---
