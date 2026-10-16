## Room 06 - SOC L1 Alert Reporting

**Date Completed:** Oct 16, 2026
**Badge:** SOC L1 Alert Reporting completed!

### Objective
Learn the 5 W model for alert reporting - Who, What, When, Where, Why - and document true positive compromises with proper analyst comments and remediation steps.

### Lab Overview
Two alerts in In Progress requiring full investigation and reporting using the 5W framework.

---

### Alert 1 - Email Marked as Phishing after Delivery

**Metadata:**
- Time: Mar 27th 2025 at 19:25
- Severity: Medium
- Status: In Progress -> Closed
- Assignee: You (L1)
- Rule: Email classified as phishing post-delivery after automated analysis

**Details:**
- Subject: Important Update: 【entity-Microsoft Teams¦canonical_name=Microsoft Teams】 Pricing Increase
- Body Keywords: 600% price increase; urgent notice; download the report; read the details;
- Sender: Microsoft Support <support@microsoft.com>
- Recipient: Eddie Huffman, IT Manager <e.huffman@tryhackme.thm>
- Security Checks: SPF/Fail; DKIM/Fail;
- Attached URLs: None
- Attached Files: REPORT.rar

**Investigation - 5 Ws:**

- **Who:** External actor spoofing Microsoft Support <support@microsoft.com> sent to victim Eddie Huffman, IT Manager <e.huffman@tryhackme.thm> - high-value target.
- **What:** Email with subject "Important Update: 【entity-Microsoft Teams¦canonical_name=Microsoft Teams】 Pricing Increase" containing suspicious attachment REPORT.rar and urgent keywords (600% price increase, urgent notice, download report) to lure user.
- **When:** Delivered on Mar 27th 2025 at 19:25, flagged post-delivery by automated analysis.
- **Where:** Origin external IP spoofing microsoft.com domain, destination is internal M365 mailbox e.huffman@tryhackme.thm.
- **Why:** Verdict is True Positive Phishing because SPF/DKIM fail proves spoofing, Urgency social engineering, Unusual .rar attachment not used by Microsoft for pricing notices, indicates likely malware delivery. Recommend purge email, check if user opened RAR, isolate host if executed and block sender. MITRE T1566.001

**Verdict:** TRUE POSITIVE - Phishing
**MITRE:** T1566.001 - Phishing: Spearphishing Attachment
**Action:** Purge email from mailbox, check M365 logs if user opened REPORT.rar, isolate host if executed, block sender domain, reset user credentials, escalate to L2.

---

### Alert 2 - Spike of Domain Discovery Commands

**Metadata:**
- Time: Mar 27th 2025 at 19:56
- Severity: Medium
- Status: In Progress -> Closed
- Assignee: You (L1)
- Rule: Detects a spike of commands like whoami, net user, and Get-ADUser, often used during AD domain discovery.

**Details:**
- Invoked Commands: dir hostname whoami /priv net group "Domain Admins" /domain nltest /dclist:tryhackme.thm
- Host Name: DMZ-MSEXCHANGE-2013
- Host OS: Windows Server 2012 R2
- User: NT AUTHORITY\SYSTEM
- Source Process: C:\Windows\System32\cmd.exe
- Parent Process: C:\Users\Public\revshell.exe
- Grandparent Process: C:\Windows\System32\inetsrv\w3wp.exe

**Investigation - 5 Ws:**

- **Who:** Attacker operating as NT AUTHORITY\SYSTEM on host DMZ-MSEXCHANGE-2013 (Windows Server 2012 R2). This is elevated SYSTEM account, not regular IT user.
- **What:** Executed spike of domain discovery commands - dir, hostname, whoami /priv, net group "Domain Admins" /domain, nltest /dclist:tryhackme.thm for AD reconnaissance to enumerate Domain Admins and DC list.
- **When:** Detected 27th 2025 at 19:56. Process chain shows ongoing compromise starting from IIS.
- **Where:** Host DMZ-MSEXCHANGE-2013 in DMZ. Process tree: Grandparent C:\Windows\System32\inetsrv\w3wp.exe (IIS) -> Parent C:\Users\Public\revshell.exe (malicious payload in public folder) -> Source C:\Windows\System32\cmd.exe. Shows IIS exploitation to drop reverse shell.
- **Why:** True Positive Compromised. w3wp spawning revshell is malicious, revshell location in Public is abnormal, SYSTEM privilege plus Domain Admin enumeration confirms post-exploitation. Requires immediate isolation of DMZ-MSEXCHANGE-2013, block and investigate w3wp, collect revshell.exe for malware analysis, and reset credentials. MITRE T1190, T1087, T1083

**Verdict:** TRUE POSITIVE - Compromised Host
**MITRE:** T1190 Exploit Public-Facing Application, T1087 Account Discovery, T1083 File and Directory Discovery
**Action:** Immediate isolation of DMZ-MSEXCHANGE-2013, block, investigate w3wp.exe (IIS), collect C:\Users\Public\revshell.exe for malware analysis, reset all credentials on host, hunt for lateral movement, escalate to L2/IR.

---

### Reporting Model Learned

- **Who:** Which user logs in, runs the command, or downloads the file
- **What:** What exact action or event sequence was performed
- **When:** When exactly did the suspicious activity start and ended
- **Where:** Which device, IP, or website was involved in the alert
- **Why:** The most important W, the reasoning for your final verdict

---

### Evidence

#### Full Model
- 5W Reporting Model - [View](./Screenshots/5W-model.png)

#### Alert 1 - Email Marked as Phishing after Delivery - TRUE POSITIVE
- Initial Alert Details - [View](./Screenshots/phishing-alert.png)
- Analyst Comment with 5Ws - True Positive Phishing - [View](./Screenshots/phishing-TP-comment.png)

#### Alert 2 - Spike of Domain Discovery Commands - TRUE POSITIVE COMPROMISED
- Initial Alert Details - Domain Discovery - [View](./Screenshots/domain-discovery-alert.png)
- Analyst Comment with 5Ws - Compromised Host via IIS -> revshell -> SYSTEM - [View](./Screenshots/domain-discovery-TP-comment.png)

#### Badge
- SOC L1 Alert Reporting completed - oteejay96 - [View](./Screenshots/SOC_L1_Alert_Reporting.png)

---

### Lessons Learned
1. SPF/DKIM Fail = spoofing proof - key for phishing verdict
2. .rar attachment + urgency + pricing increase = classic social engineering
3. Process tree analysis: w3wp.exe -> revshell.exe in Public -> cmd.exe = IIS exploit pattern
4. NT AUTHORITY\SYSTEM + Domain Admins enumeration = confirmed post-exploitation, not IT activity
5. 5W model ensures complete reporting for L2/IR handoff
