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
<img width="783" height="423" alt="Screenshot 2026-09-15 193542" src="https://github.com/user-attachments/assets/fdcef106-79d3-4192-aca3-201e174f048f" /> <img width="937" height="1033" alt="Screenshot 2026-09-15 171941" src="https://github.com/user-attachments/assets/407dd0a0-0760-494d-a223-4fa80f3ff27f" /> <img width="630" height="233" alt="Screenshot 2026-09-15 193718" src="https://github.com/user-attachments/assets/59ffbc7b-ec44-47c1-8705-07bcd8a6241e" /> <img width="837" height="722" alt="Screenshot 2026-09-15 193556" src="https://github.com/user-attachments/assets/22b33ea9-7b9b-459e-9574-39691f9118ef" /> <img width="896" height="724" alt="Screenshot 2026-09-15 193549" src="https://github.com/user-attachments/assets/bc854818-8389-4fda-8cec-9751909157be" /> <img width="942" height="758" alt="Screenshot 2026-09-15 193609" src="https://github.com/user-attachments/assets/40c95db7-7630-42d6-8c32-edf3fafd6f1c" /> <img width="944" height="675" alt="Screenshot 2026-09-15 193616" src="https://github.com/user-attachments/assets/5fd9a1f9-6f3e-4f30-ba20-e1df0d121fa7" /> <img width="639" height="517" alt="image" src="https://github.com/user-attachments/assets/617cdf07-bd81-464e-9a95-e8faea3ad929" /> <img width="717" height="401" alt="image" src="https://github.com/user-attachments/assets/012284eb-3479-4158-8b92-ab1a62299b39" />











