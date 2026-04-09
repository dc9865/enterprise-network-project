# LLDP / CDP Verification

## Objective
Verify device discovery configuration and exposure control.

---

## Commands Used

- show cdp neighbors
- show lldp neighbors
- show lldp interface

---

## Key Observations

- CDP disabled on all devices
- LLDP enabled globally
- LLDP not active on access ports
- LLDP neighbors visible only between network devices

---

## Sample Output

### 🔹 LLDP Neighbors (show lldp neighbors)
Verifies neighbor discovery.

<img width="575" height="137" alt="image" src="https://github.com/user-attachments/assets/0e81cd3b-301a-41b8-8917-b09264f30df6" />


---

## Conclusion

LLDP is functioning correctly and CDP is disabled as designed.
