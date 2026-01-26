# Step 7 — Trunk Configuration

This step configures 802.1Q trunk links between access and core switches
to allow VLAN traffic to traverse the network.

## Trunk Design
- Explicit trunk mode (no DTP negotiation)
- Native VLAN set to 99
- Only required VLANs allowed

## Security Notes
- VLAN 1 is not used as native VLAN
- DTP is disabled to prevent unauthorized trunk formation

## Verification
Use the following command:
show interfaces trunk
