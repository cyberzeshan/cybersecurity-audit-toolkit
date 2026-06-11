# Control Deficiency Assessment Workpaper

**Engagement:** [ENGAGEMENT NAME]
**Audit Period:** [START DATE] – [END DATE]
**Deficiency Reference:** [e.g., FIND-2025-003]
**Control Area:** [e.g., User Deprovisioning — CC6.3 / A.5.18]
**Auditor:** [NAME]
**Date Prepared:** [DATE]
**Status:** ☐ Draft  ☐ Reviewed  ☐ Approved  ☐ Management Response Received

---

## Purpose

This workpaper documents the evaluation and classification of a control deficiency identified during audit testing. It supports the auditor's determination of whether the deficiency constitutes a control deficiency, significant deficiency, or material weakness, and provides the basis for the audit finding reported to management.

---

## Section 1: Finding Summary

| Field | Detail |
|-------|--------|
| Finding Title | [e.g., Terminated user accounts not disabled within policy-required 24-hour SLA] |
| Control Tested | [Control name and ID from audit program] |
| Framework Mapping | [e.g., SOC 2: CC6.3 / ISO 27001: A.5.18 / NIST: AC-02(2) / PCI-DSS: Req 8.3.4] |
| Finding Type | ☐ Design Deficiency  ☑ Operating Effectiveness Deficiency  ☐ Both |
| Identified During | ☐ Walkthrough  ☑ Control Testing  ☐ Inquiry  ☐ Other |
| Related Findings | [Reference any related or compounding findings] |

---

## Section 2: Condition, Criteria, Cause, and Effect (CCCE)

> The "4 Cs" framework is the standard for structured audit finding reporting. Every finding must address all four elements.

### 2.1 Criteria — What Should Be

> State the standard, policy, or expectation against which the condition is measured. Be specific with the source.

**Source:** [e.g., Acceptable Use Policy v2.3, Section 6.4; SOC 2 CC6.3]

**Criteria Statement:**

> Per the organization's Identity Management Procedure (v2.1, Section 4.3), user accounts for terminated employees must be disabled within 24 hours of the HR-recorded termination date. This requirement aligns with SOC 2 TSC CC6.3, which requires that access be revoked when no longer needed, and with industry best practice for limiting insider threat risk.

[WRITE YOUR CRITERIA HERE]

---

### 2.2 Condition — What Was Found

> State exactly what was observed during audit testing. Be factual, specific, and non-editorial. Cite sample items.

**Condition Statement:**

> During testing of the user deprovisioning control, a sample of 25 terminated employee accounts was selected from the HR termination list for the period January 1 – December 31, 2025. Of the 25 items tested:
> - 18 accounts (72%) were disabled within 24 hours of termination — pass
> - 5 accounts (20%) were disabled between 2–7 business days of termination — exception
> - 2 accounts (8%) were disabled more than 7 business days after termination — exception
>
> Total exceptions: 7 of 25 items (28% exception rate)
>
> Notable items:
> - EMP-2025-0447: Account remained active 14 days after termination date
> - EMP-2025-0812: Account active for 9 days; employee had access to finance systems
> - EMP-2025-1103: Account active for 6 days; employee had access to customer PII

[WRITE YOUR CONDITION HERE]

---

### 2.3 Cause — Why It Happened

> Identify the root cause. Distinguish between a people issue (lack of training, non-compliance), a process issue (unclear ownership, no automation), or a technology issue (system limitation, no automated trigger).

☑ **Process** — [The deprovisioning process relies on manual handoff from HR to IT via email. There is no automated trigger from the HRIS to the IAM system when a termination is recorded.]
☐ **People** — [e.g., IT administrators were not consistently checking the HR termination report]
☐ **Technology** — [e.g., HRIS and IAM system are not integrated]
☐ **Design** — [Control design did not account for cases where HR data entry is delayed]

**Root Cause Narrative:**

> The primary cause is a process and technology gap: the HRIS (Workday) and identity management system (Okta) are not integrated. HR records terminations in Workday, but notification to IT is done via manual email to the IT service desk. In 7 of 25 cases, the email was delayed, missed, or not acted upon within the 24-hour SLA. No automated workflow or daily reconciliation between Workday and Okta exists to detect lapses.

[WRITE YOUR CAUSE HERE]

---

### 2.4 Effect — What Could Go Wrong / What Did Go Wrong

> Describe the actual or potential impact. This is what makes the finding actionable. Quantify where possible.

**Actual Impact:**
> 7 terminated employee accounts remained active beyond the policy-required 24-hour window, creating a period of unauthorized access exposure. During this window, terminated employees theoretically retained the ability to access corporate systems, including email, finance applications, and customer data repositories.

**Potential Impact:**
> Unauthorized access by terminated employees to sensitive or regulated data (customer PII, financial records) could result in data theft, sabotage, or insider threat incidents. This type of access gap is a common factor in insider threat cases and is directly tested by SOC 2 auditors and HIPAA/PCI compliance assessors.

**Regulatory / Compliance Exposure:**
> Under SOC 2, this is a direct exception to CC6.3. Under PCI-DSS v4 Requirement 8.3.4, accounts for terminated users must be immediately removed. Failure to remediate could affect the organization's SOC 2 opinion or PCI-DSS compliance attestation.

[WRITE YOUR EFFECT HERE]

---

## Section 3: Deficiency Classification

> Classify the deficiency based on severity. This is an auditor's judgment, informed by the criteria below.

### 3.1 Classification Framework

| Classification | Definition | Reporting Destination | Examples |
|:---|:---|:---|:---|
| **Control Deficiency** | A gap in design or operating effectiveness that is less than a significant deficiency. Isolated occurrence; compensating controls exist; limited potential impact. | Management letter / Observations section | One approval missed in a 25-item sample; minor procedural deviation with compensating quarterly review |
| **Significant Deficiency** | Deficiency or combination of deficiencies that is less than a material weakness but is important enough to warrant attention of those charged with governance (Audit Committee). | Audit Committee | No quarterly access reviews performed for 2 of 6 systems; 20% exception rate on access deprovisioning with no compensating control |
| **Material Weakness** | Deficiency or combination in which there is a reasonable possibility that a material misstatement, significant loss, or critical risk will not be prevented or detected in a timely manner. | Board, external auditors, regulators, customers (SOC 2 adverse/qualified opinion) | Terminated users retain access for months; no effective compensating controls; system-level access to financial records |

### 3.2 Classification Decision

**Factors Considered:**

| Factor | Assessment | Rationale |
|--------|------------|-----------|
| Exception rate | 28% (7/25) | High exception rate indicating systemic failure |
| Is this an isolated incident or systemic? | Systemic | Applies to all terminations; root cause is structural (no HRIS integration) |
| Compensating controls | Partial | Quarterly access reviews exist; would catch violations within 90 days |
| Actual harm occurred? | Unknown | No confirmed unauthorized access; investigation not performed |
| Data sensitivity affected | High | Finance and PII systems involved in notable items |
| Period of exposure | Up to 14 days | Maximum exposure window was 14 calendar days |
| Regulatory exposure | High | SOC 2, PCI-DSS, and GDPR implications |
| Prior year finding? | ☑ Yes ☐ No | Similar finding in prior year audit; remediation incomplete |

**Classification Selected:**
☐ Control Deficiency
☑ **Significant Deficiency**
☐ Material Weakness

**Classification Rationale:**

> The deprovisioning failure is systemic (28% rate across the full audit period, stemming from a structural process gap) and involves systems with access to sensitive financial data and PII. While no confirmed unauthorized access has been identified and quarterly access reviews provide a partial compensating control, the 14-day maximum exposure window and the involvement of regulated data elevate this above a control deficiency. A material weakness determination is not made at this time because compensating controls exist, actual harm has not been confirmed, and the risk, while elevated, does not create a reasonable possibility of material financial misstatement. This is classified as a **Significant Deficiency** and is reportable to the Audit Committee.

---

## Section 4: Impact on Audit Opinion / Report

| Impact Area | Assessment |
|------------|-----------|
| SOC 2 Type II impact | Exception noted in CC6.3 testing; will be reported as exception in SOC 2 report if engagement proceeds |
| ISO 27001 impact | Nonconformity with A.5.18; to be reported as Minor Nonconformity |
| Overall audit opinion impact | ☐ No impact  ☑ Qualified exception noted  ☐ Adverse |
| Related controls affected | CC6.5 (Access Reviews — compensating), CC7.2 (Monitoring) |

---

## Section 5: Compensating Control Evaluation

> Assess whether compensating controls mitigate the risk of the deficiency during the gap period.

| Compensating Control | Description | Operating Effectiveness | Residual Risk Coverage |
|---------------------|-------------|------------------------|----------------------|
| Quarterly Access Reviews | System owners review all active accounts quarterly; inappropriate access flagged | ☑ Effective | Covers within 90 days; does not prevent initial exposure window |
| SIEM User Behavior Monitoring | Logs and alerts on anomalous access post-termination | ☐ Not configured for this scenario | No coverage |
| Privileged Account Daily Reconciliation | Privileged accounts reviewed against HR daily | ☑ Effective for privileged users only | Partial — standard accounts not covered |

**Compensating Control Conclusion:**
> Compensating controls provide partial mitigation: quarterly access reviews would catch violations within 90 days, and privileged account reconciliations address the highest-risk users. However, standard user accounts with access to PII and financial data are not covered by timely compensating controls. The combination of the primary control failure and limited compensating coverage supports the Significant Deficiency classification.

---

## Section 6: Management Response

**Management Response Requested By:** [DATE]
**Response Received:** ☐ Yes  ☐ No  ☐ Pending

**Management Response:**

> [Paste management's written response here — their explanation of the root cause, corrective action plan, and target remediation date]

---

## Section 7: Recommended Remediation

| # | Recommendation | Priority | Target Date | Owner |
|---|---------------|----------|-------------|-------|
| 1 | Implement automated HRIS-to-IAM integration: when HR marks an employee as terminated in Workday, trigger automatic Okta account suspension within 1 hour | High | [DATE] | IT / HR | 
| 2 | Implement a daily reconciliation report comparing HRIS terminated employees against IAM active accounts; report auto-emailed to IT security for same-day remediation | High | [DATE] | IT Security |
| 3 | Until automated integration is implemented, establish a process where HR sends a termination notification to IT immediately upon recording the termination, with an IT acknowledgment required within 2 hours | Interim | [DATE] | HR / IT |
| 4 | Add SIEM alerting for terminated employee access: cross-reference HRIS termination data against authentication logs; alert immediately if terminated user authenticates | Medium | [DATE] | Security Ops |

---

## Section 8: Evidence Index

| Exhibit | Description | Reference |
|---------|-------------|-----------|
| Exhibit A | Control testing workpaper — Deprovisioning (WP-04) | WP-04 |
| Exhibit B | Sample of 7 exception items — termination dates vs. account disable dates | WP-04 Exceptions |
| Exhibit C | HR termination list for audit period | Provided by HR |
| Exhibit D | IAM (Okta) account disable timestamps for sample | IT export |
| Exhibit E | Prior year finding reference (if applicable) | Prior year audit report |

---

```
================================================================================
Deficiency Assessment Prepared By:  ___________________  Date: ______________
Reviewed By:  ___________________   Date: ______________
Approved By:  ___________________   Date: ______________
Classification Concurred By (Partner/Director): ________  Date: ______________
================================================================================
```

---

*Deficiency Assessment Workpaper Version: 1.0*
*Reference: AICPA AT-C Section 205, PCAOB AS 2201 (Material Weakness), IIA Practice Advisory 2320-1*
