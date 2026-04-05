# EtherChannel Configuration

## Office A – PAgP

```bash
interface range g0/1 - 2
 channel-group 1 mode desirable

interface port-channel 1
 switchport mode trunk
