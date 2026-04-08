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

## Conclusion

SSH access is secured and properly restricted.
