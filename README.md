# 🚀 ProjectX Cybersecurity Home Lab  

![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-blue)
![Tools](https://img.shields.io/badge/Tools-VirtualBox%20%7C%20Security%20Onion%20%7C%20Wazuh%20%7C%20Kali%20Linux-orange)
![Skills](https://img.shields.io/badge/Skills-Active%20Directory%20%7C%20SIEM%20%7C%20Threat%20Hunting%20%7C%20Incident%20Response-success)

---

## 📌 Overview  
As a cybersecurity analyst in training, I wanted a space where I could **learn by doing** — a place to break things, fix them, simulate attacks, and practice defenses without risking real systems. That’s how **ProjectX** was born: my own fully functional, virtualized **enterprise network**, complete with a simulated business infrastructure, a SIEM, and the ability to both **attack and defend** in a safe, controlled environment.  

Homelabs aren’t just “practice grounds” — they’re **proof of skill**. This project allowed me to apply what I’ve learned from certifications, courses, and hands-on research while producing something I can **showcase to potential employers**.  

---

## 🏆 Objectives  
The goals of this lab were:  
- **Hands-on practice** — replicate the core parts of a business network.  
- **Portfolio building** — document and showcase my work to highlight my skills.  
- **Security-first mindset** — simulate cyberattacks and practice real detection and response.  
- **Cost-effective learning** — built entirely on my own hardware, with free and open-source tools where possible.  

---

## 🎯 Expected Outcomes  
By the end of this build, my lab would have:  
- A fully functional **virtual network** with multiple simulated business components.  
- Core services like **Active Directory**, **email**, **SIEM/XDR**, and a **security sandbox**.  
- The ability to **simulate cyberattacks from initial access to full compromise**.  
- Custom-built **detections and alerts** for threat hunting and incident response practice.  

---

## 🛠 Prerequisites  
Before starting, I made sure I had:  
- **Basic IT knowledge** — networking, OS installation, and virtualization concepts.  
- **Hardware** — a workstation with at least **8 GB RAM, 4 CPU cores, and 100 GB free space**.  
- **Virtualization software** — VirtualBox (free and open-source).  
- **A willingness to experiment and learn** — the most important ingredient.  

---

## 🏗️ Lab Architecture  

The lab simulates a small company called **ProjectX**.  

| Component       | Purpose                                              | OS / Tool                        |
|----------------|------------------------------------------------------|-----------------------------------|
| **DC01**       | Domain Controller for authentication & GPOs          | Windows Server 2022 (Active Directory) |
| **W11-Client** | Corporate workstation                                 | Windows 11 Enterprise            |
| **Ubuntu-Desktop** | Linux endpoint for diversity                     | Ubuntu 22.04                     |
| **SO-Monitor** | Network monitoring, IDS/IPS, PCAP analysis            | Security Onion                   |
| **Mail-Server**| Handles corporate email communications                | Postfix on Ubuntu                 |
| **Wazuh-SIEM** | Centralized log collection, threat detection, alerts  | Wazuh Security Server             |
| **AttackBox**  | Red team simulation system                            | Kali Linux                        |

---

## 🖥️ Network Topology Diagram  

The diagram below shows the **ProjectX** enterprise simulation, including endpoints, servers, and the attack path used during the red team simulation.  

![Network Topology](images/projectx_network_topology.png)  

---

## 🔧 Step-by-Step Build  

### **1. Virtual Network Setup**  
- Created two isolated networks in VirtualBox:  
  - **Corporate Network** — for business operations.  
  - **Attack Network** — for controlled red team activity.  
- Configured static IPs for predictable connectivity.  

---

### **2. Windows Active Directory (DC01)**  
- Installed **Windows Server 2022**.  
- Configured **Active Directory Domain Services**.  
- Created **Organizational Units (OUs)** for users, groups, and computers.  
- Applied **Group Policy Objects (GPOs)** to simulate real-world restrictions.  

---

### **3. Windows 11 Enterprise Workstation**  
- Joined the machine to the **ProjectX.local** domain.  
- Configured **domain user logins**.  
- Installed basic business applications.  

---

### **4. Ubuntu Desktop**  
- Added as a non-Windows endpoint.  
- Configured SSH and installed productivity tools.  

---

### **5. Security Onion Deployment**  
- Installed **Security Onion** as a network monitoring platform.  
- Enabled **Zeek**, **Suricata**, and **Elastic Stack**.  
- Configured dashboards for **threat hunting**.  

---

### **6. Postfix Email Server**  
- Built an internal **Postfix/Dovecot email system**.  
- Created test accounts for phishing simulations.  

---

### **7. Wazuh Security Server**  
- Installed **Wazuh** for log aggregation and alerting.  
- Integrated logs from **Windows, Linux, and Security Onion**.  
- Created **custom detection rules** for specific threats.  

---

### **8. Red Team Simulation (AttackBox)**  
- Installed **Kali Linux** as an attacker box.  
- Simulated:  
  - **Phishing attack** with malicious attachments.  
  - **Credential harvesting** from a compromised endpoint.  
  - **Lateral movement** into the domain controller.  
- Logged and analyzed activity in **Wazuh** and **Security Onion**.  

---

## 🔍 Skills Demonstrated  
- **Network architecture & segmentation** for security.  
- **Windows Server administration** (AD, GPOs).  
- **Linux server configuration** (Postfix, Ubuntu endpoints).  
- **SIEM/XDR integration** with Wazuh & Security Onion.  
- **Incident response** — detecting, analyzing, responding.  
- **Threat hunting** — using Zeek, Suricata, Kibana dashboards.  
- **Custom rule writing** for detection.  

---

## 📸 Screenshots & Evidence  
> _Below are placeholders — I will replace these with actual lab screenshots._  

- ![Active Directory Setup](images/ad_setup.png)  
- ![Wazuh SIEM Dashboard](images/wazuh_dashboard.png)  
- ![Security Onion Alerts](images/so_alerts.png)  
- ![Attack Simulation Output](images/attack_sim.png)  

---

## 📄 Conclusion  
This homelab gave me a **safe, flexible, and realistic** platform to sharpen my cybersecurity skills. I practiced attacking and defending systems, learned enterprise-grade tools, and created a system I can **demonstrate to employers** as proof of my technical abilities.  

---

**Author:** Christopher Ham  
**LinkedIn:** [linkedin.com/in/christopherham252](https://www.linkedin.com/in/christopherham252)  
**License:** MIT  
