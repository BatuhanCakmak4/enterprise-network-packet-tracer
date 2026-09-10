# Small Enterprise Network Design – Cisco Packet Tracer

## Overview

This project simulates a small enterprise network designed and configured using Cisco Packet Tracer.

The network consists of two main departments, IT and IKA, with separate VLANs for wired users, wireless users, network management, and server infrastructure.

The main objective of the project is to implement network segmentation, inter-VLAN communication, centralized DHCP services, wireless connectivity, and remote network device management in a structured enterprise environment.

## Network Topology

![Network Topology](topology.png)

The topology contains:

- 2 Cisco 2911 Routers
- 3 Cisco 2960 Switches
- Multiple wired workstations
- Network printers
- Wireless laptops
- 2 Wireless Access Points
- 1 DHCP Server

## VLAN Structure

| VLAN | Purpose |
|------|---------|
| VLAN 10 | IT Department – Group 1 |
| VLAN 20 | IT Department – Group 2 |
| VLAN 30 | IT Department – Group 3 |
| VLAN 40 | IKA Department – Group 1 |
| VLAN 50 | IKA Department – Group 2 |
| VLAN 60 | IKA Department – Group 3 |
| VLAN 70 | IT Wireless Network |
| VLAN 80 | IKA Wireless Network |
| VLAN 99 | Network Management |
| VLAN 100 | Server Network |

## Network Architecture

### Department Segmentation

The enterprise network is divided into two main departments:

- IT Department
- IKA Department

Each department is further divided into multiple VLANs to separate network traffic and create independent broadcast domains.

### Inter-VLAN Routing

Devices located in different VLANs communicate through routing configured on the network routers.

This allows controlled communication between separate VLAN-based networks while maintaining logical network segmentation.

### Router-to-Router Connectivity

Two Cisco 2911 routers connect the different sections of the enterprise network.

Routing between the routers allows devices from the IT and IKA networks to communicate across the infrastructure.

### Centralized DHCP

A dedicated server is located in VLAN 100 and provides centralized DHCP services to network clients.

DHCP automatically provides network configuration information to clients, reducing the need for manual IP configuration.

### Wireless Networks

Both departments have dedicated wireless networks.

- VLAN 70 – IT Wireless Network
- VLAN 80 – IKA Wireless Network

Wireless laptops connect to the network through dedicated Access Points while remaining logically separated from the wired departmental VLANs.

### Management Network

VLAN 99 is dedicated to network management.

The management VLAN separates administrative traffic from normal user traffic and is used for remote management of network devices.

SSH is used for secure remote access to supported network devices.

## Technologies and Concepts Used

- Cisco Packet Tracer
- VLAN Segmentation
- IEEE 802.1Q VLAN Trunking
- Inter-VLAN Routing
- IP Addressing and Subnetting
- Static Routing
- DHCP
- Wireless Networking
- Management VLAN
- SSH Remote Management
- Network Printers
- Connectivity Testing

## Testing

Network connectivity was tested using ICMP ping between devices located in different parts of the network.

Testing included communication between:

- Devices within the same VLAN
- Devices located in different VLANs
- IT and IKA department networks
- Wired and wireless clients
- Network printers
- Network infrastructure devices

## Project Files

- `enterprise-network.pkt` – Cisco Packet Tracer project
- `topology.png` – Network topology diagram
- `README.md` – Project documentation

## Future Improvements

The network will continue to be developed with additional networking and security features such as:

- Access Control Lists (ACLs)
- Firewall implementation
- Port Security
- NAT/PAT
- Spanning Tree Protocol improvements
- EtherChannel
- Network monitoring
- Additional security controls

## Author

Batuhan Çakmak

Computer Engineering Student