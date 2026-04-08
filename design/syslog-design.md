# Syslog Design

## Objective
Centralize logging for network devices (All router and switches)

---

## Architecture

- SRV1 (10.5.0.4) acts as syslog server
- All devices send logs to SRV1

---

## Configuration

- Logging level: all severity levels
- Buffered logging enabled (8192 bytes)

---

## Design Principles

- Centralized log collection
- Improved troubleshooting visibility
- Remained logging histories
