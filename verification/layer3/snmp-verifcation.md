# SNMP Verification

## Objective
Verify SNMP configuration and access level.

---

## Commands Used

- show running-config | include snmp

---

## Key Observations

- SNMP community string configured
- Read-only access enforced
- No write (SET) permissions allowed

---

## Sample Output

### 🔹 SNMP Configuration (show running-config | include snmp)
Verifies community string and access level.

<img width="312" height="40" alt="image" src="https://github.com/user-attachments/assets/24242a03-3794-49b1-8a04-9c5498a5ec6a" />


---

## Conclusion

SNMP is configured correctly with read-only access.
