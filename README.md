# TheArchive — Home Network Setup

## Project Overview

This project involved replacing my ISP-provided Nokia Wi-Fi router with a self-managed home network using OPNsense, a managed Ethernet switch, and a wireless access point.

The goal was to gain hands-on experience with network hardware installation, operating system configuration, IP addressing, connectivity troubleshooting, and basic network administration.

**Project Status:** Completed

## Hardware and Software

| Component | Hardware / Software |
|---|---|
| Internet Provider | Windstream Kinetic Fiber |
| Fiber Connection | ISP-provided ONT |
| Firewall / Router | CWWK Mini PC |
| Firewall Operating System | OPNsense |
| Network Switch | D-Link DGS-1100-08PV2 |
| Wireless Network | Wi-Fi 6 Access Point |
| Network Rack | DeskPi RackMate T2 |
<img width="3000" height="4000" alt="image" src="https://github.com/user-attachments/assets/df0d5e78-b7d5-4713-9f47-8e33c5f507fc" />

## Network Topology

```text
Windstream Fiber Internet
          |
       Fiber ONT
          |
    CWWK Mini PC
      (OPNsense)
          |
  D-Link Managed Switch
          |
     +----+----+
     |    |    |
   Wi-Fi  PCs  Home Server
    AP
```

The Nokia router was removed from the network architecture. OPNsense now handles routing, firewall functionality, and LAN DHCP services.

## Implementation

### 1. OPNsense Installation

- Created a bootable OPNsense installation USB using Rufus.
- Installed OPNsense on the CWWK mini PC.
- Assigned the physical Ethernet interfaces:
  - **WAN:** ETH1 (igc1)
  - **LAN:** ETH0 (igc0)
- Accessed the OPNsense web interface and completed the setup wizard.
<img width="3431" height="972" alt="opnsensepng" src="https://github.com/user-attachments/assets/d86e6a4a-05be-4e4d-95cc-2f224736722f" />



### 2. Network Switch Setup

- Connected the OPNsense LAN interface to port 1 of the D-Link switch.
- Connected wired devices to the switch.
- Verified Ethernet link indicators and network connectivity.

### 3. Wireless Access Point

- Connected the wireless access point to the switch using Power over Ethernet (PoE).
- Configured wireless network access.
- Successfully connected a mobile device and verified internet connectivity.

## Troubleshooting and Testing

During installation, I encountered Ethernet link detection and connectivity issues.

I resolved these issues by checking physical cable connections, identifying the correct network interfaces, and verifying the WAN and LAN assignments.

After configuration, I confirmed that:

- OPNsense received a WAN IPv4 address.
- Wired devices could access the internet.
- DHCP assigned IP addresses to connected clients.
- Wireless devices could connect and access the internet.
- The OPNsense management interface was accessible.
- A backup of the OPNsense configuration was saved.

## Skills Demonstrated

- Network hardware installation and cabling
- Router and managed switch setup
- Operating system installation
- TCP/IP networking and DHCP
- Ethernet interface identification
- Wireless access point configuration
- Network connectivity troubleshooting
- Configuration backups and technical documentation

## Project Outcome

Successfully replaced my ISP-provided router with a functional, self-managed home network.

This project provided practical experience in installing, configuring, troubleshooting, and maintaining network infrastructure relevant to entry-level IT Technician and IT Support roles.
