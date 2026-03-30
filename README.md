# Kali Linux SOC Lab Environment

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Kali Linux](https://img.shields.io/badge/Kali%20Linux-2025.4-blue)](https://www.kali.org/)
[![VirtualBox](https://img.shields.io/badge/VirtualBox-7.2.6-red)](https://www.virtualbox.org/)

## 🎯 Project Overview

This project documents the **complete setup of a Kali Linux virtual machine** for **SOC (Security Operations Center) Analysts** and **Blue Team** professionals. It bridges the gap between offensive security knowledge and defensive detection.

### Why This Lab Exists
- **Understand attacker reconnaissance** by doing it yourself
- **Test detection rules** in a safe, isolated environment
- **Build realistic network simulations** without expensive hardware
- **Learn legal, ethical hacking** for defense purposes

## 🖥️ Lab Environment

| Component | Specification |
|-----------|--------------|
| **Host OS** | Windows 10/11 |
| **Hypervisor** | VirtualBox 7.2.6 |
| **Guest OS** | Kali Linux 2025.4 |
| **RAM** | 2 GB (can be increased) |
| **CPU Cores** | 2 |
| **Disk Space** | 25 GB |
| **Network Modes** | NAT, Bridged, Internal Network |

## 📸 Step-by-Step Setup (12 Screenshots)

### 1️⃣ Download VirtualBox & Extension Pack
![Step 1](screenshots/01-download-virtualbox.png)
Download VirtualBox platform package + Extension Pack for USB 3.0 and RDP support.

### 2️⃣ Create New Virtual Machine
![Step 2](screenshots/02-create-vm.png)
Name: `SOC Lab`, Type: Linux → Ubuntu (64-bit), select Kali ISO image.

### 3️⃣ Hardware Summary
![Step 3](screenshots/03-vm-summary.png)
Review default specs: 2GB RAM, 25GB storage, NAT networking.

### 4️⃣ Motherboard Settings
![Step 4](screenshots/04-motherboard-settings.png)
Configure boot order (Optical first for installation).

### 5️⃣ Increase CPU Cores
![Step 5](screenshots/05-cpu-cores.png)
Set to **2 CPUs** for better performance during scans.

### 6️⃣ Configure Bridged Network
![Step 6](screenshots/06-bridged-network.png)
Change from NAT to **Bridged Adapter** for real network access.

### 7️⃣ Optional Internal Network
![Step 7](screenshots/07-internal-network.png)
Create isolated "Home Lab" network for VM-to-VM testing.

### 8️⃣ VM Running Successfully
![Step 8](screenshots/08-vm-running.png)
Kali Linux booted and ready for action.

### 9️⃣ Verify Kali IP Address
![Step 9](screenshots/09-kali-ifconfig.png)
Run `ifconfig` - Kali shows IP `192.168.10.124` (varies by network).

### 🔟 Ping Test from Windows (Failed)
![Step 10](screenshots/10-ping-fail.png)
`ping 192.168.10.11` → 100% loss (target unreachable/firewalled).

### 1️⃣1️⃣ Ping Localhost (Success)
![Step 11](screenshots/11-ping-localhost.png)
`ping 127.0.0.1` → Works fine. Host TCP/IP stack is healthy.

### 1️⃣2️⃣ Update Kali Tools
![Step 12](screenshots/12-apt-update.png)
`sudo apt update` - ensures all security tools are latest version.

## 🛠️ Key Commands Used

| Command | Purpose |
|---------|---------|
| `ifconfig` / `ip a` | Check Kali's IP address |
| `sudo apt update` | Update package list |
| `ping <IP>` | Test network connectivity |
| `ipconfig` (Windows) | Check host IP |

## 🚀 What You Can Do Now

With this lab running, you can:

✅ **Run reconnaissance scans** (Nmap, masscan, rustscan)  
✅ **Capture and analyze traffic** (Wireshark, tcpdump)  
✅ **Test firewall rules** by scanning from Kali  
✅ **Simulate internal attackers** on bridged/internal networks  
✅ **Practice incident response** by generating real alerts  

## 📊 SOC Analyst Value Matrix

| Skill | How This Lab Develops It |
|-------|-------------------------|
| **Network Troubleshooting** | Diagnose ping failures (Step 10-11) |
| **Tool Familiarity** | Learn Kali's 600+ tools |
| **Detection Engineering** | Write Sigma rules for Nmap scans |
| **Traffic Analysis** | Capture & analyze attacker patterns |
| **Incident Response** | Simulate real attack kill chain |

## 🔐 Legal & Ethical Disclaimer

> ⚠️ **IMPORTANT**: This lab is for **AUTHORIZED** educational and professional training ONLY. Never scan networks or systems you do not own or have explicit written permission to test. Unauthorized scanning is illegal in most jurisdictions.

## 📚 Additional Resources

- [Kali Linux Official Documentation](https://www.kali.org/docs/)
- [VirtualBox Manual](https://www.virtualbox.org/manual/)
- [MITRE ATT&CK Framework](https://attack.mitre.org/)
- [SOC Analyst Training Path](https://www.sans.org/cyber-security-courses/security-operations-center-soc-analyst/)

## 📝 Author

**Owen Maake**  
- 🔬 SOC Analyst (in training)
- 🛡️ Blue Team Enthusiast
- 📧 mailto:owenlethabo28@Gmail.com
- 🔗 [(https://linkedin.com/in/yourprofile](https://www.linkedin.com/in/owen-maake-0b715a3a3/)]

## 📄 License

This project is licensed under the MIT License - see below:
