# EtherChannel Design

## Overview

EtherChannel is used to provide redundancy and increased bandwidth between distribution switches.

---

## Office A

- Protocol: **PAgP (Cisco Proprietary)**
- Mode: Desirable

### Purpose
- Demonstrates Cisco-specific implementation
- Provides redundancy between DSW-A1 and DSW-A2

---

## Office B

- Protocol: **LACP (IEEE 802.3ad)**
- Mode: Active

### Purpose
- Industry-standard EtherChannel protocol
- Ensures interoperability

---

## Benefits

- Load balancing across links
- Redundancy (link failure does not disrupt traffic)
- Simplified management (logical interface)
