# IPv6 Design

## Objective
Enable IPv6 connectivity and routing across core devices.

---

## Configuration

- IPv6 routing enabled on R1, CSW1, CSW2
- Interfaces assigned IPv6 addresses:
  - R1 G0/0/0: 2001:db8:a::2/64
  - R1 G0/1/0: 2001:db8:b::2/64

- EUI-64 used for interface IDs on:
  - R1 G0/0, CSW1 G1/0/1 (prefix - 2001:db8:a1::/64)
  - R1 G0/1, CSW2 G1/0/1 (prefix - 2001:db8:a2::/64

- CSW1, CSW2 Port-Channel1 assigned IPv6 address, using link-local (FE80::/10).

---

## Routing

- Static default route:
  - Primary: recursive next-hop
  - Backup: floating route (1 higher AD than Primary)

---

## Design Principles

- Dual-stack readiness
- Automatic interface ID generation (EUI-64)
- Redundant default routing (no single point of failure)
