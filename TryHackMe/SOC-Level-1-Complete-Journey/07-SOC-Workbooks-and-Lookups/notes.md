# Room 07: SOC Workbooks and Lookups

**Status:** ✅ Completed | **Date:** Oct 24, 2026

> Workbooks help Junior SOC Analysts triage alerts efficiently and remove the risk of errors.

### 1. Email Analysis Workbook
Header (SPF/DKIM), spoof check, VT/urlscan/Talos enrichment
MITRE: T1566.001

### 2. PowerShell Analysis Workbook  
4103/4104 logs, EncodedCommand, IEX, Hidden
MITRE: T1059.001

### 3. Network Analysis Workbook
DNS/HTTP beaconing, AbuseIPDB/OTX enrichment
MITRE: T1071

**Workflow:** Alert -> Workbook -> Enrichment -> Verdict -> 5W Report.
