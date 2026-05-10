# Network Security Assessment using Nmap and Wireshark

## Objective
The objective of this task is to perform a basic network security assessment using Nmap and Wireshark. The assessment helps identify open ports, running services, and network traffic behavior in order to understand potential security risks in a system or local network.

---

# Tools Used

- Nmap
- Wireshark
- Kali Linux / Ubuntu Linux

---

# Introduction

Network security assessment is an important process used to identify vulnerabilities, open ports, exposed services, and insecure network communications. In this project, Nmap was used for network scanning and service enumeration, while Wireshark was used for packet capturing and traffic analysis.

---

# Task Performed

## Part 1 — Network Scanning with Nmap

### Command Used

```bash
nmap -sV localhost
```

### Explanation
- `-sV` is used to detect service versions running on open ports.
- `localhost` scans the local machine.

### Output Saved Using

```bash
nmap -sV localhost > nmap_results.txt
```

---

# Nmap Scan Findings

| Port | State | Service | Risk |
|------|-------|---------|------|
| 22 | Open | SSH | Unauthorized remote access if weak credentials are used |
| 80 | Open | HTTP | Web server exposure and possible web vulnerabilities |
| 3306 | Open | MySQL | Database exposure if publicly accessible |

> Note: Actual ports may vary depending on the system configuration.

---

# Part 2 — Packet Capture using Wireshark

## Steps Performed

1. Opened Wireshark.
2. Selected active network interface.
3. Started packet capture.
4. Generated traffic by browsing websites.
5. Applied HTTP filter for analysis.

### Filter Used

```text
http
```

---

# Wireshark Analysis

The captured packets contained:
- HTTP GET requests
- Source and destination IP addresses
- Protocol details
- Packet lengths
- Host communication information

---

# Security Risks Identified

## 1. Open Ports
Open ports increase attack surface and may expose services to attackers.

## 2. Unencrypted HTTP Traffic
HTTP traffic is not encrypted, making it vulnerable to:
- Packet sniffing
- Session hijacking
- Data interception

## 3. Service Exposure
Running unnecessary services can lead to exploitation if vulnerabilities exist.

---

# Recommendations

- Close unused ports.
- Use HTTPS instead of HTTP.
- Configure firewall rules.
- Regularly update services and software.
- Monitor suspicious traffic.
- Use strong authentication for SSH and databases.

---

# Files Included

| File Name | Description |
|-----------|-------------|
| nmap_results.txt | Nmap scan output |
| wireshark_capture.pcap | Captured network traffic |
| README.md | Project documentation |
| screenshots/ | Screenshots of scan and analysis |

---

# Screenshots Included

- Nmap scan output
- Open ports detected
- Wireshark packet capture
- HTTP traffic filtering
- Packet analysis window

---

# Conclusion

This project demonstrated how network scanning and packet analysis can be used to identify security weaknesses in a system. Using Nmap and Wireshark, important information about services, open ports, and network traffic was analyzed. Proper security measures such as encryption, firewall configuration, and service hardening are necessary to improve overall network security.

---

# Learning Outcomes

- Learned basic network reconnaissance.
- Understood packet capturing and traffic analysis.
- Identified security risks associated with open ports.
- Gained practical experience with Nmap and Wireshark.
- Improved understanding of network security assessment techniques.
