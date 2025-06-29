# DBSC Global Network Infrastructure

A comprehensive design and simulation of a **secure**, **scalable**, and **resilient** global network for the **Digital Banking Service Company (DBSC)**. This project connects the **Amman HQ** with six **international branches** to ensure reliable communication, data exchange, and access to critical services.

All network design and simulation were built and tested using **Cisco Packet Tracer**.

---

## 🌐 Network Topology Overview

### Global WAN Connectivity
Connects the Amman Data Center to branches in:
- Istanbul
- Riyadh
- Dubai
- London
- Beirut
- Cairo

### Routing
- **OSPF (Open Shortest Path First)** implemented across the entire WAN for dynamic, scalable routing.

### Core Network Services (hosted in Amman HQ)
- **DHCP**: Automatic IP assignment
- **DNS**: Resolves `eis.DBSC.com.jo` to IPs
- **HTTP/HTTPS**: Internal company web portal
- **SMTP/POP3**: Email services
- **FTP**: Secure file transfers

### Topologies
- **WAN**: Hub-and-spoke model with Amman as central hub
- **LAN**: Extended star topology within each branch for easy expansion and fault isolation

---

## 🔐 Security Features
- Router access secured with passwords
- Traffic segregation between sites and functions
- Device access limited by design

---

## 🧠 IP Addressing Schema
- Address space: `172.20.0.0/16`
- Methodology: **VLSM** for efficient IP utilization and growth planning

---

## 🖥️ Branch LAN Architecture
Each office includes:
- Floor-based central switches
- End-user devices: PCs, laptops, printers
- Wireless access via secure access points

_Optional: Insert screenshot of a single branch LAN design here_

---

## 📡 Services & Protocols Summary

| Service        | Protocol(s)     | Port(s) | Purpose                                         |
|----------------|------------------|---------|-------------------------------------------------|
| Web Portal     | HTTP / HTTPS     | 80 / 443 | Secure internal system access                   |
| DNS            | DNS              | 53       | Domain name resolution                         |
| Dynamic IPs    | DHCP             | 67 / 68  | IP auto-assignment                             |
| Email          | SMTP / POP3      | 587 / 110| Internal email management                      |
| File Sharing   | FTP              | 445      | Secure file sharing and transfer               |

---

## 🚀 Getting Started

### Requirements
- Cisco Packet Tracer (version **8.0+**)

### Steps

1. **Download the Project**
   - Clone this repository or download the `.pkt` file

2. **Open in Cisco Packet Tracer**
   - Launch Packet Tracer
   - Open `DBSC_Network.pkt`

3. **Explore and Test the Network**
   - Enter **Simulation Mode** to view data flow
   - Use PC terminals for testing:
     - **Ping a server**  
       `ping 172.20.2.2`
     - **DNS Lookup**  
       `nslookup eis.DBSC.com.jo`
     - **Web Portal Access**  
       Open browser and visit: `https://eis.DBSC.com.jo`
     - **Email & FTP**  
       Test using built-in clients

---

## 📁 Repository Contents
