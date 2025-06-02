# 🛡️ Phishing Detection & Analysis Home Lab

Hi! I'm currently working on a hands-on phishing detection and analysis project in my home lab. This lab simulates a real-world phishing investigation — from identifying suspicious emails to extracting indicators of compromise (IOCs), analyzing payloads, and reporting the threat. The goal is to strengthen my skills in email forensics, threat intelligence, and incident response.

---

## 🧪 Lab Purpose

The purpose of this project is to simulate a full phishing investigation workflow within a safe, isolated environment. I’m using a mix of open-source tools and custom scripts to:
- Analyze suspicious email headers and content
- Extract malicious links, IPs, and attachments
- Run sandbox analysis of payloads
- Enrich IOCs using threat intel platforms
- Log and correlate events using a SIEM (Splunk)

---

## 🖥️ My Lab Setup

I'm using VirtualBox with a NAT network setup (10.0.0.0/24). Here's the layout:## 🧰 Tools Used

[ Kali Linux (Attacker) ]
↓
[ Email Server (Postfix + Dovecot) ]
↓
[ Windows 10 (Victim Workstation) ]
↓
[ SIEM/Log Server (Splunk on Ubuntu) ]
Everything is self-contained and isolated for safety.

---

| Tool                | Use Case                                   |
|---------------------|---------------------------------------------|
| Wireshark           | Packet capture and network traffic analysis |
| PhishTool           | Email header and metadata analysis          |
| CyberChef           | Payload decoding and deobfuscation          |
| Any.Run / Joe Sandbox | Malware dynamic analysis                  |
| VirusTotal / URLScan.io | IOC enrichment and URL analysis        |
| Splunk / ELK Stack  | Log and event correlation                   |
| Python              | Custom scripts for automation               |

---

## 🖥️ Lab Architecture
Everything is self-contained and isolated for safety.

---

## 🧰 Tools I'm Using

- **Wireshark** – To monitor and analyze network traffic
- **PhishTool** – For analyzing email headers
- **CyberChef** – To decode and deobfuscate suspicious strings
- **Any.Run** / **Joe Sandbox** – For dynamic malware analysis
- **VirusTotal** / **URLScan.io** – For threat intel lookups
- **Splunk** – For log analysis and visualization
- **Python** – For scripting IOC extraction and automation

---

## 🔍 What I Did

### 1. Simulated a Phishing Attack
I crafted a phishing email using **SET (Social Engineering Toolkit)** on my Kali box, spoofing a fake Apple ID login alert with a `.docm` attachment and suspicious link.

### 2. Received and Analyzed the Email
On my Windows 10 victim VM, I opened the phishing email in Thunderbird. Using **PhishTool**, I inspected the headers and identified:
- SPF fail
- Suspicious sender domain
- Unusual routing IP: `185.45.67.123`

### 3. Extracted IOCs
I manually and programmatically pulled out:
- URLs: `http://apple-id-login[.]update-now[.]ru`
- IPs: `185.45.67.123`
- File hash: `9a8b7c6d5e4f3a2b1c0d...`

Used **CyberChef** to decode hidden Base64 payloads.

### 4. Malware Analysis
Uploaded the `.docm` file to **Any.Run** to observe behavior. The document attempted to run PowerShell commands that downloaded a secondary payload.

### 5. Enriched Threat Data
Used **VirusTotal**, **AbuseIPDB**, and **ThreatFox** to gather intel:
- Confirmed the domain was associated with multiple phishing campaigns
- The IP was flagged in multiple abuse reports

### 6. Logged Everything in Splunk
Set up log forwarding to **Splunk** and created a dashboard to visualize:
- Phishing email alerts
- IOC hits
- Timeline of attack execution

---

## 📁 Repo Structure

phishing-lab/
├── setup/
│   └── virtualbox_config.md
├── phishing_email/
│   └── fake_apple_eml.eml
├── artifacts/
│   ├── invoice.docm
│   ├── iocs.txt
│   └── malware_hashes.txt
├── analysis/
│   ├── anyrun_report.pdf
│   ├── cyberchef_results.txt
│   └── threat_intel_notes.md
├── scripts/
│   └── extract_iocs.py
├── dashboards/
│   └── splunk_dashboard.json
└── README.md
---

## 🧠 What I Learned

- How to safely analyze phishing emails and attachments
- How to identify and decode hidden payloads
- Practical use of threat intelligence tools
- How to set up basic log collection and analysis with Splunk
- The importance of documenting every step clearly and methodically

---

## 📚 Next Steps

- Add detection rules in Splunk for similar phishing patterns
- Automate IOC enrichment using Python APIs
- Simulate lateral movement in a post-phish breach scenario

---

## 🙌 About Me

I'm currently training to become a SOC Analyst and threat intelligence specialist. This home lab is part of my ongoing cybersecurity learning journey. You can check out my other labs and projects [here](https://github.com/cham252).

If you're interested in collaborating or have feedback, feel free to connect!

📧 **Email:** ayko4430@gmail.com  
🔗 **LinkedIn:** www.linkedin.com/in/christopherham252

---

> **Note:** This project is for educational and professional development purposes only. All testing is done in a secure, offline lab environment.
