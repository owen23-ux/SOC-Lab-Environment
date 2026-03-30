
---

## 📄 File 3: soc-detection-rules.md

```markdown
# SOC Detection Rules for Attacker Activities

## 🎯 Purpose
This document provides **detection rules** (Sigma, YARA, and generic queries) for the attacker behaviors you can simulate in your Kali SOC Lab.

---

## 1. Nmap Scan Detection

### Sigma Rule for Nmap Scans
```yaml
title: Nmap Port Scan Detection
id: 8b7f6e5d-4c3a-2b1a-9f8e-7d6c5b4a3a2a
status: experimental
description: Detects Nmap port scanning activity
references:
  - https://nmap.org/book/man-detection.html
logsource:
  category: firewall
  product: windows
  service: security
detection:
  selection:
    EventID: 5156
    SourcePort: 
      - 443
      - 80
      - 22
      - 445
    DestinationPort: 
      - 1-65535
    Protocol: 6  # TCP
  condition: selection | count(DestinationIP) by SourceIP > 10
falsepositives:
  - Legitimate vulnerability scanners
  - Network monitoring tools
level: medium
tags:
  - attack.discovery
  - attack.t1046
