# Step 5 — VLAN Creation

This step creates all VLANs across HQ and branch switches.
VLANs provide Layer 2 segmentation for security and scalability.

## VLAN List
- VLAN 10 — USERS
- VLAN 20 — VOICE
- VLAN 30 — SERVERS
- VLAN 40 — MGMT
- VLAN 50 — GUEST
- VLAN 60 — DMZ

## Design Notes
- VLAN IDs are consistent across the enterprise
- Branches implement a reduced VLAN set
- No inter-VLAN routing is enabled at this stage

## Verification
Use the following command on switches:
