# Port Security Verification

## Objective
Verify MAC address limits and violation handling.

---

## Commands Used

- show port-security
- show port-security interface f0/1

---

## Key Observations

- Maximum MAC limit enforced
- Sticky MAC addresses learned
- Violation mode set to restrict
- Invalid traffic blocked

---

## Sample Output

### 🔹 Port Security Summary (show port-security)
Verifies overall port security status.

<img width="559" height="84" alt="image" src="https://github.com/user-attachments/assets/467e5b45-0561-4183-835b-91c91ad9a0eb" />


---

### 🔹 Interface Detail (show port-security interface f0/1)
Verifies maximum MAC count, sticky learning, and violation mode.

<img width="390" height="180" alt="image" src="https://github.com/user-attachments/assets/a0fcce13-a746-4bad-baaf-aa5ae973c540" />

