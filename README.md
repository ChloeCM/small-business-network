# 🏢 Multi-Site Small Business Network (Cisco Packet Tracer)

## 📖 Overview
This project simulates a **three-site small business network** connecting:
- **Kilkenny (Head Office)**
- **Waterford (Store B)**
- **Wexford (Store C)**

Each site includes its own **router, switch, PCs, printer, and DHCP server**.  
Routers are connected using serial DCE/DTE links with **static routing**, providing full communication between all offices over a simulated WAN.

---

## 🎯 Project Objective
The goal of this project was to design and configure a realistic small-business network across multiple branches using Cisco Packet Tracer.  
It demonstrates practical networking concepts including subnetting, IP addressing, static routing, DHCP automation, and WAN connectivity.  
Through this project, I strengthened my understanding of how to design, implement, and troubleshoot enterprise-style networks.

---

## 🧩 Network Topology

| Site | Subnet | Default Gateway | DHCP Range | Devices | Max Users |
|------|---------|----------------|-------------|----------|------------|
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

---

## 🧰 Skills Demonstrated
- IPv4 subnetting and address planning  
- Router and switch configuration  
- Static routing and gateway management  
- DHCP server configuration and troubleshooting  
- LAN/WAN cabling (Copper Straight-Through, Serial DCE/DTE)  
- Network testing 
- Cisco Packet Tracer design and documentation

---

## 💡 What I Learned
- How to connect multiple branch networks using WAN serial links  
- The difference between LAN and WAN addressing  
- The role of DHCP servers vs static addressing  
- How to verify connectivity using pings and visual packet flow  
- The importance of consistent subnet planning for scalability

---

## 🚀 Future Improvements
- Implement VLAN segmentation for each department   
- Introduce centralised DNS and file servers  
- Add firewall or access control configurations

---

## 👨‍💻 About Me
I’m a recent Software & IT graduate with strong interest in networking and systems administration.  
I enjoy designing practical, scalable network solutions and using tools like Cisco Packet Tracer to bring theory to life.  
This project reflects my ability to plan, document, and verify real-world network configurations with clear technical communication.




