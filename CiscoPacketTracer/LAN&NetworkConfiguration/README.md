
# 🖧 LAN & Network Configuration Lab – Packet Tracer

This repository documents hands-on exercises performed in **Cisco Packet Tracer**, focusing on LAN setup, IP addressing, subnetting, DNS integration, and inter-network communication.

---

## 🔹 Lab Objectives

1. Learn proper LAN construction using **PCs, laptops, and switches**.
2. Understand **static IP addressing and subnetting**.
3. Configure a **server and DNS** for hostname resolution.
4. Connect multiple subnets via a **router**.
5. Visualize **packet flow, ARP requests, and routing** in simulation mode.

---

## 🔹 Lab Setup

- **Devices Used:**
  - PCs and Laptops
  - Cisco 2960 Switch
  - Cisco 1941 Router
  - Server (DNS enabled)

- **Tools:**
  - Cisco Packet Tracer (Simulation Mode)

- **Cabling:**
  - **Copper straight-through:** Connect PCs to switch

---

## 🔹 Step 1: LAN Construction

- Devices were connected using **manual and automatic cabling**.
- Observed the importance of **correct cable selection** for reliable connectivity.
- **Key Learning:** Straight-through cabling reinforces proper network design practice.

---

## 🔹 Step 2: Static IP Addressing & Subnetting

- Assigned static IPs to devices, for example:
  - PC1 → `192.168.1.10 /24`
  - PC2 → `192.168.1.11 /24`
- Configured default gateway for proper network routing.
- Verified connectivity using **ping tests** in simulation mode.
- **Key Learning:** Strengthened understanding of subnet masks, gateway configuration, and IP addressing.

---

## 🔹 Step 3: Server & DNS Integration

- Added a server with **IP:** `192.168.1.50`
- Configured DNS to resolve `tsacademy.com`.
- Verified that all devices could successfully resolve the hostname.
- **Key Learning:** DNS is crucial for converting hostnames to IP addresses, enabling seamless communication across the network.

---

## 🔹 Step 4: Connecting Two Networks via Router

- Created two subnets:
  - Subnet 1 → `192.168.1.0/24`
  - Subnet 2 → `192.168.2.0/24`
- Connected via **Cisco 1941 Router** with manual interface configuration.
- Configured **default gateways** on each subnet for cross-network communication.
- Verified connectivity using ping tests.
- **Key Learning:** Routers enable communication between multiple networks by directing traffic appropriately.

---

## 🔹 Step 5: Observation in Simulation Mode

- Used Packet Tracer’s **Simulation Mode** to visualize:
  - ARP requests
  - Packet flow between devices
  - Inter-network routing via router
- **Key Insight:** Understanding real-time packet movement helps solidify theoretical networking concepts.

---

## 💡 Key Takeaways

- Hands-on network configuration is critical for mastering real-world networking concepts.
- Core skills developed:
  - Proper cabling and LAN design
  - Static IP addressing and subnetting
  - DNS server integration
  - Router-based inter-network communication
  - Simulation of packet flow for troubleshooting
