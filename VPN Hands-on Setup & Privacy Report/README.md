# VPN Hands-on Setup and Privacy Report

## Overview

This project demonstrates the practical use of a Virtual Private Network (VPN) to enhance online privacy and security. The task includes setting up a VPN, verifying IP masking and encryption, and analyzing the performance and privacy implications.

## Objectives

- Understand the role of VPNs in protecting online privacy.
- Perform hands-on setup and configuration using a free VPN (Proton VPN).
- Verify IP masking and traffic encryption.
- Assess the performance impact of VPN usage.
- Gain awareness of practical cybersecurity tools.


## Tools & Platforms Used

| Tool/Platform             | Purpose                                      |
|--------------------------|----------------------------------------------|
| Proton VPN (Free Plan)   | VPN client to secure internet traffic        |
| Google Chrome            | Browser for checking HTTPS/TLS status        |
| whatismyipaddress.com    | Check IP before and after VPN connection     |
| speedtest.net            | Measure internet speed impact                |
| Windows 11               | Operating system for VPN setup               |


## Step-by-Step Guide

### 1. Sign Up for a Reputable VPN
- Chose Proton VPN for its no-log policy and strong encryption.
- Registered on [ProtonVPN](https://protonvpn.com).

### 2. Install the VPN Client
- Downloaded and installed ProtonVPN client on Windows.
- Logged in with credentials.

### 3. Connect to a VPN Server
- Selected a free server in the Netherlands.
- Successfully connected.

### 4. Verify IP Masking
| Status       | IP Address       | Location           |
|--------------|------------------|--------------------|
| Before VPN   | 103.248.234.143  | Mahesana, India    |
| After VPN    | 93.190.141.59    | Maasdijk, Netherlands |

### 5. Confirm Traffic Encryption
- Accessed `https://www.google.com` and `https://www.wikipedia.org`.
- Verified lock icon and TLS certificates via Chrome DevTools.

### 6. Test Internet Speed

| Status       | Download | Upload | Ping |
|--------------|----------|--------|------|
| Without VPN  | 52 Mbps  | 19 Mbps| 15 ms|
| With VPN     | 31 Mbps  | 12 Mbps| 45 ms|

*Speed dropped slightly due to encryption overhead.*


## VPN Protocols & Features

| Feature             | Details                         |
|---------------------|----------------------------------|
| Encryption          | AES-256-bit                      |
| Protocols           | OpenVPN, WireGuard, IKEv2/IPSec  |
| Privacy Tools       | DNS leak protection, kill switch, no-log policy |


## Summary

### Key Learnings

- Gained hands-on understanding of VPN encryption and tunneling.
- Verified privacy enhancements using TLS and IP change.
- Evaluated performance trade-offs.
- Learned about key VPN protocols.

### Benefits

- Hides IP and location.
- Encrypts all internet traffic.
- Bypasses geo-restrictions.
- Prevents ISP and hacker surveillance.

### Limitations

- Slight internet speed reduction.
- Some websites block VPN traffic.
- Free VPNs have limited server access.
- Not fully anonymous (e.g., browser fingerprinting).

## Conclusion

This document is provided valuable practical experience with VPN technology, reinforcing cybersecurity principles such as privacy, secure communication, and protocol awareness.

**Author**: Yash Javiya  
