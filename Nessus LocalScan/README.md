# Task 3: Vulnerability Scanning with Nessus Essentials

## 📝 Objective

This project demonstrates hands-on vulnerability assessment of a **local Kali Linux system** using **Nessus Essentials**, a widely-used free-tier vulnerability scanner developed by Tenable. The goal is to identify critical security risks, understand CVSS scores, and document mitigation strategies.


## 🛠️ Tools Used

| Tool               | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| Nessus Essentials  | Free vulnerability scanner (up to 16 IPs), ideal for students and labs.     |


## 🖥️ Test Environment

| Component           | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| OS                  | Kali Linux Rolling (kernel 6.12.25-amd64)                              |
| Host Type           | Virtual Machine (VMware)                                                |
| IP Address          | 127.0.0.1 (localhost)                                                   |
| Interfaces          | `eth0`, `docker0`, `lo`                                                 |
| Services            | Apache, SSH, Docker, Nessus                                             |
| Installed Software  | Apache 2.4.63, Node.js 20.11.0, Log4j, Python Tornado, Trivy, ClamAV   |
| Firewall            | UFW not detected                                                        |


## 🔎 Scan Procedure

### 1. Install Nessus

```bash
wget <nessus-deb-url>
sudo dpkg -i <nessus-package>
sudo systemctl start nessusd
````

### 2. Setup via Web

* Visit: `https://localhost:8834`
* Register with Tenable for an activation code
* Select **Nessus Essentials**
* Create admin credentials
* Allow plugin download (\~25 minutes)

### 3. Create and Launch Scan

* Navigate to: `Scans → New Scan → Advanced Scan`
* Name: **Localhost Full Scan**
* Target: `127.0.0.1`
* Save and launch the scan

### 4. Analyze Results

* Review summary, critical/high CVEs, and Nessus recommendations.


## ⚠️ Critical Findings

| Vulnerability                    | CVE(s)                                                                        | Severity | Fix/Recommendation                 |
| -------------------------------- | ----------------------------------------------------------------------------- | -------- | ---------------------------------- |
| Apache Log4j 1.x vulnerabilities | CVE-2019-17571, CVE-2022-23307, CVE-2020-9488, CVE-2022-23305, CVE-2022-23302 | Critical | Upgrade Log4j ≥ 2.17.1             |
| Node.js flaws                    | CVE-2024-22019, CVE-2025-23167, CVE-2024-27983                                | Critical | Upgrade Node.js ≥ 20.19.2          |
| Tornado (Python) DoS             | CVE-2025-47287                                                                | High     | Upgrade Tornado ≥ 6.5.0            |
| SSL Certificate Issue            | Self-signed certificate on port 8834                                          | Medium   | Replace with CA-issued certificate |


## 📦 Installed Components

| Software         | Version(s)                     |
| ---------------- | ------------------------------ |
| Apache HTTPD     | 2.4.63                         |
| Log4j            | 1.2.16, 2.17.1, 2.19.0, 2.24.3 |
| Node.js          | 20.11.0                        |
| Tornado (Python) | 6.4.2                          |
| Trivy            | 0.62.1                         |
| ClamAV           | 1.4.2                          |
| Containerd       | 1.7.24                         |


## 🔐 Recommendations Summary

| Action          | Recommendation                                         |
| --------------- | ------------------------------------------------------ |
| Patch Log4j     | Remove all Log4j 1.x and upgrade to secure versions    |
| Patch Node.js   | Update to Node.js ≥ 20.19.2                            |
| Fix SSL         | Use valid, trusted SSL certificates                    |
| Audit Docker    | Review Docker configurations and secure exposed ports  |
| Upgrade Tornado | Update Tornado to ≥ 6.5.0                              |
| Harden Access   | Disable unused services and restrict external exposure |


## 📈 Next Steps

1. Apply all critical and high-priority patches.
2. Replace insecure SSL certificates.
3. Review Docker configurations and restrict network access.
4. Re-run vulnerability scans to confirm remediation.
5. Document updates and maintain compliance logs.

---

## 👨‍💻 Author

**Yash Javiya**
