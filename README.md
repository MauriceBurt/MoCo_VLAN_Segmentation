# MoCo VLAN Segmentation

This design expands on the Guest Wi-Fi baseline by implementing a multi-department VLAN architecture, simulating a real-world business network with controlled access between internal segments.

## Repository Structure

🔧 [Configs](./configs)  
🗺️ [Topology](./topology)  
📸 [Screenshots](./screenshots)

## Overview
The network is segmented using VLANs to separate departments and services, including:
- HR
- Sales
- Guest Wi-Fi
- Internal Server
- Public Server

Inter-VLAN routing is implemented using a router-on-a-stick configuration, allowing controlled communication between VLANs.

## Key Features
- VLAN-based network segmentation
- Router-on-a-stick inter-VLAN routing (802.1Q)
- Multi-department network design
- ACL enforcement between VLANs
- End-to-end connectivity validation using ICMP (ping)

## Network Behavior

### Internal Users (HR / Sales):
- Can communicate across permitted VLANs
- Have access to internal server resources
- Can reach external/public resources as needed

### Guest Users:
- Can connect to the wireless network
- Receive IP addressing
- Reach their default gateway
- Access public-facing resources

### Restrictions:
- Guest users are **blocked from accessing internal VLANs and servers**
- ACLs enforce segmentation boundaries between departments and guest traffic

## Outcome
This design demonstrates how segmentation scales beyond a simple guest network into a structured internal architecture.

It reflects a real-world approach to network design, where departments are isolated for security while still allowing controlled communication through routing and ACL policies.

## Tools Used
- Cisco Packet Tracer
- Cisco IOS CLI

## Screenshots

Key stages of the design and validation are included in the [Screenshots](./screenshots) directory, including:

- Network topology layout
- VLAN configuration
- Inter-VLAN connectivity
- Guest Wi-Fi connection
- ACL enforcement (blocked vs allowed traffic)

These provide a step-by-step visual breakdown of how the network operates.

## Configurations

Router and switch configurations are included in the [Configs](./configs) directory.

These configurations demonstrate:

- VLAN segmentation across departments (HR, Sales, Guest, Servers)
- Trunking between switch and router (802.1Q)
- Inter-VLAN routing using router-on-a-stick
- ACL enforcement to restrict guest access to internal resources

You can use these configs to review or replicate the design in your own environment.

---
Part of the [Modular Networks Design Library](https://github.com/MauriceBurt/Modular-Networks).
