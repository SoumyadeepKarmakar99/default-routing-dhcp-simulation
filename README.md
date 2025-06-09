# 🌐 Default Routing with DHCP Integration | Cisco Packet Tracer Project

This project simulates a multi-branch network using **default routing** and **DHCP automation** in **Cisco Packet Tracer**. Three locations—**Kolkata**, **Mumbai**, and **Delhi**—are interconnected using serial WAN links, with internal LAN setups distributing IP addresses via DHCP.

---

## 📌 Project Objectives

- Configure **default routing** between city routers to route unknown traffic through a single next-hop.
- Deploy **DHCP** on each router to assign IPs to LAN devices dynamically.
- Verify full **end-to-end connectivity** among all hosts using routing and DHCP together.
- Demonstrate a simplified **enterprise WAN + LAN** structure using practical commands.

---

## 🧰 Tools & Technologies

- **Cisco Packet Tracer**
- **DHCP Configuration**
- **Default Routing**
- **Serial WAN Interfaces (Se0/1/0, Se0/1/1)**
- **Switches (Cisco 2960)**
- **Routers (Cisco ISR series)**
- **End Devices: PC, Laptop**

---


- **Router Interfaces**:
  - Kolkata: `Se0/1/0` → `200.20.10.1`, LAN: `192.168.10.1`
  - Mumbai: `Se0/1/0`, `Se0/1/1`, LAN: `192.168.20.1`
  - Delhi: `Se0/1/0` → `200.20.20.2`, LAN: `192.168.30.1`

- **DHCP Pools**:
  - Kolkata: `192.168.10.0/24`
  - Mumbai: `192.168.20.0/24`
  - Delhi: `192.168.30.0/24`

---

## ⚙️ Configuration Overview

### ✅ Default Route Example (Kolkata Router):
```bash
ip dhcp pool kolkatapool
 network 192.168.10.0 255.255.255.0
 default-router 192.168.10.1

ip route 0.0.0.0 0.0.0.0 200.20.10.2



