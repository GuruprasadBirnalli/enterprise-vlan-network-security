# Enterprise VLAN Network Security

A Cisco Packet Tracer project demonstrating enterprise network segmentation using VLANs, inter-VLAN routing, trunking, port security, and ACL-based traffic control.

## Network Design

The network contains three departmental VLANs:

| VLAN | Department | Network |
|------|------------|---------|
| 10 | HR | 192.168.10.0/24 |
| 20 | Finance | 192.168.20.0/24 |
| 30 | IT | 192.168.30.0/24 |

## Technologies Used

- Cisco Packet Tracer
- VLANs
- 802.1Q Trunking
- Router-on-a-Stick
- Inter-VLAN Routing
- Port Security
- Extended ACLs

## Security Configuration

Port security is configured on departmental access ports.

An extended ACL is used to isolate HR and Finance from each other while allowing other network traffic.

### ACL Policy

- HR → Finance: Denied
- Finance → HR: Denied
- Other traffic: Permitted

## IP Addressing

- PC0: 192.168.10.3
- PC1: 192.168.10.2
- PC2: 192.168.20.2
- PC3: 192.168.20.3
- PC4: 192.168.30.3
- PC5: 192.168.30.2

## Project File

The Cisco Packet Tracer topology is available in:

`Enterprise_VLAN_Network_Security.pkt`

## Learning Objectives

This project demonstrates practical configuration of:

1. VLAN creation and assignment
2. Access and trunk ports
3. Router-on-a-Stick inter-VLAN routing
4. Switch port security
5. Extended ACLs
6. Network segmentation and traffic isolation
