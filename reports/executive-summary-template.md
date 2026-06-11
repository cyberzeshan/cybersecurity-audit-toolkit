# Executive Summary — Cybersecurity Audit

> This template is designed for the C-suite and Board audience: 1–2 pages maximum, no technical jargon, focused on business risk and required decisions.

---

```
================================================================================
EXECUTIVE SUMMARY
Cybersecurity Controls Audit
================================================================================
Organization:   [ORGANIZATION NAME]
Audit Period:   [START DATE] – [END DATE]
Report Date:    [DATE]
Prepared By:    [AUDITOR NAME / INTERNAL AUDIT FUNCTION]
Audience:       Executive Leadership / Board / Audit Committee
Classification: CONFIDENTIAL
================================================================================
```

---

## At a Glance

| | |
|---|---|
| **Overall Rating** | ⚠️ Needs Improvement |
| **Audit Areas Covered** | Logical Access · Vulnerability Management · Change Management · Third-Party Risk |
| **Findings Identified** | 2 Significant Deficiencies · 1 Control Deficiency · 2 Observations |
| **Immediate Actions Required** | Yes — see below |
| **Next Management Update** | [DATE — e.g., Q3 Board Meeting] |

---

## What We Audited and Why

The [Internal Audit / GRC] team completed an independent assessment of [ORGANIZATION NAME]'s cybersecurity controls for the period [DATE] through [DATE]. This audit was performed to provide assurance to leadership and the Audit Committee on the effectiveness of controls protecting our systems, data, and customers.

The audit examined four areas that represent the highest cybersecurity risk to the organization based on the current risk profile:

- **Who can access our systems** — and whether that access is managed correctly
- **How quickly we fix security vulnerabilities** — before attackers can exploit them
- **Whether system changes are properly controlled** — to prevent outages and unauthorized modifications
- **Whether our third-party vendors are protecting our data** — as effectively as we protect our own

---

## What We Found

### Areas Working Well

Two areas were found to be operating effectively and deserve recognition:

- **Multi-Factor Authentication (MFA):** 100% of user accounts require MFA. This is a critical defense against password-based attacks and is fully implemented.
- **Security Awareness Training:** 98% of employees completed annual cybersecurity awareness training during the audit period, one of the highest completion rates we have seen.

### Issues Requiring Attention

We identified two significant control gaps that require management action:

---

**Issue 1: Former Employee Accounts Not Always Deactivated on Time**
*Significant Deficiency*

When employees leave the organization, their system access must be disabled within 24 hours. In our testing, this did not happen in 28% of cases (7 of 25 tested). Two former employees had access to sensitive financial systems and customer data for up to 14 days after their departure.

**Why this matters:** A former employee with active credentials can access — or damage — your systems and customer data after leaving. This is one of the most common insider threat scenarios, and it exposes the organization to regulatory and legal liability.

**What needs to happen:** Automate the connection between HR systems and IT access systems so that when HR records a termination, access is cut off immediately — without manual steps that can be missed. Estimated completion: [DATE].

**Cost of inaction:** SOC 2 exception, potential data breach liability, regulatory scrutiny.

---

**Issue 2: Critical Security Vulnerabilities Not Patched on Time**
*Significant Deficiency*

The organization maintains a policy that critical security vulnerabilities (the most severe category) must be patched within 15 days of discovery. In our review, 40% of critical vulnerabilities identified during the audit period were not remediated within this timeframe, with some remaining open for 60+ days.

**Why this matters:** Attackers actively scan for and exploit known vulnerabilities. A critical vulnerability that remains unpatched for 60 days is a known entry point into our systems. This is a primary cause of ransomware and data breach incidents across the industry.

**What needs to happen:** Establish a dedicated vulnerability remediation program with executive escalation for any critical vulnerability approaching the SLA deadline. Assign clear ownership for patch execution and track weekly. Estimated improvement timeline: [DATE].

**Cost of inaction:** Ransomware attack, data breach, business disruption, regulatory fines.

---

### Lower-Priority Observation

**Emergency changes:** A small number of emergency system changes (1 of 5 tested) were made without following the formal change approval process. This is lower risk due to compensating reviews, but the process should be tightened to prevent unauthorized changes from being disguised as emergencies.

---

## Risk Heatmap

```
                     LIKELIHOOD
              Low         Medium        High
         ┌────────────┬─────────────┬─────────────┐
    High │            │  ● Issue 2  │             │
         │            │  (Vuln Mgmt)│             │
I   ─────┼────────────┼─────────────┼─────────────┤
M Medium │            │  ● Issue 1  │             │
P        │            │  (Access)   │             │
A   ─────┼────────────┼─────────────┼─────────────┤
C   Low  │  ● CD-01   │             │             │
T        │  (Changes) │             │             │
         └────────────┴─────────────┴─────────────┘
```

---

## What We Are Asking Leadership to Do

| Action | Owner | By When |
|--------|-------|---------|
| Approve and fund HRIS-to-IAM integration project | CTO / CFO | [DATE] |
| Establish executive ownership of vulnerability SLA compliance with weekly reporting | CISO | [DATE] |
| Review and formally accept or reject outstanding risk management letter items | CISO / Audit Committee | [DATE] |
| Confirm management responses to all findings are completed | [Name] | [DATE] |

---

## How We Compare

> Optional section — include when benchmarking data is available.

Based on benchmarking data from [source: Gartner / industry peer group / AICPA], organizations of similar size and profile typically achieve:

| Metric | Industry Median | Our Performance | Gap |
|--------|----------------|-----------------|-----|
| Account deprovisioning within SLA | 95%+ | 72% | -23% |
| Critical vuln remediation within SLA | 85%+ | 60% | -25% |
| Employee security training completion | 90%+ | 98% | +8% |
| Vendor assessment coverage (Tier 1) | 95%+ | 87% | -8% |

---

## What Happens Next

1. **Management responses due:** [DATE] — All finding owners to submit formal written responses
2. **Remediation tracking begins:** [DATE] — Monthly status updates to CISO
3. **Audit Committee briefing:** [DATE] — Significant Deficiencies formally communicated to Audit Committee per IIA Standards
4. **Follow-up audit:** [DATE] — Internal Audit will validate remediation of Significant Deficiencies at the next scheduled review

---

## About This Audit

This audit was conducted by [ORGANIZATION NAME]'s [Internal Audit / GRC] function in accordance with the International Standards for the Professional Practice of Internal Auditing (IIA Standards). Testing was performed on a sample basis; not all transactions or controls were tested. The findings in this report do not represent an exhaustive list of all control weaknesses that may exist.

This report is prepared for the exclusive use of [ORGANIZATION NAME]'s management and Audit Committee and is not intended for external distribution.

---

*Executive Summary Version: 1.0 | Audit Reference: [IA-XXXX-XXX]*

```
Prepared By:   _______________________  Date: __________
Approved By:   _______________________  Date: __________
(Chief Audit Executive)
```
