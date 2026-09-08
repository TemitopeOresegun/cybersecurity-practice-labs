
# 04 Systems as Attack Vectors - Completed [4/14]
Date: Sep 8, 2026 | Badge: First Step into SOC

## Objective
Understand systems as entry point vs humans. Patch + hunt, not just block.

## Alerts Triaged (4)
1. HQ-MAIL-02 - CVE-2024-49040 Exchange exposed -> Action: Patch + hunt for T1078 persistence. MITRE T1190 Exploit Public-Facing App
2. Corporate Website - WordPress admin brute-force -> Action: Reset breached creds + restore pages + hunt web shell. MITRE T1110 Brute Force -> T1505.003 (Same pattern as Room 01 221.181.185.159: 18:22 fail, 18:24 fail, 18:25 fail, 18:26 success)
3. Threat Intel - Neighbor ransomware via old Cisco firewall -> Action: Patched London office firewall. MITRE T1190 -> T1486 if missed. NIST DE.CT
4. LPT-01518 - Trusted 3D app running malicious CMD -> Action: Supply chain. MITRE T1195.002 Supply Chain Compromise

## Remediation Chosen
✅ Antivirus, Security Training for IT, Patch Management Policy, Secure Password Policy
❌ Rejected: Website Restrictions (business impact), Shared Accounts (kills accountability - PR.AC), Obscure Server Naming (security through obscurity)

## Chain
Room 01 T1110 Brute Force 221.181.185.159 -> Room 03 T1566 Phishing -> Room 04 T1190 & T1195.002 -> All lead to T1078 Valid Accounts -> T1071 C2 beacon (10.x.x.x -> 221.181.185.159:443 every 30s)

## NIST
DE.CM Detection, PR.IP Patch Management, RS.MA Response Analysis, DE.CT Threat Intel

## Key Takeaway
L1 must check vuln logs + auth logs + threat intel + OSINT BEFORE block/patch. Patch without hunting leaves T1078. SOC Quote: "Check email/vuln logs + OSINT before firewall block"
