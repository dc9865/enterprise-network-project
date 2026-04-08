# SSH Design

## Objective
Allows secure remote management access to all devices.

---

## Configuration

- SSH version 2 enabled
- RSA keys generated (maximum size)
- Local user authentication required

---

## Access Control

- ACL restricts SSH access to Office A PC subnet
- Applied to all VTY lines

---

## Additional Settings

- Only SSH allowed (no Telnet)
- Synchronous logging enabled on VTY lines

---

## Design Principles

- Secure remote access
- Restricted management access
- Encrypted communication

---

## Notes

Configured on all routers and switches.
