# EtherChannel Verification

## Objective
Verify EtherChannel formation, bundling, and operational status.

---

## Commands Used

- show etherchannel summary
- show interfaces port-channel 1
- show interfaces trunk

---

## Key Observations

- Port-Channel1 is up/up on both switches
- Member interfaces bundled correctly
- Protocol matches design:
  - Office A → PAgP
  - Office B → LACP
- Port-Channel operates as trunk
- No individual links in standalone state

---

## Sample Output

### 🔹 EtherChannel Summary (show etherchannel summary)
Verifies bundled interfaces and protocol.

<img width="526" height="259" alt="image" src="https://github.com/user-attachments/assets/2b73536d-1358-4e8d-90f3-a412ae27e300" />


---

### 🔹 Port-Channel Interface (show interfaces port-channel 1)
Verifies operational status.

<img width="607" height="399" alt="image" src="https://github.com/user-attachments/assets/33bf496e-9012-4de8-afbc-c03f25beb805" />


---

### 🔹 Trunk Status (show interfaces trunk)
Verifies VLANs allowed across EtherChannel.

<img width="587" height="343" alt="image" src="https://github.com/user-attachments/assets/2b3c583f-c8e4-4929-9209-3789bf4d34d2" />


---

## Conclusion

EtherChannel is functioning correctly with proper bundling and redundancy.
