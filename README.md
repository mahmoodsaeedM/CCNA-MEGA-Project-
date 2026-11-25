# Cisco Enterprise Network Infrastructure — CCNA Mega Lab

An end-to-end enterprise network simulation designed, configured, and verified in **Cisco Packet Tracer** as the capstone project for **Jeremy's IT Lab CCNA (200-301)** curriculum.

![Network Topology Overview](./images/topology-overview.png)

---

## 📋 Project Overview

This lab integrates core enterprise networking technologies into a single multi-layer topology, simulating a production branch/campus environment with high availability, segmented Layer 2/Layer 3 domains, hardened switch ports, centralized IP services, and external internet connectivity.

---

## 🛠️ Technologies & Protocols Implemented

### 1. Switching & Layer 2 Architecture
* **VLANs & Trunking:** Segmented departments and management traffic across dedicated VLANs using IEEE **802.1Q** trunking and native VLAN hardening.
* **VTP (VLAN Trunking Protocol):** Configured VTP server/client roles and domain synchronization across distribution and access switches.
* **EtherChannel:** Bundled physical links into logical Port-Channels using **LACP** for increased bandwidth and link redundancy.
* **Spanning Tree:** Configured **Rapid PVST+** with deterministic root bridge placement and PortFast/BPDU Guard on access ports.

### 2. Routing & High Availability
* **Inter-VLAN Routing:** Implemented Router-on-a-Stick (ROAS) and Layer 3 SVI routing between internal subnets.
* **Dynamic Routing (OSPF):** Configured single-area **OSPFv2** with passive interfaces on LAN segments and default route propagation.
* **First-Hop Redundancy (HSRP):** Deployed active/standby gateway redundancy using **HSRP** to ensure seamless failover for end hosts.

### 3. Network Security & Device Hardening
* **Access Control Lists (ACLs):** Applied Standard and Extended IPv4 ACLs to enforce traffic filtering policies and restrict VTY management access.
* **Layer 2 Security:** Hardened access ports with **Port Security** (MAC limiting & violation modes), **DHCP Snooping**, and **Dynamic ARP Inspection (DAI)**.
* **Secure Management:** Disabled Telnet and configured **SSHv2** with local AAA/user authentication, encrypted passwords, and login banners.

### 4. IP Services, Addressing & Wireless
* **IPv4 & IPv6 Dual-Stack:** Designed VLSM IPv4 subnets alongside global unicast IPv6 addressing and routing.
* **Core Infrastructure Services:** Configured centralized **DHCP** pools (with IP helper addresses), **DNS**, **NTP** clock synchronization, **Syslog** logging, **SNMP**, and **FTP**.
* **NAT / PAT:** Configured static NAT for internal servers and PAT (NAT Overload) for internal hosts accessing external networks.
* **Wireless Networking:** Deployed a Wireless LAN Controller (WLC) and lightweight access points (LAPs) mapped to dedicated wireless VLANs.

---

## ✅ Verification & Testing

All configurations were validated across the topology using Cisco IOS CLI verification commands:
* **Connectivity & Routing:** `ping`, `traceroute`, `show ip route`, `show ip ospf neighbor`, `show standby brief`
* **Switching & Redundancy:** `show vlan brief`, `show interfaces trunk`, `show etherchannel summary`, `show spanning-tree`
* **Security & Services:** `show access-lists`, `show port-security`, `show ip dhcp snooping`, `show ip nat translations`

---

## 🚀 How to Run This Lab

1. Download and install **Cisco Packet Tracer** (v8.2 or newer recommended).
2. Clone this repository or download `lab-files/CCNA_Mega_Lab_Completed.pkt`:
   ```bash
   git clone [https://github.com/](https://github.com/)<your-username>/ccna-enterprise-network-mega-lab.git
