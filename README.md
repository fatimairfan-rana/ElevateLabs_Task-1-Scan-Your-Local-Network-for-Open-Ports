# ElevateLabs_Task-1-Scan-Your-Local-Network-for-Open-Ports
# 🔐 Cyber Security Internship – Task 1
## Local Network Port Scanning Using Nmap

![Kali Linux](https://img.shields.io/badge/OS-Kali%20Linux-blue?logo=kalilinux)
![Nmap](https://img.shields.io/badge/Tool-Nmap-green)
![Cyber Security](https://img.shields.io/badge/Domain-Cybersecurity-red)
![Status](https://img.shields.io/badge/Status-In%20Progress-orange)

---

## 📌 Project Overview

This project is part of my Cyber Security Internship.

The objective of this task is to perform network reconnaissance by scanning an authorized local network using **Nmap (Network Mapper)** to identify active devices, open ports, and running network services.

This exercise helps develop practical knowledge of network security, port scanning, TCP SYN scanning, and identifying potential security risks associated with exposed network services.

## 🎯 Objectives

- Discover active devices on a local network.
- Identify open TCP ports.
- Understand services running on discovered ports.
- Perform TCP SYN scanning using Nmap.
- Analyze potential security risks associated with open ports.
- Understand the role of firewalls in network security.
- Save and document scan results.
- Learn basic network reconnaissance techniques.

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Operating System |
| Nmap | Network discovery and port scanning |
| Wireshark | Network packet analysis (optional) |
| VS Code | Documentation and project management |
| Git & GitHub | Version control and project submission |

## 📖 Key Concepts

### 1. Network Reconnaissance

Network reconnaissance is the process of collecting information about devices, network services, and potential entry points within a network.

### 2. Open Ports

An open port indicates that a service is listening and accepting network connections.

Some common ports include:

| Port | Service | Description |
|---|---|---|
| 21 | FTP | File Transfer Protocol |
| 22 | SSH | Secure Shell |
| 23 | Telnet | Remote Access |
| 53 | DNS | Domain Name System |
| 80 | HTTP | Hypertext Transfer Protocol |
| 443 | HTTPS | Secure Web Communication |
| 445 | SMB | Server Message Block |
| 3389 | RDP | Remote Desktop Protocol |

### 3. TCP SYN Scan

A TCP SYN scan is a half-open scanning technique used by Nmap to identify open TCP ports.

It works by sending SYN packets to target ports and analyzing the responses.

- SYN-ACK: Generally indicates an open port.
- RST: Generally indicates a closed port.
- No response or certain ICMP errors: May indicate a filtered port.

## ⚙️ Practical Implementation

### Step 1: Verify Nmap Installation

Check whether Nmap is installed:

```bash
nmap --version
```

If Nmap is not installed:

```bash
sudo apt update
sudo apt install nmap -y
```

### Step 2: Identify Local IP Address

Use the following command:

```bash
ip addr
```

Alternatively:

```bash
ip route
```

Identify the local IPv4 address and network range.

Example:

```text
Local IP: 192.168.1.105
Gateway: 192.168.1.1
Network Range: 192.168.1.0/24
```

*Note: These are example values. Use your actual local network information.*

### Step 3: Perform TCP SYN Scan

Execute the following command against your authorized local network:

```bash
sudo nmap -sS 192.168.1.0/24
```

**Command Explanation:**

- `sudo`: Executes Nmap with elevated privileges.
- `nmap`: Starts the Network Mapper tool.
- `-sS`: Performs a TCP SYN scan.
- `192.168.1.0/24`: Specifies the target network range.

### Step 4: Save Scan Results

Save the results in text format:

```bash
sudo nmap -sS 192.168.1.0/24 -oN scan-results/scan_results.txt
```

Save the results in XML format:

```bash
sudo nmap -sS 192.168.1.0/24 -oX scan-results/scan_results.xml
```

Replace the example network range with your actual authorized network range.

## 🔍 Security Analysis

Open ports may introduce security risks when the associated services are unnecessary, outdated, or improperly configured.

| Port | Potential Security Concern |
|---|---|
| 21 | Unencrypted FTP communication |
| 22 | Weak SSH authentication |
| 23 | Unencrypted Telnet communication |
| 80 | Unencrypted HTTP traffic |
| 445 | Exposed SMB file-sharing services |
| 3389 | Unauthorized RDP access |

**Important:** An open port does not automatically mean a system is vulnerable. Security risks depend on service configuration, software versions, authentication, and network exposure.

## 🛡️ Security Recommendations

- Disable unnecessary network services.
- Close unused ports.
- Configure firewall rules.
- Use strong passwords and multi-factor authentication.
- Keep network services updated.
- Restrict remote access to trusted devices.
- Replace insecure protocols with secure alternatives.
- Monitor network traffic regularly.
- Conduct periodic authorized security assessments.

## 📊 Practical Results

The following section should be updated after completing the actual scan.

| Parameter | Actual Result |
|---|---|
| Operating System | Kali Linux |
| Scanning Tool | Nmap |
| Local IP Address | [Insert Actual IP] |
| Network Range | [Insert Actual Range] |
| Active Devices | [Insert Actual Count] |
| Open Ports | [Insert Actual Ports] |
| Identified Services | [Insert Actual Services] |

### Observations

[Add observations based on your actual Nmap scan output.]

### Findings

[Document identified open ports, running services, and any potential security concerns.]

## 📸 Screenshots & Evidence

Screenshots of the practical implementation will be added to the `screenshots/` directory.

Suggested evidence:

1. Nmap version verification.
2. Local IP address identification.
3. Nmap TCP SYN scan output.
4. Identified open ports and services.
5. Wireshark packet analysis (optional).

## 🎓 Learning Outcomes

Through this task, I aim to develop practical knowledge of:

- Network reconnaissance.
- IP addressing and subnet ranges.
- TCP SYN scanning.
- Port and service identification.
- TCP and UDP protocols.
- Network exposure assessment.
- Basic firewall security.
- Network traffic analysis.

## 📝 Interview Questions

1. What is an open port?
2. How does Nmap perform a TCP SYN scan?
3. What risks are associated with open ports?
4. Explain the difference between TCP and UDP scanning.
5. How can open ports be secured?
6. What is the role of a firewall?
7. What is port scanning and why do attackers perform it?
8. How does Wireshark complement port scanning?

## 📚 References

- [Nmap Official Website](https://nmap.org/)
- [Nmap Documentation](https://nmap.org/book/man.html)
- [Wireshark Official Website](https://www.wireshark.org/)
- [Kali Linux Official Website](https://www.kali.org/)
- [RFC Editor](https://www.rfc-editor.org/)

## ⚖️ Ethical Disclaimer

All scanning activities must be performed only on networks and devices for which proper authorization has been obtained.

This project is intended for educational purposes and authorized cybersecurity assessments.

---

## 👩‍💻 Author

**Cyber Security Internship Participant**

**Project:** Task 1 – Local Network Port Scanning Using Nmap

**Repository:** CyberSecurity-Internship-Task-1

---

⭐ If you find this project useful, feel free to explore the repository and its documentation.
