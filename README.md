# Cisco-Packet-Tracer-Network

In this project, I set up a small network using Cisco Packet Tracer to configure a DHCP server, DNS server, and Web server. The network simulates a small office environment, consisting of 1 router, 2 switches, and 4 personal computers. The goal was to configure the network services for the desktops to automatically obtain IP addresses via DHCP, resolve domain names through DNS, and access a locally hosted web server for internal use.

## Network Diagram
![Cisco- complete topology](https://github.com/user-attachments/assets/6d9e4d3d-5a6a-4f4d-8ba5-247cc6869dc3)

## Setup Guide

- I configured both switches with the appropriate IP addresses and subnet masks for each VLAN, ensuring proper network segmentation and communication between devices on different subnets.

![Cisco- Configured the router for both IP addresses to communcate ](https://github.com/user-attachments/assets/daa7c94c-da43-480a-b72c-1408a8237491)

- Configured the DHCP server to automatically assign IP addresses to the personal computers on the network, using my DNS server as the primary DNS. Additionally, I created two VLANs to separate the servers from the four personal computers.
![CISCO dhcp server for 2 vlans](https://github.com/user-attachments/assets/f48b8109-37e0-42d4-93df-30da1b648ea0)

- Configured the DNS server to resolve 'google.com' to the web server at 192.168.2.4 and confirmed that I could access the webpage through HarryPC
![Cisco DNS](https://github.com/user-attachments/assets/f96b6b4f-b224-47e2-a906-f99e49288fd6)
![Cisco- From HarryPC we can type in google com and it brings up to the 192 168 2 4 web server](https://github.com/user-attachments/assets/5ee9b0ef-ac53-4805-b218-2326965b9fc5)

- Configured the web server to accept both HTTP and HTTPS traffic.
![Cisco- Webserver is setup for HTTP and HTTPS](https://github.com/user-attachments/assets/b1a5fd34-9100-4d7b-9ab6-6b290cc97518)

- The other three PCs on the 192.168.1.0/24 VLAN were able to receive IP addresses through DHCP. To achieve this, I configured the router with the 'ip helper-address' command pointing to 192.168.2.2, the IP address of the DHCP server. This configuration allows the router to forward broadcast traffic, such as DHCP requests, across different subnets, enabling communication between the PCs and the DHCP server
![CISCO IP address helper](https://github.com/user-attachments/assets/1bbc1c72-50ec-45e5-a70f-182d1d6e425a)

## Conclusion

- I successfully pinged all of my servers and endpoints to verify connectivity. All PCs were able to retrieve IP addresses via DHCP, and I was able to browse the web using the web server at 192.168.2.4. Using Cisco Packet Tracer, I was able to visually monitor the traffic flowing through the network. If any issues arose, I could examine the IOS model layers to identify the source of the problem and troubleshoot accordingly
