# Cisco Network Configuration Project (Static & RIP Routing)

This project demonstrates a multi-router network topology designed and simulated in **Cisco Packet Tracer**. It showcases the configuration of both **Static Routing** and dynamic **RIP (Routing Information Protocol)** for seamless inter-network communication.

---

## 📸 Network Topology & Evidence

![Network Topology](لقطة%20شاشة%2027-08-2026%20212645.png)

---

## 🌐 Network Specifications

* **Routers:** 3x Cisco 1841 Routers
* **Switches:** 3x Cisco 2960 Switches
* **End Devices:** 3x PCs
* **Subnetting:** Classful `/24` Addressing

| Device | Interface | IP Address | Subnet Mask | Default Gateway |
| :--- | :--- | :--- | :--- | :--- |
| **PC1** | Fa0 | `172.16.3.10` | `255.255.255.0` | `172.16.3.1` |
| **PC2** | Fa0 | `172.16.1.10` | `255.255.255.0` | `172.16.1.1` |
| **PC3** | Fa0 | `192.168.2.10` | `255.255.255.0` | `192.168.2.1` |

---

## ⚙️ Routing Protocols Configured

### 1. Static Routing
Configured using static routes to map specific paths to remote networks:
* **Router1:** Routes directed to `172.16.1.0/24`, `192.168.1.0/24`, and `192.168.2.0/24` via next-hop interface `Serial0/0/0`.
* **Router2 & Router3:** Configured with corresponding return static paths.

### 2. Dynamic Routing (RIP)
Implemented Routing Information Protocol (RIP v1/v2) to automatically advertise directly connected networks across all routers.

---

## 🧪 Testing & Verification

* **Ping Execution:** 100% ICMP success rate achieved between all end-user PCs across different routers (`PC1` ➔ `PC2` ➔ `PC3`).
* **Route Verification:** Validated using `show ip route` command on all routers.
