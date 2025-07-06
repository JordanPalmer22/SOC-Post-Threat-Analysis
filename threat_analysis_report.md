# Threat Analysis Report: Suspicious POST from HEADLESS-PC

## Overview

This analysis focuses on suspicious network behavior captured on October 31, 2018. A Windows 7 machine (`HEADLESS-PC`) made an unusual HTTP POST request shortly after resolving the public IP using `checkip.amazonaws.com`.

## Key Observations

- **Source IP**: 10.100.9.107  
- **Destination IP**: 173.171.132.82:8082  
- **Request Type**: HTTP POST  
- **User-Agent**: `test` (unusual, non-browser UA)  
- **Payload**: Multipart form-data with process list, system info, IPConfig, domain config

## Indicators of Compromise (IOCs)

| Type        | Value                       |
|-------------|-----------------------------|
| Hostname    | HEADLESS-PC                 |
| Domain      | halloweenjob.com            |
| C2 IP       | 173.171.132.82              |
| POST Path   | `/sat91/HEADLESS-PC.../90`  |
| User-Agent  | `test`                      |

## Threat Assessment

The payload contents indicate malware beaconing and reconnaissance typical of RAT (Remote Access Trojan) behavior.

---
