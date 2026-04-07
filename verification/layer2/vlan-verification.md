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

<img width="653" height="340" alt="image" src="https://github.com/user-attachments/assets/1a9c34a6-c426-43e8-b9f7-46284c1110ad" />


---

### 🔹 Trunk Status (show interfaces trunk)
Verifies VLAN propagation across trunk links.

<img src="https://github.com/user-attachments/assets/b5b840e9-8edc-4910-8226-da2e33dcc0ce" width="700">

## Conclusion

VLAN segmentation is functioning correctly across the network.
