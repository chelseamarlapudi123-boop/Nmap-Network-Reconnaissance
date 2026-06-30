# 🔍 Nmap Network Reconnaissance & Service Enumeration

## 📖 Project Overview

This project demonstrates the use of **Nmap (Network Mapper)** to perform network reconnaissance and service enumeration in a controlled Windows virtual lab environment.

The project focuses on identifying active hosts, discovering open TCP ports, detecting running services, identifying the operating system, and understanding how different Nmap scan techniques provide progressively more detailed information about a target system.

The purpose of this project is to gain hands-on experience with one of the most widely used network reconnaissance tools while documenting the process in a professional manner suitable for a cybersecurity portfolio.

---

# 🎯 Objectives

- Learn the fundamentals of Nmap.
- Perform host discovery.
- Identify open TCP ports.
- Detect running services and service versions.
- Identify the target operating system.
- Understand aggressive scanning techniques.
- Analyze scan results.
- Document findings professionally.

---

# 🛠️ Skills Demonstrated

- Network Reconnaissance
- Port Scanning
- Service Enumeration
- Operating System Detection
- TCP/IP Networking
- Windows Administration
- Cybersecurity Documentation
- Information Gathering

---

# 🧪 Lab Environment

| Component | Details |
|-----------|---------|
| Operating System | Windows 11 Virtual Machine |
| Virtualization | Oracle VirtualBox |
| Network Mode | NAT |
| Tool | Nmap 7.99 |
| Terminal | Windows Command Prompt |

---

# 🌐 Network Setup

```
Host PC
      │
      │
VirtualBox
      │
Windows 11 VM
(10.0.2.15)
```

Target scanned:

```
10.0.2.15
```

---

# 🛠️ Tool Used

## Nmap

Nmap (Network Mapper) is an open-source network scanning tool used to discover hosts, identify open ports, detect running services, identify operating systems, and perform network reconnaissance.

It is widely used by:

- SOC Analysts
- Penetration Testers
- Security Engineers
- System Administrators
- Incident Responders

---

# 🔎 Nmap Scans Performed

---

## 1. Basic TCP Scan

### Command

```bash
nmap 10.0.2.15
```

### Purpose

Perform a basic scan of the target to determine:

- Whether the host is online
- Which TCP ports are open
- Which ports are closed

### Findings

- Host was online.
- 1000 common TCP ports were scanned.
- 995 ports were closed.
- 5 ports were open.

### Screenshot

```
screenshots/03-basic-scan.png
```

---

## 2. Service Version Detection

### Command

```bash
nmap -sV 10.0.2.15
```

### Purpose

Identify the services running on each open port and determine their versions whenever possible.

### Why It Matters

Knowing the exact service and version helps security professionals:

- Identify outdated software
- Detect exposed services
- Investigate vulnerabilities
- Improve asset visibility

### Screenshot

```
screenshots/04-service-scan.png
```

---

## 3. Operating System Detection

### Command

```bash
nmap -O 10.0.2.15
```

### Purpose

Determine the operating system running on the target by comparing packet responses with Nmap's OS fingerprint database.

### Why It Matters

Operating system identification helps security analysts:

- Understand the target environment
- Identify OS-specific services
- Prioritize investigations
- Assess potential vulnerabilities

### Screenshot

```
screenshots/05-os-detection.png
```

---

## 4. Aggressive Scan

### Command

```bash
nmap -A 10.0.2.15
```

### Purpose

Perform advanced reconnaissance using multiple detection techniques.

The aggressive scan performs:

- Service Version Detection
- Operating System Detection
- Default NSE Script Scanning
- Traceroute

### Why It Matters

Aggressive scans provide more detailed information but generate more network traffic and are more likely to be detected by security monitoring tools.

### Screenshot

```
screenshots/06-aggressive-scan.png
```

---

# 📊 Scan Results

The scans identified the following open TCP ports:

| Port | Service | Description |
|------|----------|-------------|
| 135 | MSRPC | Microsoft Remote Procedure Call |
| 139 | NetBIOS | Windows NetBIOS Session Service |
| 445 | Microsoft-DS | SMB File Sharing |
| 8000 | HTTP-ALT | Alternate HTTP Service |
| 8089 | Unknown | Additional Network Service |

---

# 📝 Key Findings

- The target host was successfully identified as online.
- Nmap discovered five open TCP ports.
- Windows networking services such as MSRPC, NetBIOS, and SMB were identified.
- Additional services were detected on ports 8000 and 8089.
- Service detection provided more information than the basic scan.
- OS detection demonstrated how Nmap identifies operating systems through fingerprint analysis.
- Aggressive scanning combined multiple reconnaissance techniques into a single operation.

---

# 📚 What I Learned

Through this project I learned:

- What Nmap is and how it is used in cybersecurity.
- The purpose of host discovery.
- The difference between open, closed, and filtered ports.
- How TCP port scanning works.
- How service version detection works.
- How operating system fingerprinting works.
- The differences between basic scans and aggressive scans.
- How reconnaissance supports security investigations.
- The importance of documenting findings in a structured manner.

---

# 📂 Project Structure

```
Nmap-Network-Reconnaissance/

│── README.md

│── screenshots/
│   ├── nmap-version.png
│   ├── basic-scan.png
│   ├── service-scan.png
│   ├── os-detection.png
│   └── aggressive-scan.png

│── notes/
│   ├── nmap-basics.md
│   └── analysis.md
```

---

# 🚀 Future Improvements

Future enhancements for this project include:

- Perform UDP scanning.
- Scan multiple hosts in a lab environment.
- Explore advanced NSE scripts.
- Compare scan results across Windows and Linux systems.
- Integrate scan results into SIEM tools such as Splunk.
- Automate reporting using Nmap output formats.

---

# 📖 References

- https://nmap.org/
- https://nmap.org/book/
- Official Nmap Documentation

---

# ⚠️ Disclaimer

This project was performed in a controlled lab environment on systems that I own or have permission to test.

Nmap should only be used on networks and systems where explicit authorization has been granted.
