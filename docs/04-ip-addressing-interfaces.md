# 04 — IP Addressing & Interfaces

## VLAN Subnets (HQ)
- VLAN 10 USERS:   10.10.10.0/24  (HSRP VIP: 10.10.10.1)
- VLAN 20 VOICE:   10.10.20.0/24  (HSRP VIP: 10.10.20.1)
- VLAN 30 SERVERS: 10.10.30.0/24  (HSRP VIP: 10.10.30.1)
- VLAN 40 MGMT:    10.10.40.0/24  (HSRP VIP: 10.10.40.1)
- VLAN 50 GUEST:   10.10.50.0/24  (HSRP VIP: 10.10.50.1)
- VLAN 60 DMZ:     10.10.60.0/24  (HSRP VIP: 10.10.60.1)
- VLAN 99 NATIVE:  no user hosts recommended

## Core Switch SVIs
- CORE-SW1 uses .2 IP on each SVI
- CORE-SW2 uses .3 IP on each SVI
- VIP is .1 via HSRP

Example:
- VLAN10:
  - CORE-SW1: 10.10.10.2
  - CORE-SW2: 10.10.10.3
  - HSRP VIP: 10.10.10.1

## Routed/WAN Links
Use /30 point-to-point subnets for router links.
Document those inside `docs/Addressing-Table` (or update with your exact PT subnets).
