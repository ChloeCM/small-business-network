# 🏢 Multi-Site Small Business Network (Cisco Packet Tracer)

Designed and implemented a three-branch small business network in Cisco Packet Tracer connecting Kilkenny (Head Office), Waterford, and Wexford over a WAN. Configured routers with static routing and serial DCE/DTE links, created subnetted LANs with DHCP servers for automatic IP assignment, and set up printers, switches, and PCs for full LAN/WAN communication.

### 📖 Overview
This project simulates a **three-site small business network** connecting:
- **Kilkenny (Head Office)**
- **Waterford (Store B)**
- **Wexford (Store C)**

Each site includes its own **router, switch, PCs, printer, and DHCP server**.  
Routers are connected using serial DCE/DTE links with **static routing**, providing full communication between all offices over a simulated WAN.

---

## 🧩 Network Topology

| Site | Subnet | Default Gateway | DHCP Range | Devices | Max. Number of User |
|------|---------|----------|-------------|----------|
| **Kilkenny (Head Office)** | 192.168.10.0/26 | 192.168.10.1 | 192.168.10.10–59 | 1 Router, 1 Switch, 2 PCs, 1 Printer, 1 Server | 50 |
| **Waterford (Store B)** | 192.168.10.64/26 | 192.168.10.65 | 192.168.10.74–103 | 1 Router, 1 Switch, 2 PCs, 1 Printer, 1 Server | 30 |
| **Wexford (Store C)** | 192.168.10.128/26 | 192.168.10.129 | 192.168.10.138–172 | 1 Router, 1 Switch, 2 PCs, 1 Printer, 1 Server | 35 |

---

### 🌐 WAN Connections
| Link | Network | Mask | Router A | Router B |
|------|----------|------|-----------|-----------|
| Kilkenny ↔ Waterford | 10.0.0.0/30 | 255.255.255.252 | 10.0.0.1 (DCE) | 10.0.0.2 |
| Waterford ↔ Wexford | 10.0.0.4/30 | 255.255.255.252 | 10.0.0.5 | 10.0.0.6 |

Each `/30` subnet provides two usable IP addresses for point-to-point serial connections.

---

## ⚙️ Configuration Summary

### 🖧 Routers
Each router was configured with:
- **LAN interface (GigabitEthernet0/0)** for internal devices  
- **WAN interface (Serial0/0/x)** for inter-router communication  
- **Static routes** to reach other subnets  

