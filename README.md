# College-Centric-Network-Networking-Project– Bahria University 

## Overview
This project demonstrates the design and implementation of a scalable, secure, and efficient college-centric network. Engineered for Bahria University's Islamabad Campus, the network integrates RIP and EIGRP routing protocols, route redistribution, DHCP, and DNS services to optimize connectivity across multiple departments. Additionally, a web server provides access to LMS/CMS resources via HTTP and HTML/CSS interfaces.

## Features
- Multi-protocol routing (RIPv2 and EIGRP) configured for performance and scalability.
- Route redistribution ensures seamless communication between protocols.
- DHCP setup for dynamic IP allocation across departmental scopes.
- DNS configuration enables human-readable domain resolution.
- Route summarization reduces routing table complexity.
- Support for heterogeneous devices (PCs, laptops, smartphones, printers).
- Web-based services including DNS and HTTP hosted centrally.
- Integration of fiber-optic and wireless mediums across the infrastructure.
- Logical and physical topology mapped with layered architecture.

## Requirements
Make sure you have the following before testing or replicating the setup:
- Cisco Packet Tracer or GNS3
- Basic understanding of routing protocols and network configuration
- Hardware devices as per lab simulation (routers, switches, end devices)
- Internet access to simulate DNS and web services

## Installation & Setup
1. Clone the project repository:
   ```bash
   git clone <repository-url>
   ```
2. Open your network simulation tool (e.g., Cisco Packet Tracer).
3. Load the topology and configuration files manually or replicate using provided code blocks.
4. Verify connectivity between departments using ping and traceroute.
5. Access the central web server from lab devices using domain names.

## Project Structure
```
├── Topology Diagram
│   ├── Logical Architecture
│   └── Physical Mapping
├── Configs
│   ├── Routing Protocols (RIP, EIGRP)
│   ├── Route Redistribution
│   ├── DHCP & DNS
│   └── Web Server Setup
├── Code Explanation
└── Documentation
    ├── Project Report
    └── References
```

## Usage
- Navigate across campus departments using IP routing and DNS resolution.
- Student PCs in the lab can access web-based learning platforms via HTTP.
- Admin devices use DHCP to obtain IPs dynamically.
- Faculty can manage class-related resources through the web server.
- Mobile and wireless access points ensure campus-wide reachability.

 
## Hardware Diagrams:

<img width="412" height="775" alt="image" src="https://github.com/user-attachments/assets/190f04ea-c93a-4d89-8a5e-ce76f2d19535" />

## Logical Diagrams:

<img width="1107" height="616" alt="image" src="https://github.com/user-attachments/assets/f3636e21-d336-4dc4-b897-f433914d820e" />

 ## Screenshots
<img width="412" height="835" alt="image" src="https://github.com/user-attachments/assets/2b98fe4e-e403-4da1-b1d1-00d292e16280" />
<img width="536" height="566" alt="image" src="https://github.com/user-attachments/assets/781d9277-952d-4d31-b570-cf3f56ee7cc7" />

<img width="532" height="156" alt="image" src="https://github.com/user-attachments/assets/deef652e-f439-4e8f-b576-4e1bfef91af5" /> 


 
## Configuration Samples:
```markdown
## Routing Information Protocol (RIP) Version 2:
- Router(config)#router rip
- Router(config-router)#version 2
- Router(config-router)#network 192.168.10.0
- Router(config-router)#network 10.0.0.0
- Route (RIP) timers:
- Router(config)#router rip
- Router(config-router)#version 2
- Router(config-router)#timers basic 40 50 60 40
- Router Summarization:
- Router(config)#router rip
- Router(config-router)#no auto-summary

## Eigrp Implementation:
- Router3(config)#router Eigrp 100
- Router3(config-router)#network 10.1.2.0
- Router3(config-router)#no auto-summary
- Route Redistribution between RIP and Eigrp:
- Router2(config)#router rip
- Router2(config-router)#redistribute eigrp 100 metric 1
- Router2(config)#router eigrp 100
- Router2(config-router)#redistribute rip metric 1 0 1 1 1

## DHCP:
- Router2(config)# ip dhcp excluded-address 192.168.10.1
- Router2(dhcp-config)# network 192.168.11.0 255.255.255.0
- Router2(dhcp-config)# default-router 192.168.2.1

## DNS:
- Router2(dhcp-config)# network 192.168.11.0 255.255.255.0
- Router2(dhcp-config)# default-router 192.168.10.1
- Router2(dhcp-config)# dns-serve 8.8.8.8 //Dns Server configuration
  ```
## Conclusion
This project serves as a blueprint for campus-wide network deployment emphasizing modularity, security, and performance. With robust routing logic and integrated web services, it aims to support the digital and academic needs of a modern educational institution.
 
