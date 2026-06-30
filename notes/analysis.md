## Basic Scan Findings

Target: 10.0.2.15

Host Status:
- Host is online.

Open Ports:
- 135 (MSRPC)
- 139 (NetBIOS)
- 445 (Microsoft-DS / SMB)
- 8000 (HTTP-ALT)
- 8089 (Unknown)

Observations:
- Out of the 1000 most common TCP ports, only 5 were open.
- Several Windows networking services are exposed.
- Two ports (8000 and 8089) require further investigation using service version detection.
## OS Detection

The `-O` option enables operating system detection.

Nmap analyzes how the target responds to specially crafted network packets and compares those responses against a database of operating system fingerprints.

This helps identify the probable operating system running on the target.
## Aggressive Scan (-A)

The `-A` option enables multiple advanced detection techniques in a single scan.

It performs:
- OS Detection
- Service Version Detection
- Default NSE Script Scanning
- Traceroute

Aggressive scans provide more detailed information but take longer and generate more network traffic than basic scans.
