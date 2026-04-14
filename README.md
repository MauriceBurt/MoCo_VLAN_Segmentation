# Guest Wi-Fi Segmentation

This design demonstrates a segmented small business network that supports guest Wi-Fi access while protecting internal resources.

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
- Router-on-a-stick inter-VLAN routing
- Wireless guest network integration
- ACL enforcement to restrict guest access to internal resources
- End-to-end connectivity validation using ICMP (ping)

## Network Behavior
Guest users are able to:
- Connect to the wireless network
- Receive IP addressing
- Reach their default gateway
- Access public-facing resources

Guest users are not able to:
- Access internal server resources

Internal users retain full access to required services across VLANs.

## Outcome
This design enforces network isolation between guest and internal environments while preserving necessary access for trusted users, reflecting a real-world approach to secure network segmentation.

## Tools Used
- Cisco Packet Tracer
- Cisco IOS CLI

## Configurations

Router and switch configurations are included in the `/configs` directory.

These configurations demonstrate:

- VLAN segmentation across departments (HR, Sales, Guest, Servers)
- Trunking between switch and router (802.1Q)
- Inter-VLAN routing using router-on-a-stick
- ACL enforcement to restrict guest access to internal resources

You can use these configs to review or replicate the design in your own environment.