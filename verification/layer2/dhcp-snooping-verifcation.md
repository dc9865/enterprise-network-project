# DHCP Snooping Verification

## Objective
Verify DHCP snooping operation and trust boundaries.

---

## Commands Used

- show ip dhcp snooping
- show ip dhcp snooping binding

---

## Key Observations

- DHCP snooping enabled on VLANs
- Trusted interfaces configured correctly
- Rate limiting active
- Binding table populated

---

## Sample Output

### 🔹 DHCP Snooping Status (show ip dhcp snooping)
Verifies enabled VLANs, trust state, and rate limits.

<img width="496" height="488" alt="image" src="https://github.com/user-attachments/assets/ca024422-d786-4977-a7e5-cb3785010512" />


---

### 🔹 DHCP Snooping Bindings (show ip dhcp snooping binding)
Verifies learned client bindings.

<img width="649" height="73" alt="image" src="https://github.com/user-attachments/assets/9587a830-dd7b-4c05-8535-28e061debb57" />

