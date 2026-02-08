# Enterprise-Campus-Network-Lab

This project demonstrates the design, configuration, and troubleshooting of an enterprise-style 3-tier campus network using Cisco devices.
The lab focuses on VLAN segmentation, multilayer switching, dynamic routing (OSPF), redundancy, and real-world failure analysis.

The goal was not just to “make it work”, but to identify and fix realistic production-level issues.

--> Access Layer

Cisco 2960 (Layer 2) switches

One VLAN per access switch:

VLAN 10 – Users
VLAN 20 – Users
VLAN 30 – Users
VLAN 99 – Management

End devices connected via:

Access ports

PortFast enabled
BPDU Guard on edge ports only

--> Distribution Layer

Cisco 3650 multilayer switches

Responsibilities:

Default gateway via SVIs
Inter-VLAN routing
Redundant uplinks from access layer
Layer-3 routed uplinks toward the core
OSPF used for routing

Gateway redundancy via HSRP

--> Core Layer

Cisco 2911 routers
Pure Layer-3
High-speed routed links
OSPF backbone (Area 0)

Default route propagation

--> Key Technologies Used

VLANs & Trunking
Rapid PVST+
PortFast & BPDU Guard
Inter-VLAN Routing (SVIs)
Layer-3 Switch Routing (ip routing)
OSPF (single-area)
HSRP (gateway redundancy)
VLAN pruning & management VLAN
