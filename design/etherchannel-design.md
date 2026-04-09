# EtherChannel Design

## Objective
Provide link redundancy and increased bandwidth between distribution switches.

---

## Architecture

- Layer 2 EtherChannel configured between distribution switches
- Port-Channel1 used in both Office A and Office B

---

## Office A

- Devices: DSW-A1 ↔ DSW-A2
- Protocol: PAgP (Cisco proprietary)
- Mode: desirable (active negotiation)

---

## Office B

- Devices: DSW-B1 ↔ DSW-B2
- Protocol: LACP (open standard)
- Mode: active

---

## Configuration Summary

- Multiple physical links bundled into Port-Channel1
- Operates as a single logical interface
- Trunk configuration applied to Port-Channel interface

---

## Design Principles

- Eliminates single link failure
- Provides load balancing across links
- Ensures loop-free topology with STP
- Uses protocol diversity (PAgP vs LACP)

---

## Notes

- PAgP used in Office A for Cisco-specific implementation  
- LACP used in Office B for standards-based interoperability
