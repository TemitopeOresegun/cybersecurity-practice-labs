# Room 05 - SOC L1 Alert Triage
Date: Sep 13, 2026
Status: ✅ Completed
Platform: TryHackMe - SOC Level 1 Path (5/14)
Badge: SOC L1 Alert Triage completed

## Summary
Verdicts: 1 TP, 2 FP (handled by You L1)
- Alert 1 - Double-Extension cats2025.mp4.exe - TP Formbook - VT 51/71 - Talos Malicious
- Alert 2 - Data Exfil *.zoom.us - FP - Private IP 192.168.45.66 IANA RFC1918 - VT 0/89
- Alert 3 - GitHub facebook/react - FP - VT 0/90 - urlscan No classification - IP 140.82.121.3
- Alert 4 - Unusual VPN Login - FP - Handled by T.Ross L1
- Alert 5 - Bruteforce External - TP - Handled by J.Adams L2

Learnings: OSINT workflow (VT, Talos, urlscan, Whois), Private vs Public IP, Business context validation, Tuning recommendations, MITRE T1036.007, T1566, T1048

---

## Alert 1 - Double-Extension File Creation - TRUE POSITIVE

Confirmed True Positive - Double-Extension Masquerading / Phishing - Formbook Infostealer

Host LPT-HR-009, User S.Conway executed chrome.exe to download Target File C:\Users\S.Conway\Downloads\cats2025.mp4.exe from File MotW https://freecatvideosdhd.monster/cats2025.mp4.exe

OSINT Validation:
- File MD5 14d8486f3f63875ef93cfd240c5dc10b / SHA256 86D50A7FC8D245876B791EFE85EB7F64CD48B9E9648B4F8BEE22DBAE66FE3AA
- VirusTotal: 51/71 vendors flagged malicious - Tags: peexe, malware, spreader, checks-bios, detect-debug-environment, calls-wmi, long-sleeps [h0t.exe]
- Talos Intelligence: File Reputation Malicious - Detection Name: Formbook.28ck.in14.Talos - PE32 executable (GUI).NET assembly - Aliases: Trojan/Win.Generic.C5716670, Win32:CrypterX-gen [Trj]

Assessment: Attacker using T1036.007 Double File Extension + T1566 Phishing to masquerade EXE as MP4 video to trick user. Formbook is infostealer / RAT - risk of credential theft, data exfil.

Verdict: True Positive, Severity High maintained.

Recommended Actions: Isolate LPT-HR-009, kill chrome.exe process tree, delete cats2025.mp4.exe, block domain freecatvideosdhd.monster at proxy/firewall, block hash MD5/SHA256, reset S.Conway AD creds + MFA, hunt for persistence/autoruns + outbound C2, notify HR user security awareness. Escalate to L2/IR for Formbook cleanup.

---

## Alert 2 - Potential Data Exfiltration - FALSE POSITIVE

False Positive - Legitimate Zoom Business Activity - Meeting Room High Bandwidth

Alert triggered rule: 5+ GB to single destination = possible exfil. Source IP 192.168.45.66 (UK04/MEETINGROOM) sent 5.8 GB / received 5.2 GB to Destination *.zoom.us

OSINT Validation:
- Source IP 192.168.45.66 - Private RFC1918 address - VT 0/89 Clean - WHOIS: NetRange 192.168.0.0-192.168.255.255, NetName PRIVATE-ADDRESS-CBLK-RFC1918-IANA-RESERVED, Org IANA. Internal host, not public malicious IP.
- Destination *.zoom.us - Legitimate Zoom infrastructure - Trusted business application

Context: Source Network UK04/MEETINGROOM indicates conference room device running prolonged Zoom meetings - high sent/received volume is expected for video conferencing, not data exfiltration to untrusted location.

Verdict: False Positive. No exfil. Rule threshold met due to legitimate business use.

Action: Close alert. Recommend tuning rule to whitelist *.zoom.us / known meeting room subnets to reduce noise. No isolation needed.

---

## Alert 3 - Download from GitHub Repository - FALSE POSITIVE

False Positive - Legitimate Developer Activity - GitHub React Library

Alert: Download from GitHub Repository - Accessed URL https://github.com/facebook/react - Source User G.Chandler - Source Host LPT-IT-063 - Source Network VPN/DEVELOPERS

OSINT Validation:
- URL https://github.com/facebook/react - VirusTotal 0/90 Clean - No security vendors flagged
- urlscan.io: Verdict No classification (benign) - Main IP 140.82.121.3 / 140.82.121.4 located in Frankfurt, belongs to GITHUB - GitHub, Inc., US. Primary domain github.com - Cisco Umbrella rank 1678 - Domain age 13yr old (Created Oct 9th 2007), Registrar MarkMonitor, Inc. TLS cert Sectigo Public Server Authentication valid. github.com scanned 10000+ times on urlscan - No malicious indicators.
- Page Title: GitHub - react/react: The library for web and native user interfaces - Official Facebook React project

Context: Source network VPN/DEVELOPERS - IT/Developer user expected to pull open-source libraries. facebook/react is known-good, trusted open-source framework with millions of users.

Verdict: False Positive - Legitimate business justified download.

Action: Close alert. Recommend tuning: whitelist github.com/facebook/react for DEVELOPERS group to reduce noise. No isolation needed.

---
## Evidence

### Full Triage Board
- Board showing alerts closed - [View Board](./screenshots/triage-board.png)

### Alert 1 - Double-Extension cats2025.mp4.exe - Formbook - TRUE POSITIVE
- Formbook TP - [View](./screenshots/Formbook%20TP.png)
- VirusTotal 51/71 Malicious - [View](./screenshots/Formbook%20VT.png)
- Talos Malicious Formbook.28ck.in14.Talos - [View](./screenshots/Formbook%20Talos.png)

### Alert 2 - Potential Data Exfiltration *.zoom.us - FALSE POSITIVE
- Zoom FP - [View](./screenshots/Zoom%20FP.png)
- VirusTotal 0/89 Clean - Private RFC1918 - [View](./screenshots/Zoom%20VT.png)
- WHOIS IANA-RESERVED PRIVATE-ADDRESS - [View](./screenshots/Zoom%20Whois.png)

### Alert 3 - Download from GitHub Repository - FALSE POSITIVE
- GitHub FP - [View](./screenshots/GitHub%20FP.png)
- VirusTotal 0/90 Clean - [View](./screenshots/GitHub%20VT.png)
- urlscan.io No Classification - 140.82.121.3 GitHub Inc - [View](./screenshots/GitHub%20urlscan.png)
  
### Badge
- SOC L1 Alert Triage completed Sep 13, 2026 - [View](./screenshots/SOC%20L1%20Alert%20Triage.png)
