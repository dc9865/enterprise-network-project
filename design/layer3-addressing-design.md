# Layer 3 Addressing Design

## Objective
Provide Layer 3 connectivity across core, distribution, and access layers.

---

## Architecture

- Core and distribution switches operate as Layer 3 devices
- Point-to-point routed links between core and distribution
- Layer 3 EtherChannel between CSW1 and CSW2
- Loopbacks used for stable device identification
- VLAN 99 used for access layer management

---

## Core Interconnect (EtherChannel)

- Interfaces: G1/0/2–3
- Mode: PAgP (active)

| Device | Interface      | IP Address   |
|--------|---------------|--------------|
| CSW1   | Port-Channel1 | 10.0.0.41/30 |
| CSW2   | Port-Channel1 | 10.0.0.42/30 |

---

## Routed Links

- Core ↔ Distribution links use /30 subnets
- Each link provides a dedicated point-to-point path

---

## Loopback Interfaces

| Device  | Loopback IP  |
|---------|--------------|
| CSW1    | 10.0.0.77/32 |
| CSW2    | 10.0.0.78/32 |
| DSW-A1  | 10.0.0.79/32 |
| DSW-A2  | 10.0.0.80/32 |
| DSW-B1  | 10.0.0.81/32 |
| DSW-B2  | 10.0.0.82/32 |

---

## R1 Addressing

- G0/0/0, G0/1/0 → DHCP client
- Routed interfaces:
  - 10.0.0.33/30
  - 10.0.0.37/30
- Loopback0: 10.0.0.76/32

---

## Access Layer Management (VLAN 99)

| Switch  | IP Address   |
|---------|--------------|
| ASW-A1  | 10.0.0.4/28  |
| ASW-A2  | 10.0.0.5/28  |
| ASW-A3  | 10.0.0.6/28  |
| ASW-B1  | 10.0.0.20/28 |
| ASW-B2  | 10.0.0.21/28 |
| ASW-B3  | 10.0.0.22/28 |

- Default gateway = first usable IP in subnet

---

## Server Addressing

- SRV1: 10.5.0.4/24
- Default gateway: 10.5.0.1

---

## Design Principles

- /30 subnets preserve addresses
- EtherChannel provides redundancy and load balancing
- Loopbacks provide stable router IDs (OSPF-ready)
- Management traffic isolated via VLAN 99
