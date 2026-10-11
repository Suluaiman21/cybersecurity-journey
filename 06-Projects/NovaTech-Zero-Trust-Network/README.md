
# NovaTech Solutions — Zero-Trust Network Implementation

## Project Overview

Designed and implemented a segmented enterprise network for a fictional organization, NovaTech Solutions, using Cisco Packet Tracer. The project focused on network segmentation, controlled inter-VLAN communication, secure device administration, and traffic filtering using Zero-Trust-inspired security principles.

## Objectives

- Design a segmented network with five VLANs.
- Apply Variable Length Subnet Masking (VLSM) for efficient IP address allocation.
- Configure inter-VLAN routing using a router-on-a-stick architecture.
- Establish dynamic routing between two routers using OSPF.
- Implement Access Control Lists (ACLs) to restrict unauthorized network traffic.
- Configure SSH for secure remote administration.
- Test network connectivity and verify security policies.

## Network Segmentation

The network was divided into five logical security zones:

| VLAN | Purpose | Subnet |
|---|---|---|
| Management | Administrative devices | `192.168.10.0/28` |
| Staff | Employee devices | `192.168.20.0/27` |
| Guest | Guest devices | `192.168.30.0/27` |
| Server | Web and database services | `192.168.40.0/29` |
| Monitoring | Monitoring tools | `192.168.50.0/28` |

The two routers were connected through a serial WAN link using the `10.0.0.0/30` subnet.

## Technologies and Tools

- Cisco Packet Tracer
- VLANs and network segmentation
- IPv4 addressing and VLSM subnetting
- Router-on-a-stick inter-VLAN routing
- OSPF dynamic routing
- Access Control Lists (ACLs)
- SSH remote administration
- WAN traffic filtering

## Security Controls Implemented

### 1. Network Segmentation
Separated management, staff, guest, server, and monitoring devices into distinct VLANs to improve isolation and control traffic flow.

### 2. Least-Privilege Access
Configured ACLs to restrict Guest VLAN access to the Server VLAN and control which sources could reach server resources.

### 3. Secure Administration
Enabled SSH for encrypted remote management of network devices instead of relying on insecure Telnet access.

### 4. WAN Traffic Filtering
Configured inbound ACL-based filtering on the WAN interface to reject selected private and reserved source addresses.

## Testing and Verification

- Verified connectivity through successful ping tests.
- Confirmed OSPF neighbor formation between the routers.
- Tested ACL rules to verify that selected unauthorized traffic was blocked.
- Verified SSH authentication for remote device administration.

## Key Learning Outcomes

- Practical experience with enterprise network design and subnetting.
- Improved understanding of VLAN segmentation and inter-VLAN routing.
- Hands-on configuration of OSPF between routers.
- Application of ACLs to enforce traffic restrictions.
- Understanding of secure network administration and WAN ingress filtering.
- Experience validating network behaviour through connectivity and security testing.

## Project Environment

This project was implemented in a simulated environment using Cisco Packet Tracer. The Zero-Trust approach was demonstrated through segmentation and access restrictions; it does not represent a complete production Zero-Trust architecture.

---

*Academic network security project — implemented and tested in Cisco Packet Tracer.*
