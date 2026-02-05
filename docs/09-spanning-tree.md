# Step 9 — Spanning Tree Protocol (STP)

This step configures Rapid PVST+ to prevent Layer 2 loops
and control traffic paths across the enterprise network.

## STP Mode
- Rapid PVST+ enabled on all switches

## Root Bridge Design
- Core switches explicitly configured as root
- VLANs split across core switches for load sharing

## Edge Protection
- PortFast enabled on access ports
- BPDU Guard enabled to block rogue switches

## Benefits
- Loop prevention
- Faster convergence
- Improved security and stability


## Root Strategy (example)
- CORE-SW1 root primary for VLANs 10/30/40
- CORE-SW2 root primary for VLANs 20/50/60

## Example (CORE-SW1)
spanning-tree mode rapid-pvst
spanning-tree vlan 10,30,40 priority 24576
spanning-tree vlan 20,50,60 priority 28672

## Verify
- `show spanning-tree vlan 10`
- `show spanning-tree root`
