# FTP Design

## Objective
Enable file transfer for IOS upgrade.

---

## Architecture

- SRV1 acts as FTP server
- R1 downloads IOS image from SRV1

---

## Configuration

- FTP credentials:
  - Username: cisco
  - Password: cisco

- File transferred:
  - c2900-universalk9-mz.SPA.155-3.M4a.bin

---

## Design Principles

- Centralized image storage
- Simplified IOS upgrade process

---

## Notes

R1 reboots after upgrade and removes old IOS image.
