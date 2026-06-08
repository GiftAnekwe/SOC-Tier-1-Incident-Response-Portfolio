# SOC Tier-1 Incident Response Portfolio

## Overview

This portfolio demonstrates incident investigation, threat analysis, pattern detection, and ethical decision-making in a cybersecurity operations center (SOC) environment. The analysis covers a real-world breach scenario where a financial services client was compromised, customer data was exfiltrated, and critical security alerts were systematically dismissed.

## What This Shows

**Technical Skills:**
- SSH authentication log analysis and IP geolocation
- Ticket history pattern recognition and root cause analysis
- Threat actor attribution through payload decoding
- Evidence preservation and escalation procedures
- Hash function identification and keyspace assessment

**Decision-Making Under Pressure:**
- Applying ISC2 Code of Ethics to conflicting directives
- Balancing organizational hierarchy with security obligations
- Incident prioritization and escalation judgment
- Account lifecycle management and compliance implications

## The Scenario

**Timeline**: June 3-5, 2024  
**Threat Actor**: The Griot (known regional threat actor)  
**Impact**: Customer financial data (names, addresses, transactions) exfiltrated  
**Root Cause**: Organizational process failure — single analyst with no escalation requirements dismissed 9 alerts

## Files in This Portfolio

### Analysis Deliverables (4 parts)

**D1 — Suspicious-Login-Analysis.md**
- 8-row evidence table with confidence assessments (HIGH/MEDIUM/LOW)
- Row-by-row analysis of suspicious authentication events
- Pattern summary and next investigative steps
- Demonstrates: log analysis, evidence correlation, confidence reasoning

**D2 — Dismissal-Pattern-Analysis.md**
- Per-ticket walkthrough of 9 dismissed alerts
- Root cause analysis (single-analyst decision-making)
- Cost of each dismissal (hours of undetected access, data theft)
- Procedural recommendations (mandatory escalation rules)
- Demonstrates: process analysis, failure mode identification, remediation design

**D3 — Executive-Brief.md**
- Business impact summary for non-technical decision-makers
- 72-hour incident response action plan
- Regulatory obligations (NDPR, data protection)
- Week 2 continued investigation steps
- Demonstrates: technical-to-business translation, prioritization, stakeholder communication

**D4 — Judgment-Essay.md**
- Part A: Ethical decision-making when instructed to close a serious alert
- Part B: Real-time incident response scenario under time pressure
- ISC2 Code of Ethics application
- Demonstrates: ethical reasoning, judgment under uncertainty, escalation procedures

### Technical Guides

See **TECHNICAL-GUIDES/README.md** for:
- Hash identification (MD5, SHA-1, SHA-256, bcrypt)
- Password security and keyspace analysis
- Threat actor attribution techniques

## Key Findings

**Attack Sequence:**
1. Jun 3: Brute force reconnaissance (blocked)
2. Jun 4 02:07 UTC: Successful break-in (valid credentials)
3. Jun 4 02:09 UTC: Privilege escalation and system reconnaissance
4. Jun 4 02:31 UTC: Customer data staging
5. Jun 4 03:01 UTC: Data exfiltration confirmed
6. Jun 5 03:14 UTC: Return visit (persistent access)

**Critical Issue:**  
Nine CRITICAL and HIGH severity alerts were dismissed without investigation by a single analyst operating without escalation requirements.

**Recommendation:**  
Implement mandatory escalation rule: CRITICAL/HIGH alerts require peer review and manager approval before closure.

## External References

- NIST SP 800-63B (Password Security)
- NIST SP 800-61 (Incident Handling)
- ISC2 Code of Ethics
- MITRE ATT&CK Framework (T1078 — Valid Accounts)
- NDPR (Nigerian Data Protection Regulation)

## Anonymization

This scenario uses a fictional fintech client. Employee names, ticket IDs, and company names have been anonymized to comply with programme guidelines:
- Employee names → Role labels ([OPERATIONS-ANALYST], [HEAD-OF-SECURITY], etc.)
- Ticket IDs → Generic placeholders ([TICKET-A], [TICKET-B], etc.)
- Company name → [FINTECH-CLIENT]

All technical evidence (IPs, timestamps, commands, file paths) is preserved for authenticity.

## How to Use This Portfolio

1. **Start with D1** — Understand the evidence and suspicious patterns
2. **Read D2** — See how and why the alerts were missed
3. **Review D3** — Understand business impact and response priorities
4. **Study D4** — Learn the ethical and procedural decision-making process
5. **Reference TECHNICAL-GUIDES** — For deep dives on specific technical topics

## Credentials

- UBI Stage 0 Completion Certificate
- Letter of Recommendation

See CREDENTIALS/ folder.

## License

MIT License — See LICENSE file for details.

---

**Author**: Gift Anekwe  
**Date**: June 2026  
**Programme**: Ubuntu Bridge Initiative Cybersecurity Internship, Cohort 1, Stage 0
