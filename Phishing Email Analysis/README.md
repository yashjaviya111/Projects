# 🛡️ Phishing Email Analysis Report

## 📄 Overview

This project demonstrates a comprehensive analysis of a phishing email. The goal is to detect, dissect, and document the indicators of phishing to help raise awareness and improve cybersecurity defenses.


## 🔍 What is a Phishing Email?

A phishing email is a deceptive message designed to:
- Trick users into clicking malicious links or downloading infected attachments
- Steal credentials or sensitive data
- Impersonate trusted services (e.g., PayPal, banks)
- Deploy malware such as ransomware or remote access tools


## 🧪 Steps in Phishing Email Analysis

| Step                     | Description |
|--------------------------|-------------|
| 1. Header Analysis       | Examine sender, reply-to, and received paths. |
| 2. Body Inspection       | Identify urgent language, fake branding, grammar errors. |
| 3. URL Analysis          | Hover/extract links and scan using tools like VirusTotal. |
| 4. Attachment Analysis   | Check for malware in ZIP, DOCM, XLSM files. |
| 5. Technical Indicators  | Extract IOCs like IPs, hashes, domains. |
| 6. Behavioral Analysis   | Sandbox to observe actions of links/attachments. |
| 7. Threat Attribution    | Map indicators to known threat campaigns. |


## 📧 Sample Phishing Email Summary

| Field           | Detail |
|----------------|--------|
| **Subject**     | `Account Verification Required – Suspicious Login Attempt` |
| **From**        | `support@secure-paypals.com` (Spoofed) |
| **Reply-To**    | `support@paypals-verify.com` |
| **Attachment**  | `Account_Lock_Details.zip` |
| **Body Message**| Claims suspicious login from Russia and requests urgent verification |

**Red Flags Identified:**
- ⚠️ Spoofed email domain (not PayPal)
- ⚠️ Urgency: Threat of account lock within 24 hours
- ⚠️ Malicious ZIP attachment flagged by VirusTotal
- ⚠️ Mismatched and fraudulent links (`secure-paypal-confirm-portal.info`)
- ⚠️ Blacklisted IP (154.12.65.78)
- ⚠️ SPF/DKIM/DMARC checks failed


## 🔬 Technical Deep Dive

### 🔗 URL & Attachment Analysis
- **Domain**: Newly registered (2 days ago), flagged as phishing
- **Attachment**: ZIP file contains dropper trojan
- **Dynamic Behavior**: Redirects to fake PayPal login, credentials harvested via attacker-controlled PHP script

### 🛠️ Tools Used
- `MXToolbox` – Header & domain analysis
- `VirusTotal` – URL and file scanning
- `AbuseIPDB` – IP reputation check
- `Google Header Analyzer` – SPF/DKIM results


## 🛡️ Recommendations

- ✅ Enable **SPF, DKIM, DMARC** for all domains
- ✅ Use **anti-phishing filters**
- ✅ **Sandbox** suspicious emails
- ✅ Train employees in **phishing awareness**
- ✅ Enforce **multi-factor authentication (MFA)**


## 📌 Author
Yash Javiya 
(Cybersecurity & Digital Forensics Enthusiast)  
