Enterprise Network Infrastructure Design using Cisco Packet Tracer
 Project Overview

This project is a Cisco Packet Tracer Enterprise Network Simulation designed to demonstrate how a medium-to-large organization can build a secure, scalable, reliable, and fault-tolerant network.

The network follows the Three-Tier Architecture consisting of the Core Layer, Distribution Layer, and Access Layer, ensuring efficient communication between multiple departments while providing centralized network services and Internet connectivity.

 Objectives
Design a scalable enterprise network.
Implement VLAN-based network segmentation.
Enable Inter-VLAN communication.
Configure centralized DHCP, DNS, and Email services.
Provide wired and wireless connectivity.
Implement redundant links for high availability.
Simulate real-world enterprise networking concepts.


 Network Architecture
                    Internet
                  ISP-1     ISP-2
                     |         |
                Core Router 1  Core Router 2
                     \         /
                      \       /
            -------------------------
            | Multilayer Switch 1   |
            | Multilayer Switch 2   |
            -------------------------
      |        |        |        |        |        |
    Sales      HR    Finance   Admin    ICT    Server
      |        |        |        |        |        |
 End Devices End Devices End Devices End Devices End Devices Servers

 
 Three-Tier Architecture
1. Core Layer
Devices
2 ISP Routers
2 Cisco 2811 Core Routers
Purpose

The Core Layer serves as the backbone of the enterprise network.

It is responsible for:

Connecting the organization to the Internet
High-speed packet forwarding
Routing traffic outside the organization
Providing Internet redundancy through dual ISPs
Features
Dual ISP Connectivity
Redundant Core Routers
Fault Tolerance
High Availability
2. Distribution Layer
Devices
2 Cisco 3560 Multilayer Switches
Purpose

The Distribution Layer acts as the intelligence of the network.

Responsibilities include:

VLAN Creation
Inter-VLAN Routing
Default Gateway Configuration
Route Processing
Traffic Management
Network Segmentation
Why Multilayer Switch?

Unlike a Layer 2 switch, a Multilayer Switch performs both:

Layer 2 Switching
Layer 3 Routing

This provides faster routing between VLANs than using a traditional router.

3. Access Layer
Devices
Cisco 2960 Switches

Departments:

Sales
Human Resources
Finance
Administration
ICT
Server Room
Purpose

The Access Layer connects all end-user devices to the network.

Connected devices include:

Desktop PCs
Printers
Wireless Access Points
Laptops
Tablets

 
 Department Structure

Each department contains:

1 Desktop PC
1 Network Printer
1 Wireless Access Point
1 Laptop
1 Tablet

Benefits:

Easy management
Department isolation
Secure communication
Wireless mobility

 
 
 VLAN Configuration

Each department is assigned its own VLAN.

Department	VLAN	Example Network
Sales	VLAN 10	192.168.10.0/24
HR	VLAN 20	192.168.20.0/24
Finance	VLAN 30	192.168.30.0/24
Administration	VLAN 40	192.168.40.0/24
ICT	VLAN 50	192.168.50.0/24
Server Room	VLAN 60	192.168.60.0/24
Benefits of VLANs
Improved Security
Reduced Broadcast Traffic
Better Network Performance
Simplified Management
Department Isolation

 
 
 Inter-VLAN Routing

Inter-VLAN Routing is performed by the Cisco 3560 Multilayer Switches.

Each VLAN has its own Switch Virtual Interface (SVI) which acts as the default gateway.

Example:

Sales PC
      ↓
Sales Switch
      ↓
Multilayer Switch
      ↓
Finance Switch
      ↓
Finance PC

This allows different departments to communicate securely when required.


 
 Network Services
DHCP Server

Automatically assigns:

IP Address
Subnet Mask
Default Gateway
DNS Server Address

Benefits:

Eliminates manual IP configuration
Prevents IP conflicts
Simplifies network administration
DNS Server

Responsible for converting:

mail.company.com

into

192.168.x.x

This enables users to access services using domain names instead of IP addresses.

Email Server

Provides internal organizational email communication.

Example:

sales@company.com

↓

admin@company.com

 
Wireless Network

Each department includes a Wireless Access Point.

Purpose:

Connect laptops wirelessly
Connect tablets wirelessly
Increase employee mobility
Maintain users within their department VLAN

 
 Redundancy

This project implements redundancy at multiple levels.

Internet Redundancy
ISP 1
ISP 2

If one ISP fails, the second ISP continues providing connectivity.

Router Redundancy
Core Router 1
Core Router 2

Provides uninterrupted routing services.

Switch Redundancy

Every department switch connects to both Multilayer Switches.

Benefits:

Backup communication path
High Availability
Fault Tolerance
Reduced downtime
📡 Data Flow
Internet Communication
Laptop

↓

Access Point

↓

Department Switch

↓

Multilayer Switch

↓

Core Router

↓

ISP

↓

Internet
Inter-Department Communication
Sales PC

↓

Sales Switch

↓

Multilayer Switch

↓

Finance Switch

↓

Finance Printer
🛠 Technologies Used
Cisco Packet Tracer
Cisco 2811 Routers
Cisco 3560 Multilayer Switches
Cisco 2960 Access Switches
VLANs
Trunking
Inter-VLAN Routing
DHCP
DNS
Email Server
Wireless Access Points
Static Routing
Redundant Links

 
 
Features
Enterprise Three-Tier Architecture
Department-wise VLAN Segmentation
Inter-VLAN Communication
Centralized Network Services
Wireless Connectivity
Redundant Network Design
Fault-Tolerant Infrastructure
Scalable Architecture
High-Speed Internal Routing
Secure Department Isolation


Learning Outcomes

Through this project, the following networking concepts were implemented and understood:

Enterprise Network Design
Cisco Router Configuration
Cisco Switch Configuration
VLAN Configuration
Trunk Port Configuration
Inter-VLAN Routing
IP Addressing and Subnetting
DHCP Configuration
DNS Configuration
Email Server Configuration
Wireless Networking
Redundancy and High Availability
Three-Tier Network Architecture
Fault Tolerance in Enterprise Networks

 
 

 
 
 Conclusion

This project demonstrates the design and implementation of a modern enterprise network using Cisco Packet Tracer. By combining Three-Tier Architecture, VLAN segmentation, Inter-VLAN Routing, centralized network services, wireless connectivity, and redundant infrastructure, the network achieves improved security, scalability, reliability, and performance.

The design closely resembles real-world enterprise networking practices and provides a strong foundation for understanding campus network architecture, making it suitable for academic projects, networking laboratories, and interview demonstrations.
