# 00 — Overview

## Goal
Build a realistic enterprise network in Packet Tracer that covers major CCNA topics:
- VLAN segmentation
- Trunking + Native VLAN
- EtherChannel (LACP)
- Spanning Tree (Rapid-PVST+)
- Inter-VLAN Routing (SVIs on multilayer core)
- HSRP gateway redundancy
- OSPF WAN routing to branches
- ACL security for Users/Mgmt/Guest/DMZ
- DMZ services (Web/DNS/Mail/FTP concept)

## High-Level Design
### VLANs
- VLAN 10 — USERS
- VLAN 20 — VOICE
- VLAN 30 — SERVERS
- VLAN 40 — MGMT
- VLAN 50 — GUEST
- VLAN 60 — DMZ
- VLAN 99 — NATIVE / INFRA (trunk native vlan)

### Core
Two Catalyst 3560 multilayer switches:
- SVIs + HSRP as default gateways
- STP tuned per VLAN
- LACP EtherChannel between core switches

### Edge/WAN
- HQ edge routers connect to core and to branch routers
- OSPF used for routing between HQ and branches

## Validation Targets
- Clients receive correct VLAN/IP
- Trunks carry correct VLANs
- EtherChannel bundles cleanly (no suspended links)
- HSRP active/standby correct per VLAN
- Inter-VLAN routing works with ACL enforcement
- OSPF neighbors form and routes propagate
