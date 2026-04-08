# DAI Verification

## Objective
Verify ARP inspection and validation behavior.

---

## Commands Used

- show ip arp inspection
- show ip arp inspection interfaces

---

## Key Observations

- DAI enabled on VLANs
- Trusted ports configured
- ARP validation active

---

## Sample Output

### 🔹 DAI Status (show ip arp inspection)
Verifies enabled VLANs and trusted interfaces.

<img width="555" height="315" alt="image" src="https://github.com/user-attachments/assets/782a407e-9c27-4ef2-9d36-8e9280ee90da" />


---

### 🔹 DAI Interfaces (show ip arp inspection interfaces)
Verifies trusted interfaces with DAI-rating configurations.

<img width="511" height="418" alt="image" src="https://github.com/user-attachments/assets/c9730c6a-5364-414e-98be-df4900a95190" />


---

## Conclusion

DAI is functioning correctly.
