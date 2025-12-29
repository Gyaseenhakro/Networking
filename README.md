# Cisco L2 Switches Configration

# Understading Network Diagram 
The network is a three-switch topology using PVST+ (Per-VLAN Spanning Tree Plus) with VLAN 10 and VLAN 20. Redundancy and loop prevention are achieved using Spanning Tree and an EtherChannel between the lower switches.


# Please Note Down That
'enable' password is "enable123"
'admin' password is "admin123"
# Switches

SW-01
Management IP: 192.168.10.200

SW-02
Management IP: 192.168.10.201

SW-03 (top / distribution switch)
Management IP: 192.168.10.202

# Inter-Switch Connections

SW-01 ↔ SW-02
Connected using an EtherChannel (bundled links)
Increases bandwidth and provides redundancy

SW-01 ↔ SW-03 and SW-02 ↔ SW-03
Trunk links carrying multiple VLANs
PVST+
Runs per VLAN to prevent loops
Allows different root paths for VLAN 10 and VLAN 20
VLANs and End Devices

VLAN 10 (Green)
Host 192.168.10.101 connected to SW-02
Host 192.168.10.102 connected to SW-01
Host 192.168.10.103 connected to SW-03

VLAN 20 (Yellow)
Host 192.168.20.101 connected to SW-02
Host 192.168.20.102 connected to SW-02
Host 192.168.20.103 connected to SW-03

# Key Features Illustrated
Layer 2 VLAN segmentation (VLAN 10 & VLAN 20)
Redundant paths between switches
Loop prevention using PVST+
Higher throughput & fault tolerance using EtherChannel
Centralized distribution switch (SW-03)

If you want, I can also:
Explain PVST+ behavior per VLAN
Identify root bridge placement
Walk through traffic flow for each VLAN
Help you configure this topology on Cisco switches


