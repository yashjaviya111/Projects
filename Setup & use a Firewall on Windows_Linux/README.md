Task 4: Setup and Use a Firewall on Linux (UFW)


## 📘 Task Objective

To gain hands-on experience in configuring a firewall using **UFW (Uncomplicated Firewall)** on a Linux system (Kali). The task involved enabling UFW, configuring port rules, and testing firewall behavior.


## 🧪 Test Environment

| Component        | Details                              |
|------------------|--------------------------------------|
| OS               | Kali Linux (Rolling)                 |
| Target IP        | 127.0.0.1 / 192.168.X.X              |
| Firewall Tool    | UFW (Uncomplicated Firewall)         |
| Privileges       | Root / Sudo                          |
| Ports Used       | 22 (SSH), 23 (Telnet)                |
| Interface        | eth0 (primary)                       |
| VM Platform      | VMware / VirtualBox (Bridged/NAT)    |


## ⚙️ Steps Performed

1. **Install & Update UFW**
   ```bash
   sudo apt update && sudo apt install ufw -y
````

2. **Enable UFW**

   ```bash
   sudo ufw enable
   ```

3. **Check UFW Status**

   ```bash
   sudo ufw status
   ```

4. **Block Telnet (Port 23)**

   ```bash
   sudo ufw deny 23
   ```

5. **Allow SSH (Port 22)**

   ```bash
   sudo ufw allow 22/tcp
   ```

6. **Verify Applied Rules**

   ```bash
   sudo ufw status verbose
   ```

7. **Test Port Blocking**

   ```bash
   nmap -p 23 localhost
   ```

8. **Remove Deny Rule (Port 23)**

   ```bash
   sudo ufw delete deny 23
   ```

9. **Disable UFW**

   ```bash
   sudo ufw disable
   ```


## 🔒 Firewall Concepts

* **Inbound Rules**: Control incoming traffic.
* **Outbound Rules**: Control outgoing traffic.
* **Default Policy**: UFW starts with default rules which can be changed.
* **Ports**: Firewall filters based on TCP/UDP port access.


## ✅ Outcome

Successfully learned how to:

* Install and manage UFW
* Add/remove firewall rules
* Test open/closed ports using `nmap`
* Understand firewall rule behavior in a live Linux environment


