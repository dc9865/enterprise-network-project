# NAT Design

## Objective
Enable internal hosts to access the Internet and provide external access to SRV1.

---

## Static NAT

- SRV1 mapped to public IP:
  - 203.0.113.113

---

## Dynamic NAT (PAT)

- ACL 2 defines internal subnets:
  - 10.1.0.0/24
  - 10.2.0.0/24
  - 10.3.0.0/24
  - 10.4.0.0/24
  - 10.6.0.0/24

- NAT pool:
  - POOL1: 203.0.113.200–207 (/29)

- PAT enabled using ACL 2 and POOL1

---

## Design Principles

- Internal address translation for Internet access
- Public access to internal server via static NAT
- Efficient IP usage via PAT

---

## Notes

Default route failover tested by disabling R1 interface.
