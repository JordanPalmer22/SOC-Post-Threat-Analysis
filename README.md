# 🛡️ Threat Analysis: Suspicious POST Request from `HEADLESS-PC`

This project demonstrates real-world threat detection using Wireshark and PCAP analysis. It focuses on identifying a suspicious outbound HTTP POST that contains internal host reconnaissance data — a strong indicator of malware beaconing or data exfiltration to a Command and Control (C2) server.

---

## 📌 Summary

- **Tool Used**: Wireshark  
- **Detected Behavior**: Data exfiltration via HTTP POST  
- **Outcome**: Identified C2 communication and extracted indicators of compromise (IOCs)  

---

## 📂 Project Files

| File/Folder               | Description                                      |
|---------------------------|--------------------------------------------------|
| `threat_analysis_report.md` | Full markdown report detailing the analysis steps and findings |
| `pcap/`                   | Contains the original PCAP file used in analysis |
| `artifacts/`              | Extracted malicious POST payload for inspection  |
| `screenshots/`            | Visual documentation (Wireshark views)           |

---

## 📷 Preview

![Wireshark Payload Screenshot](screenshots/wireshark_post_payload_view.png)

---

## 🛠 Tools Used

- Wireshark  
- GitHub (version control)  
- Markdown (reporting)  

---

## 🧠 What I Learned

- How to detect and analyze suspicious POST activity using Wireshark  
- Indicators of malware C2 behavior and network reconnaissance  
- How to document and report IOCs for a SOC environment  

---

> 🧩 This project is part of my SOC Analyst GitHub portfolio. For more projects, check out my [portfolio index](../).
