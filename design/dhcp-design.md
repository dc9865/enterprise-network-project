# DHCP Design (Part 6 – Tasks 1–2)

## Objective
Provide centralized IP address assignment for all VLANs across both offices.
This file covers DHCP configuration and relay behavior.

---

## Architecture

- R1 acts as the centralized DHCP server
- Distribution switches relay DHCP requests to R1 (Loopback0: 10.0.0.76)

---

## DHCP Pools

| Pool     | Subnet         | Default Gateway | DNS Server       | Notes |
|----------|----------------|-----------------|------------------|-------|
| A-Mgmt   | 10.0.0.0/28    | 10.0.0.1        | 10.5.0.4 (SRV1)  | WLC: 10.0.0.7 |
| A-PC     | 10.1.0.0/24    | 10.1.0.1        | 10.5.0.4 (SRV1)  | |
| A-Phone  | 10.2.0.0/24    | 10.2.0.1        | 10.5.0.4 (SRV1)  | |
| B-Mgmt   | 10.0.0.16/28   | 10.0.0.17       | 10.5.0.4 (SRV1)  | WLC: 10.0.0.7 |
| B-PC     | 10.3.0.0/24    | 10.3.0.1        | 10.5.0.4 (SRV1)  | |
| B-Phone  | 10.4.0.0/24    | 10.4.0.1        | 10.5.0.4 (SRV1)  | |
| Wi-Fi    | 10.6.0.0/24    | 10.6.0.1        | 10.5.0.4 (SRV1)  | |

---

## Excluded Addresses

- First 10 usable IPs in each subnet are excluded
- Prevents assignment of reserved/static addresses

---

## DHCP Relay

- Configured on distribution switch SVIs
- Target: 10.0.0.76 (R1 Loopback0)

---

## Design Principles

- Centralized IP management
- Reduced configuration overhead on clients
- Scalable across multiple VLANs
- Consistent DNS and gateway assignment
