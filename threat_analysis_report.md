# 🧪 Threat Analysis Report: Suspicious POST from `HEADLESS-PC`

---

## 📅 Overview

This report analyzes suspicious network behavior captured on **October 31, 2018**, involving a Windows 7 endpoint named `HEADLESS-PC`. The system initiated an outbound **HTTP POST** request to an uncommon destination shortly after performing public IP discovery using `checkip.amazonaws.com`.

---

## 🔍 Key Observations

| Field           | Detail                                 |
|----------------|-----------------------------------------|
| **Source IP**   | `10.100.9.107`                         |
| **Destination** | `173.171.132.82:8082`                  |
| **Request Type**| HTTP `POST`                            |
| **User-Agent**  | `test` (non-standard; not browser-based) |
| **Payload**     | `multipart/form-data` including:       |
|                 | - Running process list                 |
|                 | - System information (OS, hostname)    |
|                 | - Network configuration (ipconfig)     |
|                 | - Domain trust relationships           |

---

## 🚨 Indicators of Compromise (IOCs)

| Type        | Value                                 |
|-------------|----------------------------------------|
| Hostname    | `HEADLESS-PC`                          |
| Domain      | `halloweenjob.com`                     |
| C2 IP       | `173.171.132.82`                       |
| POST Path   | `/sat91/HEADLESS-PC.../90`             |
| User-Agent  | `test`                                 |

---

## 🧠 Threat Assessment

The structure and content of the POST payload indicate the presence of **malware beaconing behavior**, consistent with a **Remote Access Trojan (RAT)** or **C2 staging implant**. Specifically:

- The `test` User-Agent suggests a custom or scripted agent, not typical of standard software.
- The reconnaissance data (system info, domain structure, process list) suggests pre-exfiltration or staging for lateral movement.
- The POST destination (`173.171.132.82`) and URL path (`/sat91/...`) do not match legitimate services and likely represent a malicious Command and Control (C2) endpoint.

---

## 🧾 Conclusion

This activity should be considered **malicious**. Immediate action should include:

- Isolating `HEADLESS-PC` from the network
- Scanning for persistence mechanisms (e.g., scheduled tasks, registry keys)
- Reviewing additional traffic to/from `173.171.132.82`
- Performing a full forensic analysis of the host

---

> 🧩 This report is part of my SOC Analyst portfolio project. For more information, see the full [GitHub repository](https://github.com/JordanPalmer22/SOC-Post-Threat-Analysis).
