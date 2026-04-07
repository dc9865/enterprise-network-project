# Redundancy Design

## Objective
Ensure high availability and eliminate single points of failure.

## Implementation

- Dual core switches (CSW1 / CSW2)
- Redundant uplinks from distribution to core
- EtherChannel for link aggregation
- RSTP for loop prevention

## Failure Scenarios Covered

- Link failure → traffic rerouted via EtherChannel
- Switch failure → alternate path via secondary core

## Why This Matters

- Prevents downtime
- Maintains traffic flow
- Critical for enterprise environments
