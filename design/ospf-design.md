# OSPF Design

## Objective
Enable dynamic routing across all Layer 3 devices and provide full network reachability. 

---

## Scope

- OSPF enabled on R1, Core, and Distribution switches
- All Layer 3 interfaces included
- Loopbacks advertised
- Static default route redistributed by R1

---

## OSPF Configuration Model

- Process ID: 1
- Area: 0 (single-area design)

---

## Router ID Strategy

Each device uses its loopback IP as Router ID.

---

## Interface Design

- All Layer 3 interfaces included using exact network statements
- Loopback interfaces:
  - Advertised
  - Set as passive

- Distribution SVIs (except management):
  - Passive interfaces

---

## Neighbor Relationships

- All physical links between routers form OSPF adjacencies
- Network type adjusted to avoid unnecessary DR/BDR election
- Layer 3 EtherChannel (CSW1–CSW2) uses default behavior

---

## Default Route Design

- R1 configured with static default route to Internet
- Floating static route used for backup (higher AD)
- R1 redistributes default route into OSPF
- R1 acts as ASBR

---

## Design Principles

- Dynamic route learning across network
- Stable Router ID using loopbacks
- Reduced unnecessary adjacency overhead (passive interfaces)
- Controlled default route propagation
