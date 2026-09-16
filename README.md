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
<img width="717" height="401" alt="Screenshot 2026-09-15 200502" src="https://github.com/user-attachments/assets/6026f642-1d79-44d9-9e18-ea08b1d2c4f2" /> 
<img width="639" height="517" alt="Screenshot 2026-09-15 200444" src="https://github.com/user-attachments/assets/9f4cbf57-535b-4ec0-8f13-5f9982ee1bcd" />

### pfSense and Kali Network Configuration
pfSense is configured with a WAN interface using VirtualBox NAT and a static LAN interface at `192.168.56.101/24`. The Kali Linux client uses pfSense as its default gateway.

<img width="896" height="724" alt="Screenshot 2026-09-15 193549" src="https://github.com/user-attachments/assets/a3936b9d-3933-45d7-838a-b536b9f206b5" />
<img width="837" height="722" alt="Screenshot 2026-09-15 193556" src="https://github.com/user-attachments/assets/8a45b90c-0f31-45cc-b583-0cbadb048528" />
<img width="937" height="1033" alt="Screenshot 2026-09-15 171941" src="https://github.com/user-attachments/assets/ffd21a16-bce1-485e-9c0f-6cefafa8d825" />

### pfBlockerNG DNSBL Configuration
Configured a custom DNSBL list containing YouTube-related domains to enforce domain-based filtering.

<img width="942" height="758" alt="Screenshot 2026-09-15 193609" src="https://github.com/user-attachments/assets/a747662b-b20b-49f5-ac9e-30f094ddec5e" />
<img width="944" height="675" alt="Screenshot 2026-09-15 193616" src="https://github.com/user-attachments/assets/4c677618-b034-43df-8684-610c1654c5c7" />
### Final Validation
Google remains accessible while YouTube is blocked, confirming selective DNS filtering through pfSense.











 











