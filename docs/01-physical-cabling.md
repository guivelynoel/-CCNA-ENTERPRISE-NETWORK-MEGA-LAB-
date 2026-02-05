# Physical Cabling (Packet Tracer)

## Core-to-Core
- Two links between CORE-SW1 and CORE-SW2 used for LACP EtherChannel
  - Example: Gi0/1 + Gi0/2 on both sides

## Core-to-Access
- Access switches connect via trunk(s) to core (prefer 1 trunk per access switch)

## Core-to-Edge
- CORE-SW1 and/or CORE-SW2 connect to HQ edge routers using routed ports or trunk depending on design.
  - In this lab: Core is L3 (SVIs), edge routers are WAN/Internet.

## Branches
- Each branch router uplinks to HQ edge via serial or routed Ethernet depending on PT design.

## Best Practice in PT
- Label every link (interface name + subnet)
- Keep EtherChannel links identical (same speed/duplex, same trunk settings)
