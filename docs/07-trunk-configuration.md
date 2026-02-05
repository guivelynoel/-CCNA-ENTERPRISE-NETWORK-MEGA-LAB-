# Step 7 — Trunk Configuration

This step configures 802.1Q trunk links between access and core switches
to allow VLAN traffic to traverse the network.


## Trunk to Access Switch
interface fa0/10
 switchport mode trunk
 switchport trunk native vlan 99
 switchport trunk allowed vlan 10,20,30,40,50,60,99

## Core-to-Core (EtherChannel trunk)
Port-channel should be trunk with same native/allowed VLANs.

## Verify
- `show interfaces trunk`
- `show spanning-tree vlan 10`

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
