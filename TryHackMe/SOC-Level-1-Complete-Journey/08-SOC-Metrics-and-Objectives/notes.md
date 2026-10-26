# Room 08: SOC Metrics and Objectives | TryHackMe SAL1

**Status:** ✅ Completed  
**Date:** Oct 26, 2026  
**Path:** SOC-Level-1-Complete-Journey  
**Badge:** SOC Metrics and Objectives

## Overview
A SOC that can't measure itself can't improve. This room covers how SOC efficiency is measured using KPIs.

## Key Metrics

**1. MTTD - Mean Time to Detect**
Time from event occurrence to detection by SOC. High MTTD = more attacker dwell time.

**2. MTTA - Mean Time to Acknowledge**
Time from alert creation to L1 acknowledging it. Shows queue health.

**3. MTTR - Mean Time to Respond / Resolve**
Time from acknowledgement to containment & closure/escalation. Core SLA metric.

**4. False Positive (FP) Rate**
% of alerts incorrectly flagged as malicious. High FP = alert fatigue + slow MTTA/MTTR.

**Other:** SLA (business promise), Zero alerts != good (could be broken sensors).

## L1 Impact
- Fast triage = low MTTA
- Clean 5W report + workbook = low MTTR for L2
- Flag noisy rules = lower FP rate

## Workflow
Alert -> MTTD -> MTTA -> Workbook -> Report -> MTTR -> Close/Escalate.
