# NAT Verification

## Objective
Verify NAT translation and Internet connectivity.

---

## Commands Used

- show ip nat translations
- show ip nat statistics
- ping

---

## Key Observations

- Static NAT entry for SRV1 present
- Dynamic NAT translations created for clients
- Internal hosts can reach Internet
- NAT overload functioning correctly

---

## Sample Output

### 🔹 NAT Translations (show ip nat translations)
Verifies address translation.

<img width="626" height="183" alt="image" src="https://github.com/user-attachments/assets/aaac0a90-8588-4a72-9e85-1834cd258cea" />


---

## Conclusion

NAT is functioning correctly for both static and dynamic translations.
