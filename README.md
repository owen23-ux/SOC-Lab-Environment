# 🛡️ Kali Linux SOC Lab Environment

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Kali Linux](https://img.shields.io/badge/Kali%20Linux-2025.4-blue)](https://www.kali.org/)
[![VirtualBox](https://img.shields.io/badge/VirtualBox-7.2.6-red)](https://www.virtualbox.org/)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen)]()
[![SOC](https://img.shields.io/badge/SOC-Analyst%20Training-orange)]()
[![Blue Team](https://img.shields.io/badge/Team-Blue%20Team-blue)]()

> *"To defend effectively, you must think like an attacker."* — My SOC Journey

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [Why I Built This Lab](#-why-i-built-this-lab)
- [Lab Environment](#-lab-environment)
- [Step-by-Step Setup](#-step-by-step-setup)
- [Key Commands I Used](#-key-commands-i-used)
- [What I Can Now Do](#-what-i-can-now-do)
- [SOC Analyst Value Matrix](#-soc-analyst-value-matrix)
- [Critical Lessons Learned](#-critical-lessons-learned)
- [What's Next](#-whats-next)
- [Connect With Me](#-connect-with-me)
- [Legal Disclaimer](#-legal-disclaimer)

---

## 🎯 Project Overview

This repository documents my **complete journey setting up a Kali Linux virtual machine** as an aspiring **SOC Analyst** and **Blue Team** professional. Instead of just reading about attacks, I built this lab to:

- 🔍 **Run real reconnaissance scans** in a safe environment
- 🛡️ **Test detection rules** against actual attack patterns
- 📡 **Capture and analyze malicious traffic** with Wireshark
- 🧪 **Simulate internal attackers** without expensive hardware
- ⚖️ **Learn legal, ethical hacking** for defense purposes

---

## 💡 Why I Built This Lab

As a SOC Analyst in training, I realized that reading threat reports wasn't enough. I needed to:

| Challenge | How This Lab Solved It |
|-----------|------------------------|
| **Abstract attack concepts** | I can now *see* and *execute* attacks myself |
| **No safe testing environment** | Isolated VMs let me break things without consequences |
| **Expensive hardware requirements** | Runs entirely on my existing Windows laptop |
| **Limited detection practice** | I generate my own alerts and practice response |

---

## 🖥️ Lab Environment

| Component | My Configuration |
|-----------|------------------|
| **Host OS** | Windows 11 |
| **Hypervisor** | VirtualBox 7.2.6 |
| **Guest OS** | Kali Linux 2025.4 |
| **RAM Allocated** | 2 GB (upgradable) |
| **CPU Cores** | 2 |
| **Disk Space** | 25 GB |
| **Network Modes Used** | NAT, Bridged, Internal Network |

---

## 📸 Step-by-Step Setup

> *I documented every step with screenshots. Here's what I did and what I learned.*

### 1️⃣ Download VirtualBox & Extension Pack
![Step 1](screenshots/01-download-virtualbox.png)
> Downloaded VirtualBox platform package + Extension Pack for USB 3.0 and RDP support.

### 2️⃣ Create New Virtual Machine
![Step 2](screenshots/02-create-vm.png)
> Named it `SOC Lab`, Type: Linux → Ubuntu (64-bit), selected Kali ISO.

### 3️⃣ Hardware Summary
![Step 3](screenshots/03-vm-summary.png)
> Default specs: 2GB RAM, 25GB storage, NAT networking.

### 4️⃣ Motherboard Settings
![Step 4](screenshots/04-motherboard-settings.png)
> Configured boot order (Optical first for installation).

### 5️⃣ Increase CPU Cores ⚡
![Step 5](screenshots/05-cpu-cores.png)
> **Key tweak:** Set to **2 CPUs** for better performance during scans.

### 6️⃣ Configure Bridged Network 🌐
![Step 6](screenshots/06-bridged-network.png)
> **Critical moment:** Changed from NAT to **Bridged Adapter** for real network access.

### 7️⃣ Optional Internal Network 🔒
![Step 7](screenshots/07-internal-network.png)
> Created isolated "Home Lab" network for VM-to-VM testing.

### 8️⃣ VM Running Successfully ✅
![Step 8](screenshots/08-vm-running.png)
> Kali Linux booted and ready for action!

### 9️⃣ Verify Kali IP Address
![Step 9](screenshots/09-kali-ifconfig.png)
> Ran `ifconfig` - Kali showed IP `192.168.10.124` on my home network.

### 🔟 Ping Test from Windows (Failed) ❌
![Step 10](screenshots/10-ping-fail.png)
> `ping 192.168.10.11` → 100% loss. **This failure taught me more than success would have.**

### 1️⃣1️⃣ Ping Localhost (Success) ✅
![Step 11](screenshots/11-ping-localhost.png)
> `ping 127.0.0.1` → Works fine. Host TCP/IP stack is healthy.

### 1️⃣2️⃣ Update Kali Tools 📦
![Step 12](screenshots/12-apt-update.png)
> `sudo apt update` - Ensured all security tools are latest version.

---

## 🛠️ Key Commands I Used

| Command | Purpose | My Learning |
|---------|---------|-------------|
| `ifconfig` / `ip a` | Check Kali's IP address | Quickly identifying network position |
| `sudo apt update` | Update package list | Keeping tools current is critical |
| `ping <IP>` | Test network connectivity | Diagnosing firewall vs. connectivity issues |
| `ipconfig` (Windows) | Check host IP | Correlating host and VM addresses |

---

## 🚀 What I Can Now Do

With this lab running, I've gained hands-on experience in:

<table>
<tr>
<td width="50%">

**✅ Reconnaissance Skills**
- Run Nmap scans from Kali
- Execute masscan for fast discovery
- Use rustscan for efficient port scanning

</td>
<td width="50%">

**✅ Traffic Analysis**
- Capture attacks in Wireshark
- Distinguish normal vs. malicious traffic
- Export PCAPs for deeper analysis

</td>
</tr>
<tr>
<td width="50%">

**✅ Detection Engineering**
- Test firewall rules effectiveness
- Write Sigma rules for Nmap scans
- Generate real security alerts

</td>
<td width="50%">

**✅ Incident Response**
- Simulate attack kill chain
- Practice response procedures
- Investigate my own "attacks"

</td>
</tr>
</table>

---

## 📊 SOC Analyst Value Matrix

| Skill | How This Lab Develops It | 🎯 Proficiency Gained |
|-------|-------------------------|----------------------|
| **Network Troubleshooting** | Diagnosing ping failures (Step 10) | 🔥🔥🔥🔥 |
| **Tool Familiarity** | Learning Kali's 600+ tools | 🔥🔥🔥 |
| **Detection Engineering** | Writing Sigma rules for Nmap scans | 🔥🔥🔥 |
| **Traffic Analysis** | Capturing & analyzing attacker patterns | 🔥🔥🔥🔥 |
| **Incident Response** | Simulating real attack kill chain | 🔥🔥🔥 |

---

## 💡 Critical Lessons Learned

### 🔑 The Ping Failure Was a Gift

> When I saw `100% packet loss` in Step 10, I initially thought I'd misconfigured something. Then I realized — **real networks aren't perfectly open.** As a SOC analyst, I'll see failed connections constantly. The skill is knowing whether it's a:
> - Network misconfiguration
> - Firewall actively blocking
> - Host being offline
> - Security control working as designed

### 🛡️ Ethical Hacking Mindset

> Every scan I run is on **my own systems or authorized targets**. This lab taught me that the line between attacker and defender isn't technical — it's **consent and authorization**.

---

## 📈 What's Next

- [ ] Write my first Sigma rule to detect an Nmap scan
- [ ] Set up a Windows target VM for full attack/defense cycles
- [ ] Export PCAPs from Wireshark and practice with Zeek
- [ ] Build a detection lab with Elastic Stack (ELK)
- [ ] Create detection alerts for my own attacks
- [ ] Document SOC playbooks based on lab findings

---

## 📚 Resources I Recommend

| Resource | Why It Helped Me |
|----------|------------------|
| [Kali Linux Docs](https://www.kali.org/docs/) | Official, always up-to-date |
| [VirtualBox Manual](https://www.virtualbox.org/manual/) | Deep networking configuration |
| [MITRE ATT&CK](https://attack.mitre.org/) | Understanding attacker behavior |
| [SANS SOC Training](https://www.sans.org/cyber-security-courses/security-operations-center-soc-analyst/) | Professional SOC methodologies |

---

## 👨‍💻 Connect With Me

**Owen Maake**

<table>
<tr>
<td>🔬 <strong>Role</strong></td>
<td>SOC Analyst (in training) — actively building hands-on skills</td>
</tr>
<tr>
<td>🛡️ <strong>Focus</strong></td>
<td>Blue Team — detection and response</td>
</tr>
<tr>
<td>📧 <strong>Email</strong></td>
<td><a href="mailto:owenlethabo28@Gmail.com">owenlethabo28@Gmail.com</a></td>
</tr>
<tr>
<td>🔗 <strong>LinkedIn</strong></td>
<td><a href="https://www.linkedin.com/in/owen-maake-0b715a3a3/">Connect with me</a></td>
</tr>
</table>

> *I'm documenting this journey to help other aspiring SOC analysts. If you're doing the same, let's connect and learn together.*

---

## ⚠️ Legal Disclaimer

> **IMPORTANT**: This lab is for **AUTHORIZED** educational and professional training ONLY.
> 
> ✅ **You MAY:**
> - Scan your own systems
> - Test on networks you own
> - Practice in isolated lab environments
> - Use with written permission from system owners
>
> ❌ **You MAY NOT:**
> - Scan networks or systems you don't own
> - Test without explicit written permission
> - Use these skills for unauthorized access
> - Share scan results without authorization
>
> *Unauthorized scanning is illegal in most jurisdictions. This repository documents my personal learning journey on authorized systems only.*

---

## 📄 License

This project is licensed under the MIT License — feel free to use, modify, and share with attribution.
