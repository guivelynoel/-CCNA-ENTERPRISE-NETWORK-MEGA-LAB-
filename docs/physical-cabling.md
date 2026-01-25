## Serial Interfaces Limitation (CCNA Concept)

Serial interfaces are available only on routers, not on switches.
In this lab, WAN connectivity is implemented using router-to-router
serial DCE/DTE links to simulate ISP connections.

Layer 3 switches (3560/3650) are used strictly for LAN switching and
inter-VLAN routing using Ethernet and fiber interfaces.

## Fiber vs Copper in Packet Tracer

In a real enterprise or data center environment, core-to-core and
distribution uplinks are typically implemented using fiber optics
for higher bandwidth and longer distances.

Cisco Packet Tracer abstracts hardware capabilities and may not expose
SFP fiber ports on certain switch models (3560/3650).

For this lab, Gigabit Ethernet copper links are used to simulate
fiber backbone connections. Logical design, redundancy, EtherChannel,
and STP behavior remain identical.

## Interface Type Constraint (Packet Tracer)

In this lab, HQ core switches have a limited number of GigabitEthernet
interfaces available in Cisco Packet Tracer. After reserving Gigabit
ports for uplinks, FastEthernet interfaces are used for additional
core-to-core and distribution connections.

This does not affect logical design, redundancy, EtherChannel operation,
Spanning Tree behavior, or CCNA objectives. In a real production
environment, these links would typically be implemented using
Gigabit or fiber-based uplinks.

