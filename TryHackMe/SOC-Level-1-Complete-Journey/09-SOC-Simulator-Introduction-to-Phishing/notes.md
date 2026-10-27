# Room 09: SOC Simulator - Introduction to Phishing | TryHackMe SAL1

**Status:** ✅ Completed - Victory! Security Breach Prevented!  
**Date:** Oct 27, 2026

## Performance Metrics

| Metric | Value |
|---|---|
| True Positive Rate | 100% - Excellent |
| False Positive Rate | 100% - Excellent |
| Closed Alerts | 4 alerts |
| Mean Time to Resolve | 21 minutes |
| Mean Dwell Time | 60 minutes |

## Alerts Triaged

**True Positives:**
- 8815 - Inbound Email Containing Suspicious External Link - Medium - Phishing - 31.92m - Correct
- 8816 - Access to Blacklisted External URL Blocked by Firewall - High - Firewall - 25.62m - Correct
- 8817 - Inbound Email Containing Suspicious External Link - Medium - Phishing - 18.88m - Correct

**False Positives:**
- 8814 - Inbound Email Containing Suspicious External Link - Medium - Phishing - 9.43m - Correct

## Overall Analysis

Reports show solid understanding of alert triage and good analytical thinking.

**Areas to improve (AI feedback):**
- Why: Explain attacker's motive/objective, not just technique
- Where: Add specific system locations, network segments, environmental context for L2

## MITRE ATT&CK
- T1566.001 - Phishing
- T1105 - Ingress Tool Transfer

## Workflow
Alert -> Workbook (Email / Firewall) -> Enrichment -> 5W Report -> TP/FP Classification -> Close


