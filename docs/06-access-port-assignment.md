# 06 — Access Port Assignment

## Goal
Assign user-facing ports to the correct VLANs.

## Example (User port)
interface fa0/5
 switchport mode access
 switchport access vlan 10
 spanning-tree portfast
 spanning-tree bpduguard enable

## Example (Voice + Data on a phone port)
interface fa0/10
 switchport mode access
 switchport access vlan 10
 switchport voice vlan 20
 spanning-tree portfast
 spanning-tree bpduguard enable

## Verify
- `show interfaces switchport`
- `show vlan brief`
