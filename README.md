# CCNA Mega Lab – Enterprise Network Simulation

This project is a full-scale enterprise network lab based on Jeremy’s IT Lab CCNA Mega Lab. It simulates a multi-site enterprise network with redundancy and scalable design.

---

## 📌 Phase 1 – Initial Device Configuration

This phase establishes baseline configurations across all routers and switches to ensure secure and consistent device management.

### 🔧 Tasks Performed

- Configured hostnames on all routers and switches
- Secured privileged EXEC mode using encrypted enable secrets
- Created local user accounts for authentication
- Enabled console login using local credentials
- Configured console session timeout (30 minutes)
- Enabled synchronous logging for better CLI usability

### 💡 Purpose

- Enforces secure access to network devices
- Standardizes device configuration across the environment
- Prepares devices for remote management and future configurations

---

## 📌 Phase 2 – VLANs & Layer 2 EtherChannel

This phase focuses on network segmentation and link redundancy using VLANs, trunking, and EtherChannel.

### 🔧 Tasks Performed

- Configured Layer 2 EtherChannel:
  - **Office A:** PAgP (Cisco proprietary)
  - **Office B:** LACP (IEEE standard)
- Configured trunk links across Distribution switches
- Disabled DTP and manually set trunking
- Implemented VLAN segmentation across both offices
- Configured VTP domain (`JeremysITLab`)
- Assigned access ports for:
  - PCs
  - Phones (voice VLAN)
  - Servers
- Configured trunks to support required VLANs
- Disabled unused ports for security

### 💡 Purpose

- Provides network segmentation (Users, Voice, Servers, Management)
- Ensures redundancy with EtherChannel
- Reduces broadcast domains
- Prepares network for inter-VLAN routing (next phase)

---

