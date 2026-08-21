Company Business Network Design

Overview

This project is a Cisco Packet Tracer implementation of a
company/enterprise network. The design separates departments into VLANs,
connects them through multilayer switches, provides inter-VLAN routing,
and includes network services such as DHCP, DNS, wireless connectivity,
OSPF routing, trunk links, and server infrastructure.

The project demonstrates how a medium-sized company network can be
organized into separate departments while still allowing controlled
communication between different network segments.

Network Architecture

The main communication path is:

ISP
 |
Core Router
 |
OSPF Routing / Backbone
 |
+-------------------------+
| Multilayer Switch 1     |
| Multilayer Switch 2     |
+-------------------------+
 |
Trunk Links
 |
Department Access Switches
 |
PCs / Printers / Smartphones / Servers

Wireless devices connect through an Access Point and are assigned to the
wireless network.

Departments and VLANs

VLAN      Department              Network

VLAN 10   Administration and HR   192.168.16.0/25
VLAN 20   Sales and Marketing     192.168.17.0/24
VLAN 30   Finance                 192.168.18.128/25
VLAN 40   Public Relations        192.168.19.0/25
VLAN 50   Wireless                192.168.20.0/22
VLAN 60   IT and Communication    192.168.18.0/24
VLAN 70   Server Room             192.168.19.128/27

Note: The addressing plan is based on the network labels shown in the
Packet Tracer topology.

Technologies Used

VLAN (Virtual Local Area Network)

VLANs logically separate departments into different broadcast domains.
This improves organization, reduces unnecessary broadcast traffic, and
supports better network segmentation.

Trunk Ports

Trunk links carry traffic for multiple VLANs between switches and
multilayer switches.

Multilayer Switching

The multilayer switches perform both switching and routing functions.
They support communication between different VLANs through inter-VLAN
routing.

Inter-VLAN Routing

Devices in different VLANs are on different IP networks. Inter-VLAN
routing allows them to communicate through a Layer 3 device, such as a
multilayer switch.

OSPF (Open Shortest Path First)

OSPF is used as the dynamic routing protocol for exchanging routing
information between the routed devices. The topology uses OSPF Area 0 as
the backbone area.

DHCP (Dynamic Host Configuration Protocol)

The DHCP server automatically provides network configuration information
such as IP addresses, subnet masks, default gateways, and DNS server
information.

DNS (Domain Name System)

The DNS server translates domain or host names into IP addresses.

Wireless Networking

An Access Point provides wireless connectivity for smartphone devices
connected to the wireless network/VLAN.

STP (Spanning Tree Protocol)

STP is relevant because the topology contains redundant Layer 2 paths.
It helps prevent switching loops by blocking redundant paths when
necessary.

ICMP and PDU Testing

Cisco Packet Tracer Simple PDU tests use ICMP to verify connectivity
between devices. A successful PDU indicates that the source can
communicate with the destination.

Devices Used

The project includes the following main device types:

ISP router

Core router

Two multilayer switches

Departmental access switches

PCs

Printers

Smartphones

Wireless Access Point

DHCP Server

DNS Server

System Administrator PC

Network Services

DHCP Server

The DHCP server dynamically assigns IP addressing information to client
devices.

DNS Server

The DNS server provides name resolution services.

System Administrator PC

The Sys Admin PC can be used for network administration and management
activities.

Server Room

The server room is separated into its own VLAN to isolate important
network services from normal user departments.

Connectivity Testing

The network can be tested using Cisco Packet Tracer's Add Simple PDU
tool.

Steps

Open the project in Cisco Packet Tracer.

Switch to Simulation Mode.

Click Add Simple PDU (closed envelope icon).

Select the source device.

Select the destination device.

Use Capture/Forward or Auto Capture/Play.

Check the PDU status.

A successful result indicates that the tested communication path is
working.

Simulation Buffer Full

Cisco Packet Tracer may display:

Buffer Full --- The maximum number of events has been reached.

This does not necessarily mean the network configuration is incorrect.
It means the Simulation Event List has reached its storage limit because
the network is generating many events.

To resolve this:

Click Clear Event List.

Remove unnecessary old PDUs.

Filter events to only the protocols being tested, such as ICMP.

Use Capture/Forward for step-by-step testing instead of
continuously running the whole topology.

Clearing the event list does not delete the network topology or device
configurations.

Learning Objectives

This project demonstrates:

Enterprise/company network design

IP subnetting and addressing

VLAN segmentation

Trunk configuration

Inter-VLAN routing

Dynamic routing with OSPF

DHCP configuration

DNS services

Wireless connectivity

Server network design

Redundant network architecture

ICMP connectivity testing

Cisco Packet Tracer simulation

Conclusion

This Company Business Network Design demonstrates a structured
enterprise network architecture in Cisco Packet Tracer. Different
company departments are separated using VLANs and subnetting, while
multilayer switches provide inter-VLAN communication. OSPF supports
dynamic routing, and DHCP/DNS servers provide essential network
services.

The project can be used to demonstrate a practical company network
containing departmental segmentation, wireless access, server
infrastructure, routing, switching, and end-to-end connectivity testing.
