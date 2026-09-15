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
