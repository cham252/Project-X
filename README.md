# 🛡️ Phishing Detection & Analysis Home Lab

Welcome to the **Phishing Detection and Analysis Home Lab**, a realistic hands-on environment for simulating and investigating phishing attacks. This project is ideal for SOC analysts, students, and cybersecurity enthusiasts who want to sharpen their skills in phishing email investigation, malware analysis, and threat intelligence.

---

## 📌 Objectives

- Simulate phishing attacks in a sandboxed environment
- Analyze phishing emails and attachments
- Extract and correlate Indicators of Compromise (IOCs)
- Investigate payloads and malicious URLs
- Enrich findings with threat intelligence tools
- Report findings and mitigation strategies

---

## 🧰 Tools Used

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
All VMs are hosted in VirtualBox or VMware under a NAT network (10.0.0.0/24) for safe isolation.

---

## ⚙️ Setup Guide

1. **Deploy VMs**  
   - Kali Linux (Attacker)  
   - Windows 10 (Victim)  
   - Ubuntu/Debian (Email server + Splunk)

2. **Send Phishing Email**  
   - Use Social Engineering Toolkit (SET) or manual spoofing  
   - Attach malicious `.docm` or link

3. **Analyze Email on Victim VM**  
   - Review email headers using PhishTool  
   - Open attachments in Any.Run or safe sandbox

4. **Extract IOCs**  
   - URLs, hashes, IPs, domains  
   - Use CyberChef for decoding payloads  
   - Use VirusTotal, URLScan, ThreatFox for enrichment

5. **Log Analysis**  
   - Configure Splunk or ELK to ingest logs and alerts  
   - Visualize and correlate events using dashboards

6. **Document & Report**  
   - Use provided template to write a full threat report

---

## 📂 Directory Structure
---

## 🧪 Example IOC Output

**Email Header:**
**Extracted IOCs:**
- `http://appleid-login[.]secure-update[.]ru`
- File hash: `e99a18c428cb38d5f260853678922e03`
- IP Address: `185.123.45.67`

---

## 📚 Learning Outcomes

✅ Understand phishing attack vectors  
✅ Perform detailed email header analysis  
✅ Decode obfuscated payloads and links  
✅ Enrich and correlate IOCs with open-source intel tools  
✅ Report and document findings professionally

---

## 🙌 Credits

Created by **Christopher Ham**, Cybersecurity Student | SOC Analyst in Training  
This project is part of a broader cybersecurity home lab initiative for developing real-world defensive security skills.

---
