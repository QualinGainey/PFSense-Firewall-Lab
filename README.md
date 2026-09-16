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
↓  
pfSense LAN (192.168.56.101/24)  
↓  
pfSense Firewall  
↓  
pfSense WAN (VirtualBox NAT)  
↓  
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
- Successfully routed the Kali Linux client through pfSense
- Maintained normal internet connectivity through the firewall
- Verified Google and other permitted websites remained accessible
- Successfully blocked YouTube using pfBlockerNG DNSBL
- Verified DNS-based filtering without disrupting general web access

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
<img width="717" height="401" alt="Screenshot 2026-09-15 200502" src="https://github.com/user-attachments/assets/6026f642-1d79-44d9-9e18-ea08b1d2c4f2" /> <img width="639" height="517" alt="Screenshot 2026-09-15 200444" src="https://github.com/user-attachments/assets/435acfa6-1d57-423e-aa2e-9f5c23499586" /> <img width="896" height="724" alt="Screenshot 2026-09-15 193549" src="https://github.com/user-attachments/assets/01f0b5e9-7c4f-417e-8316-67fc28ae40fc" /> <img width="837" height="722" alt="Screenshot 2026-09-15 193556" src="https://github.com/user-attachments/assets/4dc4e093-50d2-4f96-beb2-ffd4beb4b97f" /> <img width="942" height="758" alt="Screenshot 2026-09-15 193609" src="https://github.com/user-attachments/assets/2cd95897-46e1-47cd-aad7-fb1101be73f1" /> <img width="944" height="675" alt="Screenshot 2026-09-15 193616" src="https://github.com/user-attachments/assets/9b4e150d-25a4-46bf-a5ee-d18342037867" />










 











