# Layer 3 Addressing Design

## Objective
Introduce Layer 3 connectivity across the enterprise topology using routed interfaces, loopbacks, and management addressing.

---

## Scope

This phase includes:

- Router (R1) interface addressing
- Enabling Layer 3 routing on core and distribution switches
- Layer 3 EtherChannel between CSW1 and CSW2
- Point-to-point routed links between core and distribution switches
- Loopback interface assignments
- Management IP addressing for access switches (VLAN 99)
- Static IP configuration for SRV1

---

## Core Design Components

### 1. Routed Core Architecture

All core and distribution switches were converted to Layer 3 devices by enabling IPv4 routing.

This allows:
- Inter-device routing without relying on Layer 2 extension
- Smaller failure domains
- Better scalability

---

### 2. Layer 3 EtherChannel (Core Interconnect)

An EtherChannel was formed between CSW1 and CSW2 using:

- Interfaces: G1/0/2 and G1/0/3  
- Mode: Cisco-proprietary (PAgP active)

Port-channel configuration:

| Device | Interface       | IP Address     |
|--------|----------------|----------------|
| CSW1   | Port-Channel1  | 10.0.0.41/30   |
| CSW2   | Port-Channel1  | 10.0.0.42/30   |

#### Why this matters
- Provides redundancy between core switches
- Enables load balancing
- Prevents single link failure impact

---

### 3. Point-to-Point Routed Links

All core-to-distribution connections use /30 subnets.

Example:
- CSW ↔ DSW links use dedicated point-to-point addressing

#### Why /30?
- Minimizes IP waste
- Clearly defines two endpoints
- Standard enterprise design practice

---

### 4. Loopback Interfaces

Loopbacks were configured on:

- CSW1 → 10.0.0.77/32  
- CSW2 → 10.0.0.78/32  
- DSW-A1 → 10.0.0.79/32  
- DSW-A2 → 10.0.0.80/32  
- DSW-B1 → 10.0.0.81/32  
- DSW-B2 → 10.0.0.82/32  

#### Purpose
- Stable logical identifiers
- Useful for testing routing protocols (ie.OSPF)

---

### 5. Router (R1) Addressing

R1 was configured with:

- DHCP client on G0/0 and G0/1
- Routed interfaces:
  - 10.0.0.33/30
  - 10.0.0.37/30
- Loopback:
  - 10.0.0.76/32

#### Purpose
- Provides upstream connectivity toward external networks
- Acts as edge router

---

### 6. Access Layer Management (VLAN 99)

Each access switch was assigned an SVI in VLAN 99:

| Switch  | IP Address     |
|--------|----------------|
| ASW-A1 | 10.0.0.4/28    |
| ASW-A2 | 10.0.0.5/28    |
| ASW-A3 | 10.0.0.6/28    |
| ASW-B1 | 10.0.0.20/28   |
| ASW-B2 | 10.0.0.21/28   |
| ASW-B3 | 10.0.0.22/28   |

Default gateway:
- First usable IP in each management subnet

#### Why this matters
- Enables remote management of switches
- Separates management traffic from user traffic

---

### 7. Server Addressing (SRV1)

SRV1 was manually configured:

- IP Address: 10.5.0.4  
- Subnet Mask: 255.255.255.0  
- Default Gateway: 10.5.0.1  

#### Purpose
- Provides stable addressing for services
- Avoids dependency on DHCP

---

## Design Principles

- Routed access between layers (Layer 3 boundaries)
- Redundancy via EtherChannel
- Minimal subnet sizing (/30)
- Separation of management plane (VLAN 99)
- Use of loopbacks for stability
