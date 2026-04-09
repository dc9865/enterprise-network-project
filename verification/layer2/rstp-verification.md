# RSTP Verification

## Objective
Verify root bridge placement, port roles, and edge protections.

---

## Commands Used

- show spanning-tree
- show spanning-tree vlan <vlan-id>
- show spanning-tree root
- show interfaces status err-disabled

---

## Key Observations

- Root bridge matches HSRP active router per VLAN
- Secondary root configured correctly
- No unexpected blocking on critical uplinks
- PortFast enabled on end-host interfaces
- BPDU Guard enabled on end-host interfaces
- No unintended err-disabled ports

---

## Sample Output

### 🔹 Root Bridge (show spanning-tree)
Verifies root bridge per VLAN.

<img width="710" height="555" alt="image" src="https://github.com/user-attachments/assets/d9bddebc-549e-4e65-80b7-8701b43a8e21" />


---

### 🔹 VLAN STP (show spanning-tree vlan <id>)
Verifies port roles and states.

<img width="603" height="270" alt="image" src="https://github.com/user-attachments/assets/a506c5a3-6a88-438a-937e-41be222e8850" />


---

## Conclusion

RSTP is functioning correctly with proper root placement and edge protection.
