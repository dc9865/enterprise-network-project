# SSH Verification

## Objective
Verify secure remote access configuration.

---

## Commands Used

- show ip ssh
- show running-config | section vty
- show access-lists

---

## Key Observations

- SSH version 2 enabled
- RSA keys present
- VTY lines allow SSH only
- ACL applied restricting access
- Local login required

---

## Sample Output

### 🔹 SSH Status (show ip ssh)
Verifies SSH version and status.

<img width="534" height="62" alt="image" src="https://github.com/user-attachments/assets/647847a1-a654-436c-97c1-9536f7f01341" />


---

### 🔹 VTY Configuration (show running-config | section vty)
Verifies login method and transport input settings.

<img width="371" height="154" alt="image" src="https://github.com/user-attachments/assets/42e2ed46-f151-4c33-8d3f-5d66486e706a" />


---

### 🔹 ACL Check (show access-lists)
Verifies SSH source restriction.

<img width="274" height="43" alt="image" src="https://github.com/user-attachments/assets/d6cbbff9-bcc1-422a-bc7e-f706de2aec37" />


---

## Conclusion

SSH access is secured and properly restricted.
