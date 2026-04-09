# VLAN Verification

## Objective
Verify VLAN creation, assignment, and trunk propagation.

## Commands Used

- show vlan brief
- show interfaces trunk

## Key Observations

- VLANs 10, 20, 30, 40, 99 present on all switches
- Access ports correctly assigned
- Trunks allow correct VLANs

## Sample Output

### 🔹 VLAN Table (show vlan brief)
Verifies VLAN creation and access port assignment.

<img width="643" height="279" alt="image" src="https://github.com/user-attachments/assets/5b62e6fb-6e26-4ec5-abe4-6d077b252c8b" />


---

### 🔹 Trunk Status (show interfaces trunk)
Verifies VLAN propagation across trunk links.

<img src="https://github.com/user-attachments/assets/b5b840e9-8edc-4910-8226-da2e33dcc0ce" width="700">


---

## Conclusion

VLAN segmentation is functioning correctly across the network.
