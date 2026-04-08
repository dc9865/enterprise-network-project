# RSTP Design (Part 4)

## Objective
Provide loop prevention, fast convergence, and predictable Layer 2 forwarding.

---

## Root Bridge Strategy

- Root bridge aligned with HSRP active router per VLAN
- Primary root → lowest STP priority
- Secondary root → next lowest priority

---

## VLAN Root Alignment

### Office A
- VLAN 99, 10 → DSW-A1 (Primary)
- VLAN 20, 40 → DSW-A2 (Primary)

### Office B
- VLAN 99, 10 → DSW-B1 (Primary)
- VLAN 20, 30 → DSW-B2 (Primary)

---

## Edge Port Configuration

- PortFast enabled on all end-host ports
- BPDU Guard enabled on all end-host ports

---

## Design Principles

- Prevent Layer 2 loops
- Align Layer 2 path with Layer 3 gateway (HSRP)
- Fast host connectivity (PortFast)
- Protect against rogue switches (BPDU Guard)

