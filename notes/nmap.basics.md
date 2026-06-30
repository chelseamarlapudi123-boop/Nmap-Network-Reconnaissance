# Nmap Basics

## What is Nmap?
Nmap (Network Mapper) is an open-source network scanning tool used to discover hosts, identify open ports, detect running services, and gather information about devices on a network.

## Why is it used?
- Network discovery
- Port scanning
- Service detection
- Operating system detection
- Security assessments
- Troubleshooting

## Who uses Nmap?
- SOC Analysts
- Penetration Testers
- Security Engineers
- System Administrators
- Incident Responders
## What is a Port?

A port is a numbered communication endpoint on a computer. Services listen on specific ports so other devices can communicate with them.

## Port States

- Open – A service is actively listening.
- Closed – No service is listening on the port.
- Filtered – A firewall or security device is blocking access.

## Common Ports

22 - SSH
53 - DNS
80 - HTTP
443 - HTTPS
445 - SMB
3389 - RDP

## Host Discovery

Host discovery is the process of determining whether a device is online before scanning its ports.

Nmap first checks if the target responds. If the host is up, Nmap proceeds with further scans. If the host does not respond, Nmap may stop scanning unless instructed otherwise.
