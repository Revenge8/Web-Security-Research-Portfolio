# Web-Security-Research-Portfolio
"A specialized repository documenting advanced web security research methodologies, focusing on BOLA and IDOR vulnerability discovery in complex API environments. Includes techniques for traffic filtering and logic-based authorization testing."
# Web Security Research Methodology

This portfolio documents my approach to identifying **BOLA (IDOR)** and logic-based vulnerabilities in complex web environments.

## 🛠 Core Tools
- **Proxy:** Burp Suite.
- **Extensions:** Autorize, AutoRepeater.

## 🔍 Methodology
### 1. Traffic Filtering
Focused on stripping analytics noise (e.g., third-party trackers) to isolate high-value Internal Admin APIs.

### 2. Authorization Testing (BOLA)
Testing for Broken Object Level Authorization by manipulating UUIDs in:
- **URL Paths:** e.g., `/signup/[UUID]/extend-trial`
- **Request Bodies:** Analyzing JSON fields like `subjectValue` for IDOR potential.

## 📝 Case Study: Trial Extension Flow
Tested an endpoint that relied on a UUID to identify merchant trial status. By swapping identifiers between sessions, I analyzed the server's permission enforcement (403 Forbidden vs 200 OK).

## ⚖️ Disclaimer
Educational purposes only. All testing was conducted on authorized targets via Bug Bounty programs.
