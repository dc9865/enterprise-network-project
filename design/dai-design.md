# Dynamic ARP Inspection (DAI) Design

## Objective
Prevent ARP spoofing attacks.

---

## Configuration

- Enabled on all VLANs
- Trusted ports configured
- Validation checks enabled

---

## Design Principles

- Validate ARP packets against DHCP snooping database
- Prevent man-in-the-middle attacks (ie. ARP Spoofing attack)
- Protect Layer 2 integrity

---

## Notes

Depends on DHCP snooping binding table.
