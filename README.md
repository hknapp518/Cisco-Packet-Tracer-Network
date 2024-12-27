# Cisco-Packet-Tracer-Network

In this project, I set up a small network using Cisco Packet Tracer to configure a DHCP server, DNS server, and Web server. The network simulates a small office environment, consisting of 1 router, 2 switches, and 4 personal computers. The goal was to configure the network services for the desktops to automatically obtain IP addresses via DHCP, resolve domain names through DNS, and access a locally hosted web server for internal use.

## Network Diagram
![Cisco- complete topology](https://github.com/user-attachments/assets/6d9e4d3d-5a6a-4f4d-8ba5-247cc6869dc3)

## Setup Guide

- I configured both switches with the appropriate IP addresses and subnet masks for each VLAN, ensuring proper network segmentation and communication between devices on different subnets.

![Cisco- Configured the router for both IP addresses to communcate ](https://github.com/user-attachments/assets/daa7c94c-da43-480a-b72c-1408a8237491)

- Configured the DHCP server to automatically assign IP addresses to the personal computers on the network, using my DNS server as the primary DNS. Additionally, I created two VLANs to separate the servers from the four personal computers.
![CISCO dhcp server for 2 vlans](https://github.com/user-attachments/assets/f48b8109-37e0-42d4-93df-30da1b648ea0)
