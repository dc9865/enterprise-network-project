# Syslog Verification

## Objective
Verify log forwarding and buffering.

---

## Commands Used

- show logging

---

## Key Observations

- Logs sent to 10.5.0.4
- All severity levels logged
- Local buffer enabled (8192 bytes)

---

## Sample Output

### 🔹 Logging Status (show logging)
Verifies remote syslog server and local buffer settings.

<img width="575" height="446" alt="image" src="https://github.com/user-attachments/assets/ddb41d45-4e4e-447c-9a9f-5620f6359626" />


---

## Conclusion

Syslog is functioning correctly with centralized logging.
