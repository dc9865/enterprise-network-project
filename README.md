# CCNA Mega Lab – Enterprise Network Simulation

This project is a full-scale enterprise network simulation based on Jeremy’s IT Lab Mega Lab.  
It models a **multi-site enterprise architecture** with redundant Layer 2/Layer 3 design, segmentation, and high availability mechanisms.

The goal of this project is not only to implement configurations, but to **demonstrate real-world network design, validation, and troubleshooting practices**.

---

## 🏗️ Project Overview

- Multi-site topology (Office A / Office B)
- Hierarchical design:
  - Core Layer (CSW1 / CSW2)
  - Distribution Layer (DSW-A / DSW-B)
  - Access Layer (ASW)
- Redundant links across all layers
- Wireless + wired client integration

---

## 🌐 Topology

![Network Topology](topology/topology.png)

> Includes dual-core design, redundant distribution switches, EtherChannel links, and segmented VLAN architecture.

---

## 🚀 Key Features Implemented

- VLAN segmentation for traffic isolation
- Trunking for inter-switch VLAN propagation
- EtherChannel (PAgP + LACP) for redundancy and load balancing
- VTP for centralized VLAN management
- Inter-VLAN routing (later phases)
- First-hop redundancy using HSRP (later phases)
- Rapid Spanning Tree Protocol (RSTP) for loop prevention
- Layer 2 security (port shutdown, DTP disabled)

---

## 🧠 What I Implemented

Instead of following step-by-step instructions, the network was configured with the following design goals:

- Segmented user, voice, server, and management traffic using VLANs
- Built redundant uplinks using EtherChannel to eliminate single points of failure
- Standardized trunk configurations across all inter-switch links
- Implemented VTP to ensure VLAN consistency across distribution and access layers
- Applied secure baseline configurations across all network devices
- Disabled unused interfaces to reduce attack surface

---

# 📌 Phase 1 – Device Baseline Configuration

## Objective
Establish a secure and consistent configuration baseline across all routers and switches.

## Implementation

- Hostnames assigned based on topology roles
- Encrypted enable secret configured
- Local authentication database created
- Console access secured using local login
- Idle timeout enforced (30 minutes)
- CLI usability improved using synchronous logging

## Why This Matters

This ensures:
- Controlled administrative access
- Consistent device behavior across the network
- Readiness for future remote management (SSH, AAA)

---

# 📌 Phase 2 – VLAN Segmentation & EtherChannel

## Objective
Design a scalable Layer 2 network with segmentation and redundancy.

## Implementation

### VLAN Design

| VLAN | Purpose        |
|------|--------------|
| 10   | User Devices |
| 20   | Voice        |
| 30   | Servers (Office B) |
| 40   | Wireless     |
| 99   | Management   |

### Key Configurations

- VLANs created and propagated using VTP (Domain: `JeremysITLab`)
- Access ports assigned per device type (PC, Phone, AP, Server)
- Voice VLAN configured for IP phones
- Trunk links manually configured (`switchport mode trunk`)
- DTP disabled on all trunk links

### EtherChannel Design

| Location | Protocol | Purpose |
|----------|--------|--------|
| Office A | PAgP   | Cisco-specific redundancy |
| Office B | LACP   | Industry-standard redundancy |

- Distribution switches connected via Port-Channel
- Load balancing + failover achieved

## Why This Matters

- Reduces broadcast domains → improves performance
- Provides redundancy → prevents outages
- Enables scalable network growth

---

# 📌 Validation (CRITICAL)

The network was validated using standard operational commands:

```bash
show vlan brief
show interfaces trunk
show etherchannel summary
show mac address-table
