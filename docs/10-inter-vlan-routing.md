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
- 
## Requirements
- `ip routing` enabled on both core switches
- SVIs created for VLANs 10/20/30/40/50/60
- HSRP group per VLAN with VIP .1

## Verify
- `show ip interface brief`
- `show standby brief`
- Ping between VLANs (as permitted by ACLs)
