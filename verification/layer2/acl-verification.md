# ACL Verification

## Objective
Verify traffic filtering between Office A and Office B.

---

## Commands Used

- show access-lists
- show running-config interface

---

## Key Observations

- ICMP allowed between Office A and B PCs
- Other traffic blocked
- ACL applied to correct interface/direction

---

## Sample Output

### 🔹 ACL Entries (show access-lists)
Verifies permit/deny rules.

<img width="462" height="105" alt="image" src="https://github.com/user-attachments/assets/b05ad362-0ea7-4db3-b2ba-b09f3bed2f62" />


---

## Conclusion

ACL is functioning correctly with intended traffic filtering.
