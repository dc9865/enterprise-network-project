# Base Device Configuration Template

This template was applied to all routers and switches in the lab.

```bash
hostname <DEVICE_NAME>

enable secret jeremylab

username ccna secret ccna

line console 0
 login local
 exec-timeout 30 0
 logging synchronous
