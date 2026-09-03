
# 03 - Humans as Attack Vectors
Date: Sep 3, 2026
Status: ✅ Completed

Objective: Understand how attackers exploit humans as entry point.

Human Attack Types:
- Phishing (email), Vishing (voice call), Smishing (SMS)
- Baiting, Pretexting, Tailgating

Phishing Anatomy: Spoofed sender, urgent subject, malicious link/attachment, credential harvest

MITRE ATT&CK: T1566 Phishing, T1078 Valid Accounts (after credentials stolen)
NIST CSF: PR.AT (Awareness & Training), DE.CM (Detection)

Connection to Room 01: 
In Room 01 I saw T1110 Brute Force on port 22 for John. If John was phished first (T1566), attacker wouldn't need brute force — they'd have T1078 directly. Human vector enables technical vectors.

Key Takeaway: Firewall block of 221.181.185.159 is useless if user clicks phishing link and gives creds. L1 must check email logs + user reports + OSINT on sender.
