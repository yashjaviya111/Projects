# Task 5: Wireshark Network Traffic Analysis

## Objective
This task aims to provide practical experience in capturing and analyzing real-time network traffic using Wireshark. By the end of this task, the learner will:
- Understand how data flows across a network.
- Identify and interpret various network protocols.
- Apply filters to isolate relevant data from large packet captures.
- Gain insights into packet structure and protocol behavior for cybersecurity use.

## Tools and Environment
| Component         | Description                                  |
|------------------|----------------------------------------------|
| **Wireshark**     | Open-source network packet analyzer          |
| **Operating System** | Windows 10 (64-bit)                         |
| **Traffic Generator** | Web browsers (Chrome), ping command in CMD |
| **Network**       | Wi-Fi (private network)                      |

## Task Execution Steps

### Step 1: Install Wireshark
- Downloaded from: [https://www.wireshark.org/download.html](https://www.wireshark.org/download.html)
- Installed Npcap for Windows-based packet capturing.
- Launched Wireshark successfully.

### Step 2: Start Packet Capture
- Opened the Wi-Fi interface.
- Started live capture using the blue shark fin icon.
- Observed real-time packet flow.

### Step 3: Generate Network Traffic
- Visited websites:
  - https://www.google.com
  - https://www.github.com
  - https://www.example.com
- Used command: `ping 8.8.8.8 -n 5` to generate ICMP traffic.

### Step 4: Stop Capture
- Stopped after 1 minute using the red square icon.
- Saved the capture as `task5_capture.pcapng`.

### Step 5: Filter and Analyze Network Traffic
Opened the capture file and applied various filters:

#### Protocol Filters
- `tcp` – View all TCP traffic
- `http` – View unencrypted web traffic (port 80)
- `dns` – Show DNS resolution queries and responses
- `icmp` – View ping request/replies
- `arp` – Show local IP-to-MAC resolution
- `tls` – Analyze encrypted HTTPS traffic

#### Combined Filters Example
```text
tcp or dns
````

#### Useful Filters

| Filter                     | Description                           |
| -------------------------- | ------------------------------------- |
| `http`                     | HTTP packets only                     |
| `tcp`                      | All TCP traffic                       |
| `udp`                      | All UDP traffic                       |
| `icmp`                     | Ping-related packets                  |
| `dns`                      | DNS resolution data                   |
| `ip.addr == 8.8.8.8`       | Traffic to/from Google DNS            |
| `tcp.port == 443`          | HTTPS traffic (TLS over TCP port 443) |
| `frame contains "example"` | Finds packets with the word "example" |

## Protocols Observed

| Protocol  | Layer       | Role                     | Observation                             |
| --------- | ----------- | ------------------------ | --------------------------------------- |
| HTTP      | Application | Web browsing (port 80)   | GET requests before HTTPS redirection   |
| HTTPS/TLS | Application | Secure browsing          | TLS handshake; encrypted payload        |
| DNS       | Application | Domain resolution        | DNS queries for visited domains         |
| ICMP      | Network     | Diagnostics              | Echo request/reply, TTL, response time  |
| TCP       | Transport   | Reliable communication   | Three-way handshake (SYN, SYN/ACK, ACK) |
| UDP       | Transport   | Lightweight transmission | DNS uses UDP for queries                |
| ARP       | Link        | IP-to-MAC mapping        | Resolved local network addresses        |

## Outcome

* Gained hands-on experience with Wireshark and packet-level data.
* Learned protocol behavior and network communication structure.
* Acquired foundational skills for network security and troubleshooting.

## Author
**Yash Javiya**
