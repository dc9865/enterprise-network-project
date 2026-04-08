# DNS Design

## Objective
Provide centralized name resolution for network devices and clients.

---

## DNS Server

- SRV1 acts as DNS server
- IP address: 10.5.0.4

---

## DNS Records

| Name                  | Mapping            |
|-----------------------|--------------------|
| google.com            | 172.253.62.100     |
| youtube.com           | 152.250.31.93      |
| jeremysitlab.com      | 66.235.200.145     |
| www.jeremysitlab.com  | jeremysitlab.com   |

---

## Device Configuration

All routers and switches:

- Domain name: jeremysitlab.com
- DNS server: 10.5.0.4

---

## Design Principles

- Centralized name resolution
- Consistent domain usage
- Simplified management and troubleshooting
