# Wireless Design

## Objective
Provide wireless connectivity for clients in the Wi-Fi VLAN.

---

## Architecture

- WLC1 manages LWAP1(Office A) and LWAP2(Office B)
- Wireless clients connect through SSID mapped to VLAN 40
- Wi-Fi subnet: 10.6.0.0/24

---

## WLC Interface Configuration

| Parameter | Value        |
|----------|--------------|
| Name     | Wi-Fi        |
| VLAN     | 40           |
| Port     | 1            |
| IP       | 10.6.0.4     |
| Gateway  | 10.6.0.1     |
| DHCP     | 10.0.0.76    |

---

## WLAN Configuration

| Parameter | Value        |
|----------|--------------|
| Profile  | Wi-Fi        |
| SSID     | Wi-Fi        |
| ID       | 1            |
| Status   | Enabled      |
| Security | WPA2-PSK (AES) |
| PSK      | cisco123     |

---

## Design Principles

- Centralized wireless management via WLC
- VLAN-based segmentation (VLAN 40)
- Secure wireless access using WPA2-PSK
- Integration with centralized DHCP (R1)

---

## Notes

- Packet Tracer limitation: wireless clients may not obtain DHCP leases
