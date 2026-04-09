# DHCP Verification

## Objective
Verify DHCP pool operation, address assignment, and relay functionality.

---

## Commands Used

- show ip dhcp pool
- show ip dhcp binding
- show running-config | section ip dhcp
- show running-config interface vlan <vlan-id>

---

## Key Observations

- DHCP pools created for all VLANs
- Excluded addresses not assigned to clients
- Clients receive correct:
  - IP address
  - Default gateway
  - DNS server
- DHCP relay configured toward 10.0.0.76

---

## Sample Output

### 🔹 DHCP Pools (show ip dhcp pool)
Verifies pool configuration and usage.

<img width="754" height="690" alt="image" src="https://github.com/user-attachments/assets/3bf30db7-f066-4716-b4e6-80aa2ec2b7b4" />

---

### 🔹 DHCP Bindings (show ip dhcp binding)
Verifies leased addresses.

<img width="594" height="125" alt="image" src="https://github.com/user-attachments/assets/2ea98f1b-5e98-4f94-8837-664c198e3607" />


---

## Conclusion

DHCP services are functioning correctly across all VLANs.
