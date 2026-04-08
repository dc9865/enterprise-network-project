# HSRP Design

## Objective
Provide default gateway redundancy for all VLANs across Office A and Office B. 

---

## HSRP Role Distribution

### Office A

| VLAN | Purpose     | Active |
|------|------------|--------|
| 99   | Management | DSW-A1 |
| 10   | PCs        | DSW-A1 |
| 20   | Phones     | DSW-A2 |
| 40   | Wi-Fi      | DSW-A2 |

---

### Office B

| VLAN | Purpose     | Active |
|------|------------|--------|
| 99   | Management | DSW-B1 |
| 10   | PCs        | DSW-B1 |
| 20   | Phones     | DSW-B2 |
| 30   | Servers    | DSW-B2 |

---

## Key Configuration Points

- Virtual IP (VIP) used as default gateway for all hosts
- Active router priority set above default (+5)
- Preemption enabled on active router

---

## Design Principles

- Default gateway redundancy (no single point of failure)
- Load distribution across distribution switches
- Alignment with Layer 2 topology (optimized traffic flow)
