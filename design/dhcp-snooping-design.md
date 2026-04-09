# DHCP Snooping Design

## Objective
Prevent rogue DHCP servers.

---

## Configuration

- Enabled on all VLANs
- Trusted ports configured appropriately
- Option 82 disabled
- Rate limit: 15 pps (100 pps for WLC link)

---

## Design Principles

- Block unauthorized DHCP responses
- Protect clients from rogue servers
- Control DHCP traffic rate

---

## Notes

Applied on all access switches.
