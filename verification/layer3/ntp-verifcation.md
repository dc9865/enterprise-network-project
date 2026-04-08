# NTP Verification

## Objective
Verify time synchronization and NTP configuration.

---

## Commands Used

- show ntp status
- show ntp associations
- show clock

---

## Key Observations

- R1 synchronized with external NTP server
- Switches using 10.0.0.76 as NTP source
- Clock synchronized across devices
- NTP authentication configured

---

## Sample Output

### 🔹 NTP Status (show ntp status)
Verifies the operational state.

<img width="843" height="110" alt="image" src="https://github.com/user-attachments/assets/9f2090df-3f77-4387-a25d-9922026188fa" />


---
### 🔹 NTP Status (show ntp associations)
Verifies synchronization of NTP connections.

<img width="765" height="101" alt="image" src="https://github.com/user-attachments/assets/48256382-1d34-40c4-aa12-c232fd670baa" />


## Conclusion

NTP is functioning correctly across all devices.
