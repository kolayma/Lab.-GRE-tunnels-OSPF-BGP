# 🌐 Enterprise Network: GRE, OSPF, and BGP

Connectivity scheme between central and remote offices with gateway redundancy, dynamic routing, and automated IP address assignment.
<img width="1612" height="648" alt="2026-04-27_22-01-36" src="https://github.com/user-attachments/assets/2a8419b8-a36a-4695-9a3c-35a65fb8045f" />


## 🏢 Central Office
- Multiple routers combined into a gateway redundancy group.
- **HSRP** (Hot Standby Router Protocol) is configured.
- Virtual default gateway IP address: **`192.168.1.254`**.
- Each router has its own independent internet connection.
- **IP routing** is enabled for packet forwarding between networks.
- **DHCP pools** are configured for dynamic IP address allocation to end devices within the office LAN.

## 🏭 Remote Office
- Has its own independent internet connection (separate ISP/link).
- **IP routing** is enabled for packet forwarding between networks.
- **DHCP pools** are configured for dynamic IP address allocation to end devices within the office LAN.

## 🔗 Office Interconnectivity
- Offices are connected into a corporate network via **GRE tunnels** (over public IP addresses).
- **OSPF** dynamic routing protocol is used for routing between offices inside the tunnels.

## 🌍 Global Routing (BGP)
- Autonomous Systems (AS) are interconnected using **BGP**.
- Used to exchange routes with external networks (ISPs) or between different company AS.
