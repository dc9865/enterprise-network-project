# VLAN Design

## Overview

The network is segmented into multiple VLANs to separate traffic types and improve security and scalability.

---

## Office A VLANs

| VLAN ID | Name        | Purpose        |
|---------|-------------|----------------|
| 10      | PCs         | User devices   |
| 20      | Phones      | VoIP traffic   |
| 40      | WiFi        | Wireless users |
| 99      | Management  | Device mgmt    |

---

## Office B VLANs

| VLAN ID | Name        | Purpose        |
|---------|-------------|----------------|
| 10      | PCs         | User devices   |
| 20      | Phones      | VoIP traffic   |
| 30      | Servers     | Internal apps  |
| 99      | Management  | Device mgmt    |

---

## Key Design Decisions

- Separate VLAN for voice traffic → enables QoS later
- Management VLAN isolated for security
- Server VLAN isolated to reduce broadcast traffic
- VLAN consistency maintained across trunk links
