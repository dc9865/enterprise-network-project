# HSRP Verification

## Objective
Verify HSRP virtual gateways, active/standby roles, and failover readiness.

---

## Commands Used

- show standby brief
- show standby
- show ip interface brief

---

## Key Observations

- HSRP configured on all VLAN interfaces
- Virtual IP addresses match design
- Active routers:
  - DSW-A1 (VLAN 99, 10)
  - DSW-A2 (VLAN 20, 40)
  - DSW-B1 (VLAN 99, 10)
  - DSW-B2 (VLAN 20, 30)
- Standby routers present on all VLANs
- Preemption enabled on active devices

---

## Sample Output

### 🔹 HSRP Status (show standby brief)
Verifies active/standby roles per VLAN.

<img width="559" height="111" alt="image" src="https://github.com/user-attachments/assets/23120ab7-accb-4b89-8932-99dda6bde31e" />


---

### 🔹 Detailed HSRP (show standby)
Verifies priority, preemption, and virtual IP.

<img width="594" height="506" alt="image" src="https://github.com/user-attachments/assets/00e31c26-cccb-47d8-a66c-4e773d4a8cd4" />


---

## Conclusion

HSRP is functioning correctly and providing gateway redundancy across all VLANs.
