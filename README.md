# FIFA World Cup Multi-National Network Infrastructure Simulation

An enterprise-level network infrastructure designed and simulated solo in **Cisco Packet Tracer**. This project models a robust, redundant, and highly available network spanning six countries (France, Spain, Germany, Argentina, Brazil, and Portugal) hosting the FIFA World Cup infrastructure.

## 🚀 Key Achievements & Core Architecture

* **Precision VLSM Subnetting:** Manually architected a Variable Length Subnet Masking (VLSM) scheme to efficiently allocate addresses for over 1,100+ end-hosts across various locations, ensuring zero IP address wastage.
* **Intelligent Routing & High Availability:** Implemented hybrid routing protocols using **RIP** for dynamic routing between European sectors and optimized **Static Routing** for South American sectors. 
* **Failover Redundancy:** Configured **Recursive Routing** between Portugal and France to establish an alternate path, guaranteeing continuous packet delivery during a primary link failure.
* **Dynamic IP Management:** Deployed a multi-tiered DHCP infrastructure using centralized servers in France, Argentina, and Brazil alongside **DHCP Relay Agents** in Spain and Germany.

---

## 🗺️ Topology Diagram

*Replace this placeholder with your actual image path once uploaded to GitHub*
![Network Topology](https://github.com/AhsanurRahman787/Fifa-World-Cup-Network/blob/ab3f49ea7f777f33e082ad182be444669f96507d/Screenshot%20From%202026-05-23%2001-04-36.png)

##Project Demo
https://github.com/user-attachments/assets/3c54c696-a48e-4d00-bc3d-c4831876e397

## 🛠️ Technical Specifications & Implementation Details

### 1. Network Requirements & Host Allocation
The network layout satisfies strict capacity constraints optimized via customized subnetting parameters:
* **Portugal:** 300 Hosts
* **Brazil:** 250 Hosts
* **France:** 200 Hosts
* **Argentina:** 200 Hosts
* **Germany:** 150 Hosts
* **Spain:** 100 Hosts

### 2. Protocol Configuration Layer
| Feature / Protocol | Scope / Implementation |
| :--- | :--- |
| **Dynamic Routing** | RIP Protocol running across France, Spain, and Germany hotels to seamlessly share network maps. |
| **Static Routing** | Manually configured routing tables on Argentina and Brazil routers. |
| **Default Routing** | Implemented on Brazil’s edge router to funnel all exterior traffic safely through Argentina. |
| **DHCP Relay Agents** | Configured on Spain, Germany, and Portugal routers to securely forward boot requests to the core servers. |

### 3. Application Services Infrastructure
* **Centralized DNS Server:** Hosted entirely in Argentina, processing domain resolutions for the entire infrastructure.
* **Dedicated Web Servers:** Configured HTTP/HTTPS capacities for accessible nodes (`www.argentina.fifa.com` and `www.france.fifa.com`).
* **Distributed Mail Network:** Individualized SMTP/POP3 Email Servers (`mail.france.com`, `mail.portugal.com`, etc.) deployed locally on every regional network node.

---

## 📂 Repository Structure

```text
├── Topology.png                  # High-resolution network topology schematic
├── FIFA_World_Cup_Network.pkt   # Cisco Packet Tracer source file
├── VLSM_IP and Commands             # Complete breakdown of subnets, gateways, and masks
