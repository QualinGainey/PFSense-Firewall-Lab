# pfSense Firewall & DNS Filtering Lab

## Project Overview
Built a virtual firewall lab using pfSense, Kali Linux, VirtualBox, and pfBlockerNG to practice firewall administration, routing, NAT, DNS filtering, and troubleshooting.

The goal of the lab was to route a Kali Linux client through pfSense and selectively block YouTube while maintaining access to other websites such as Google.

## Lab Environment
- pfSense Community Edition
- Kali Linux
- Oracle VirtualBox
- pfBlockerNG / DNSBL

## Network Topology
Kali Linux (192.168.56.102)
        |
        v
pfSense LAN (192.168.56.101)
        |
        v
pfSense WAN (VirtualBox NAT)
        |
        v
Internet

## Configuration
- Configured separate WAN and LAN interfaces on pfSense
- Assigned a static LAN address of 192.168.56.101/24
- Configured Kali Linux to use pfSense as its default gateway
- Configured WAN connectivity through VirtualBox NAT
- Configured firewall rules and aliases
- Enabled pfSense DNS Resolver
- Installed and configured pfBlockerNG
- Implemented DNSBL domain filtering

## DNS Filtering
Configured Kali Linux to use pfSense as its DNS server.

Used pfBlockerNG DNSBL to restrict access to YouTube-related domains while allowing other internet traffic.

## Troubleshooting
During the lab, I troubleshot:
- Missing WAN default routes
- DNS resolution failures
- VirtualBox adapter configuration
- Kali Linux default gateway configuration
- pfSense WAN connectivity
- Firewall rule placement
- FQDN/IP-based blocking limitations
- DNSBL configuration

## Results
- Kali Linux successfully routed through pfSense
- General internet connectivity remained available
- Google remained accessible
- YouTube access was successfully blocked using DNS filtering

## What I Learned
This lab gave me hands-on experience with:
- Firewall policy
- Routing and NAT
- DNS resolution
- DNS filtering
- Virtual networking
- Traffic flow
- Network troubleshooting

## Screenshots
<img width="717" height="401" alt="Screenshot 2026-09-15 200502" src="https://github.com/user-attachments/assets/6026f642-1d79-44d9-9e18-ea08b1d2c4f2" /> <img width="937" height="1033" alt="Screenshot 2026-09-15 171941" src="https://github.com/user-attachments/assets/a056c915-0aea-47f4-85c6-41280c8bfffc" /> <img width="639" height="517" alt="Screenshot 2026-09-15 200444" src="https://github.com/user-attachments/assets/352e6a01-0487-44a3-813d-023511fb520e" /> <img width="925" height="840" alt="Screenshot 2026-09-15 200112" src="https://github.com/user-attachments/assets/7c1ca280-34f3-4615-9739-943e794459c0" /> <img width="837" height="722" alt="Screenshot 2026-09-15 193556" src="https://github.com/user-attachments/assets/cad0023c-d6fa-4be5-ab52-6a36bb1d47a6" /> <img width="944" height="675" alt="Screenshot 2026-09-15 193616" src="https://github.com/user-attachments/assets/5287a988-ad07-4b06-ab21-b2ba94912009" /> <img width="942" height="758" alt="Screenshot 2026-09-15 193609" src="https://github.com/user-attachments/assets/e074d6a2-b124-427f-a927-f598d2fd5a7a" />






 











