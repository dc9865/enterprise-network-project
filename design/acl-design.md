# ACL Design

## Objective
Control traffic between Office A and Office B PCs.

---

## Policy

- Allow ICMP from Office A PCs → Office B PCs
- Deny all other traffic between these subnets
- Permit all other traffic

---

## Placement

- Extended ACL applied close to source (Office A)

---

## Design Principles

- Least privilege access
- Reduce unnecessary traffic
- Follow extended ACL best practice (source placement)

---

## Notes

ACL applied to control inter-office communication.
