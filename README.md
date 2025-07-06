# 🛡️ Threat Analysis: Suspicious POST Request from HEADLESS-PC

This project showcases a real-world threat detection analysis using Wireshark and PCAP files. The analysis reveals a suspicious outbound HTTP POST containing internal host reconnaissance data — a strong indicator of malware beaconing or data exfiltration.

## 📌 Summary
- **PCAP Analysis Tool**: Wireshark
- **Detected Behavior**: Data exfiltration via HTTP POST
- **Outcome**: Identified C2 communication and clear indicators of compromise (IOCs)

## 📂 Project Files
| File/Folder | Description |
|-------------|-------------|
| `threat_analysis_report.md` | Full markdown write-up of the threat analysis. |
| `pcap/` | Contains the original PCAP file. |
| `artifacts/` | Extracted malicious POST payload. |
| `screenshots/` | Wireshark visual aid of the request. |

## 📷 Preview
![Wireshark Payload](screenshots/wireshark_post_payload_view.png)

## 🛠 Tools Used
- Wireshark
- GitHub for versioning
- Markdown for documentation

## 🧠 What I Learned
- How to identify and extract POST payloads from PCAP
- Signs of malware C2 and domain reconnaissance
- Documenting IOCs in a professional report format

---

> 🧩 This project is part of my SOC Analyst GitHub portfolio. For more, check out my [portfolio index](../).
