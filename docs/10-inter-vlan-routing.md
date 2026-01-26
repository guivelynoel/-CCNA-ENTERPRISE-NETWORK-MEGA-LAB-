# Step 10 — Inter-VLAN Routing (SVIs)

This step enables Layer 3 routing on core switches using
Switch Virtual Interfaces (SVIs).

## Design
- Core switches act as default gateways
- One SVI per VLAN
- No router-on-a-stick

## Benefits
- High performance routing
- Simplified design
- Enterprise scalability

## Verification
show ip interface brief
ping between VLANs
