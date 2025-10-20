# 🌐 Enterprise Network Simulation (Cisco Packet Tracer)

## 📌 Overview
This project represents a simulated enterprise network built in **Cisco Packet Tracer**, demonstrating routing, services, and access control across multiple interconnected subnets. The goal of the project is to design a scalable and secure topology with dynamic routing, network services, traffic control, and remote management.

---

## 🏗️ Topology Summary
The network consists of multiple LAN segments connected through routers running **OSPF** and **RIP v2**, with **route redistribution** between domains. End hosts receive IP configurations from **DHCP**, DNS resolution is enabled, and traffic filtering is enforced using **ACLs**. Remote access to networking devices is enabled through **TELNET**.

> The `.pkt` file contains the complete and working topology.

---

## ✅ Implemented Technologies

| Category | Technology | Status |
|----------|------------|:------:|
| Dynamic Routing | **OSPF (Area 0, Stub, Totally Stubby)** | ✅ |
| Dynamic Routing | **RIP v2** | ✅ |
| Routing | **Route Redistribution (OSPF ↔ RIP)** | ✅ |
| Addressing | **IPv4 Subnetting** | ✅ |
| Addressing | **DHCP Server / Relay** | ✅ |
| Security | **ACL (Access Control Lists)** | ✅ |
| Services | **DNS Server** | ✅ |
| Management | **TELNET Remote Access** | ✅ |

---

## 🌍 Routing Design
- **OSPF Area 0** is used as the backbone
- Additional **stub / totally stubby areas** for reduced routing-table load
- **RIP v2** runs on remote branch networks
- Redistributed routes ensure full end-to-end reachability through both protocols

---

## 📌 Services and Security
| Service | Description |
|---------|------------|
| **DHCP** | Automatically assigns IP, mask, gateway, DNS |
| **DNS** | Resolves domain names to IP addresses |
| **ACL** | Filters and restricts inter-VLAN or inter-site traffic |
| **TELNET** | Allows remote router/switch administration |

---

## 🧪 Test Scenarios (How to Verify)
After opening the project in **Cisco Packet Tracer**, test the following:

| Test | Command / Action | Expected Result |
|--------|------------------|----------------|
| Ping between LANs | `ping <IP>` | ✅ Reachable through OSPF/RIP |
| DNS check | `ping hostname` | ✅ Name gets resolved |
| DHCP check | `ipconfig /renew` | ✅ Client receives correct config |
| ACL check | Blocked subnet ping | ✅ Ping fails as intended |
| TELNET login | `telnet <router-ip>` | ✅ Remote CLI access |

---
