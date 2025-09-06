# 🔍 Task 1: Scan Your Local Network for Open Ports

## 📘 Objective
This task was assigned as part of an internship focused on **ethical hacking and network reconnaissance**. The goal was to perform an **active scan on the local network** using Nmap, identify open ports, analyze network traffic with Wireshark, and understand the associated risks and services.


## 🛠️ Tools Used

- **Nmap** – for network scanning and service enumeration  
- **Wireshark** – for packet capture and traffic analysis  
- **Kali Linux** – penetration testing OS (used throughout)


## 📌 Steps Performed

### 1. ✅ Install or Verify Nmap Installation
Kali Linux comes with Nmap pre-installed, but we verified and updated it:
```bash
sudo apt update
sudo apt install nmap -y
nmap --version
````

### 2. 🌐 Determine Local IP Address and Subnet

Used `ip a` to gather network interface details:

* IP Address: `192.168.248.128`
* Subnet: `/24` (i.e., `192.168.248.0/24`)


### 3. ⚡ Performed TCP SYN Scan

A stealthy TCP SYN scan was executed:

```bash
sudo nmap -sS 192.168.248.0/24
```

This scan discovered:

| IP Address      | Status | Open Ports    | Notes                   |
| --------------- | ------ | ------------- | ----------------------- |
| 192.168.248.1   | Up     | None          | Host responded          |
| 192.168.248.2   | Up     | 53 (filtered) | Likely DNS service      |
| 192.168.248.254 | Up     | None          | Host responded          |
| 192.168.248.128 | Up     | None          | Scanning machine (Kali) |



### 4. 🔎 Analyze Packets with Wireshark

**Steps:**

* Open Wireshark: `sudo wireshark`
* Select interface: `eth0`
* Apply filter:

  ```
  tcp.flags.syn == 1 && tcp.flags.ack == 0
  ```
* Observe packet behavior: SYN, SYN-ACK, RST
* Save capture as: `nmap_scan_capture.pcapng`


### 5. 🧠 Service Identification

Only port **53/tcp (DNS)** was observed (filtered), suggesting a DNS server is active.

**About Port 53 (DNS):**

* Protocol: TCP/UDP
* Service: Domain Name System
* Purpose: Resolves domain names to IP addresses


### 6. ⚠️ Identified Security Risks on Open Ports

| Threat              | Description                                           |
| ------------------- | ----------------------------------------------------- |
| DNS Amplification   | Used for DDoS attacks via spoofed requests            |
| DNS Cache Poisoning | Redirects traffic to malicious destinations           |
| Zone Transfers      | May leak internal DNS records if not restricted       |
| Information Leakage | Poor configuration may reveal hostnames or subdomains |

**Mitigation Tips:**

* Restrict DNS access to trusted IPs
* Disable unnecessary zone transfers
* Keep DNS software updated
* Monitor DNS traffic regularly


### 7. 💾 Save Results to File

Nmap scan results saved in plaintext:

```bash
sudo nmap -sS 192.168.248.0/24 -oN scan_results.txt
```

Wireshark capture saved as `.pcapng`.


## 📂 Repository Contents

| File                       | Description                            |
| -------------------------- | -------------------------------------- |
| `README.md`                | This documentation file                |
| `TASK-1.pdf`               | Full report with screenshots and steps |
| `scan_results.txt`         | Nmap TCP SYN scan output               |
| `nmap_scan_capture.pcapng` | Packet capture from Wireshark          |


## 👨‍💻 Author

**Yash Javiya**
Intern | Ethical Hacking & Cybersecurity
[GitHub Profile](https://github.com/yashjaviya111)


## 🔗 License

This repository is shared for educational and internship documentation purposes. Redistribution is prohibited without permission.
