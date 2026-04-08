# NTP Design

## Objective
Provide consistent time synchronization across all network devices.

---

## Architecture

- R1 acts as NTP server (stratum 5)
- R1 syncs from external NTP server: 216.239.35.0
- All switches use R1 Loopback0 (10.0.0.76) as NTP source

---

## Authentication

- NTP authentication enabled
- Key ID: 1
- Password: ccna

---

## Design Principles

- Centralized time source (R1)
- Secure time synchronization using authentication
- Consistent timestamps for logging and troubleshooting
