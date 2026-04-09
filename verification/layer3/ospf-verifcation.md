# OSPF Verification

## Objective
Verify OSPF adjacencies, route exchange, and default route propagation.

---

## Commands Used

- show ip ospf neighbor
- show ip route
- show ip ospf interface brief
- show ip protocols

---

## Key Observations

- OSPF neighbors formed on all routed links
- Router IDs match loopback addresses
- Loopback networks present in routing table
- Passive interfaces do not form adjacencies
- Default route learned from R1
- Full reachability across network

---

## Sample Output

### 🔹 OSPF Neighbors (show ip ospf neighbor)
Verifies adjacency formation.

<img width="630" height="144" alt="image" src="https://github.com/user-attachments/assets/38c37d88-ed01-4263-b8ab-83f36b70015f" />

---

### 🔹 Routing Table (show ip route)
Verifies OSPF routes and default route.

<img width="663" height="351" alt="image" src="https://github.com/user-attachments/assets/d50af676-ad97-4e4e-9047-80282f58910e" />


---

## Conclusion

OSPF is functioning correctly with full route exchange and stable neighbor relationships.

