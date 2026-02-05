# CCNA ENTERPRISE NETWORK MEGA LAB (Packet Tracer)

This project is a full enterprise-style CCNA lab built in **Cisco Packet Tracer**, designed as a realistic portfolio network:
- VLANs (Users, Voice, Servers, Mgmt, Guest, DMZ)
- Trunking + Native VLAN
- EtherChannel (LACP)
- Rapid-PVST+ spanning tree design
- Inter-VLAN routing on multilayer core (3560)
- HSRP default gateways
- OSPF routing (HQ core + WAN/branches)
- ACL segmentation (Users/Mgmt/Guest/DMZ)
- NAT/DMZ publishing (conceptual in PT)
- Troubleshooting & Packet Tracer limitations documented

> Note: Some IOS features (IP SLA, advanced QoS, full Internet cloud routing) are limited in Packet Tracer.
Those limitations are documented in `docs/11-troubleshooting-and-limitations.md`.

---

## Repo Structure

- `packet-tracer/`  
  Packet Tracer `.pkt` file(s)

- `configs/`  
  Device configuration exports (core, edge, branches) + cheat sheets

- `docs/`  
  Step-by-step lab documentation

- `diagrams/`  
  Topology and VLAN maps

---

## Quick Start (How to Use)

1. Open the Packet Tracer file in `packet-tracer/`
2. Follow the docs in this order:
   1) `docs/00-overview.md`  
   2) `docs/physical-cabling.md`  
   3) `docs/base-device-configuration.md`  
   4) `docs/04-ip-addressing-interfaces.md`  
   5) `docs/05-vlan-creation.md`  
   6) `docs/06-access-port-assignment.md`  
   7) `docs/07-trunk-configuration.md`  
   8) `docs/09-spanning-tree.md`  
   9) `docs/10-inter-vlan-routing.md`

---

## Skills Demonstrated (for recruiters)
- Layer 2/3 enterprise switching
- Redundancy (HSRP + EtherChannel)
- Routing design (OSPF)
- Network segmentation (ACLs + VLANs)
- Troubleshooting (EtherChannel mismatches, trunk VLAN masks, PT limitations)
- Documentation & configuration management (GitHub)

---

## License
MIT
