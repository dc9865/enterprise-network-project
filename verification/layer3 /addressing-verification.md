# Layer 3 Addressing Verification

## Objective
Verify Layer 3 interfaces, EtherChannel, loopbacks, and management IPs.

---

## Commands Used

- show ip interface brief
- show etherchannel summary
- show ip route

---

## Key Observations

- Port-Channel1 is up/up on CSW1 and CSW2
- G1/0/2–3 correctly bundled into EtherChannel
- Routed interfaces between core and distribution are up
- Loopback interfaces present on all L3 devices
- VLAN 99 SVI configured on all access switches
- R1 interfaces received IPs and are operational

---

## Sample Output

### 🔹 Interface Status (show ip interface brief)
Verifies all Layer 3 interfaces and loopbacks are up.

<img width="652" height="467" alt="image" src="https://github.com/user-attachments/assets/c431d9e6-5741-4dcc-aa95-12bb62b26c20" />


---

### 🔹 EtherChannel Status (show etherchannel summary)
Verifies Port-Channel1 and member interfaces.

<img width="550" height="252" alt="image" src="https://github.com/user-attachments/assets/26a70c86-3415-42aa-83be-a271488bbc77" />


---

### 🔹 Routing Table (show ip route)
Verifies Layer 3 reachability.

<img width="823" height="728" alt="image" src="https://github.com/user-attachments/assets/c34caa47-cc5d-4b54-9f90-0eeb9e8428f4" />


---
