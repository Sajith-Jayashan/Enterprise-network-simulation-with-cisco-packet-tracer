# Enterprise-network-simulation-with-cisco-packet-tracer

## Project
This project is a high-fidelity simulation of a secure enterprise branch office network designed using Cisco Packet Tracer. The goal was to engineer a robust, scalable architecture that mimics how a local office connects to a cloud-based environment while maintaining strict security protocols.

## Key features

### Network segmentation
- Implemented VLAN 10 (Admin) and VLAN 20 (Staff) to isolate departmental traffic at the Layer 2 level.

### Inter-VLAN routing
- Configured Router-on-a-Stick using sub-interfaces on a Cisco ISR 4321 to allow controlled communication between subnets.

### Dynamic addressing
- Established a DHCP Server on the router to automate IP management for end devices.

### Edge connectivity (NAT/PAT)
- Configured Network Address Translation (Overload) to bridge private internal subnets with a simulated public cloud server (`8.8.8.8`).

### Security using extended ACLs
- Developed and applied Access Control Lists to enforce a **"Least Privilege"** policy:
  - Admin → Allowed access to cloud resources  
  - Staff → Restricted access  

## Network topology

- **Router:** Cisco ISR 4321 (Edge Gateway)  
- **Switch:** Cisco Catalyst 2960 (Access Layer)  
- **End Devices:**  
  - Admin PC  
  - Staff PC  
  - Generic Server

## Addressing Schema

| Network | Subnet |
|--------|--------|
| Admin  | 192.168.10.0/24 |
| Staff  | 192.168.20.0/24 |
| Cloud  | 8.8.8.0/24 |
