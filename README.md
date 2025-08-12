Enterprise Networking Project – JFSL Financial Institution Network
Overview
Jubilee Financial Services Ltd (JFSL) is a leading financial services provider in Kenya, offering online financial solutions and client services. The company operates from Nairobi in an eleven-story building, with its headquarters occupying the 7th and 8th floors.

JFSL’s headquarters is divided into five departments:

Human Resources (HR)

Customer Service (CS)

Marketing (MK)

Legal Management (LM)

Information Technology (IT)

Each department requires dedicated network resources, including wired and wireless connectivity, IP phones, and integration with a secure external server site hosting essential services (DHCP, DNS, Web, and Email).

Network Requirements
Multi-floor LAN Design

7th Floor: HR, CS, and MK – each with ≥ 40 user devices, 40 IP phones, and 1 Wi-Fi AP.

8th Floor: LM and IT – each with ≥ 20 user devices, 20 IP phones, and 1 Wi-Fi AP.

External Server-Side Site

Connected to HQ via a secure WAN link.

Hosts DHCP, DNS, Web, and Email servers.

Redundancy & ISPs

Two ISP connections (Sataricom ISP and JTL ISP) for load balancing and failover.

VoIP Integration

Voice VLAN (ID 120) implemented across all departments.

Cisco Catalyst 2811 router used as VoIP gateway with dial number allocation.

Security & Access Control

ACLs to restrict access to external resources.

Port security to limit devices per port with sticky MAC and shutdown violation mode.

SSH with standard ACL for secure remote device management.

Network Services & Routing

VLAN segmentation for each department with unique subnets.

OSPF as the routing protocol for LAN and WAN connectivity.

NAT for internet access.

IPsec Site-to-Site VPN between HQ and server site for secure data exchange.

IP Addressing Scheme
Data Network: 192.168.20.0/24 (subnetted per VLAN)

Voice Network: 10.10.10.0/24

Public Addressing: 190.200.100.0/30 (WAN links)

Server Network: 192.168.21.0/28

Technologies Implemented
VLANs & Inter-VLAN Routing via multilayer switches.

DHCP relay for dynamic IP allocation from the server site.

OSPF for route advertisement.

ACLs & Port Security for access control.

NAT/PAT for internet connectivity.

IPsec VPN for secure site-to-site communication.

Redundant ISP links for resilience.
