# Management Letter — Template

> A management letter communicates control deficiencies, significant deficiencies, and other observations to management and those charged with governance. It is separate from (and less formal than) the full audit report, and is commonly issued as a companion document to SOC 2 reports, financial statement audits, and regulatory examinations.

---

```
================================================================================
MANAGEMENT LETTER
[CONFIDENTIAL — RESTRICTED DISTRIBUTION]
================================================================================
Date:               [DATE]
To:                 [CEO / CTO / CISO / Audit Committee Chair]
                    [ORGANIZATION NAME]
From:               [AUDITOR NAME / FIRM NAME]
Re:                 Management Letter — Cybersecurity Controls
                    Audit Period: [START DATE] – [END DATE]
================================================================================
```

---

[DATE]

[RECIPIENT NAME]
[TITLE]
[ORGANIZATION NAME]
[ADDRESS]

Dear [Mr./Ms./Mx. LAST NAME]:

---

## Introduction

In connection with our [SOC 2 Type II examination / ISO 27001 internal audit / cybersecurity controls assessment] of [ORGANIZATION NAME] for the period [START DATE] through [END DATE], we identified certain matters relating to your organization's internal controls over information security that we believe are important to bring to management's attention.

This letter is intended to assist management in fulfilling its responsibility for the design, implementation, and maintenance of effective internal controls. The observations included here do not affect our [examination opinion / audit conclusion], but are presented to help management strengthen controls and reduce risk.

This letter is intended solely for the use of management and those charged with governance of [ORGANIZATION NAME] and is not intended for any other purpose.

---

## Control Deficiency Summary

We identified the following matters during our work. Matters are classified as follows:

- **Significant Deficiency:** A deficiency, or combination of deficiencies, that is less than a material weakness but is important enough to warrant the attention of those charged with governance.
- **Control Deficiency:** A gap in design or operating effectiveness that is less than a significant deficiency; typically isolated or with compensating controls in place.
- **Observation:** A matter that is not a deficiency at this time but represents an opportunity for improvement or a trend that should be monitored.

---

## Significant Deficiencies

### [SD-01] — Terminated Employee Accounts Not Timely Disabled

**Classification:** Significant Deficiency
**Control Area:** Logical Access — User Deprovisioning
**Framework Reference:** SOC 2 CC6.3 / ISO 27001 A.5.18

**Background:**
Management is required by its Identity Management Procedure to disable accounts for terminated employees within 24 hours of the HR-recorded termination date. This control is designed to prevent unauthorized access to systems and data by former employees.

**What We Found:**
In our testing of 25 terminated employee accounts selected from the audit period, we found that 7 accounts (28%) were not disabled within the 24-hour policy requirement. Of these, 2 accounts remained active for more than 7 days and were associated with access to finance systems and customer personal data.

**Why This Matters:**
Former employees with active accounts retain the technical ability to access sensitive systems after their employment ends. This creates risk of unauthorized data access, data theft, or sabotage, and represents a departure from the organization's stated policy and from the requirements of SOC 2 CC6.3.

**Root Cause:**
The deprovisioning process relies on manual email notification from HR to IT. There is no automated integration between the HRIS (Workday) and the identity management system (Okta), creating opportunities for delay and missed notifications.

**Our Recommendation:**
We recommend management:
1. Implement automated HRIS-to-IAM integration to trigger immediate account suspension upon HR termination recording, with a target completion date of [DATE]
2. Implement a daily automated reconciliation comparing HRIS terminations against active IAM accounts as an interim detective control
3. Configure SIEM alerting to detect post-termination authentication activity

**Management Response:**
> [Paste management's response here — to be completed before issuance]

---

### [SD-02] — [Second Significant Deficiency Title]

**Classification:** Significant Deficiency
**Control Area:** [e.g., Vulnerability Management]
**Framework Reference:** [SOC 2 CC7.5 / ISO 27001 A.8.8]

**Background:**
[Brief context]

**What We Found:**
[Brief, specific condition]

**Why This Matters:**
[Brief risk statement]

**Root Cause:**
[Root cause]

**Our Recommendation:**
[Recommendations]

**Management Response:**
> [To be completed]

---

## Control Deficiencies

### [CD-01] — [Control Deficiency Title]

**Classification:** Control Deficiency
**Control Area:** [Area]
**Framework Reference:** [Reference]

**What We Found:**
[Condition]

**Our Recommendation:**
[Recommendation]

**Management Response:**
> [To be completed]

---

## Observations and Recommendations

Observations do not represent control deficiencies but are presented as opportunities for strengthening the control environment.

### [OBS-01] — Vendor Security Assessment Coverage

**Area:** Third-Party Risk Management

**Observation:**
During our review of the vendor inventory, we noted that 8 of 47 vendors classified as Tier 2 (moderate risk) had not received a security assessment in the past 24 months. While Tier 1 vendors were fully assessed, the Tier 2 coverage gap represents an increasing exposure, particularly as some Tier 2 vendors have expanded the scope of data they process.

**Recommendation:**
We recommend scheduling security assessments for all overdue Tier 2 vendors within the next 90 days and implementing a tracking calendar to ensure assessments are renewed before expiry.

---

### [OBS-02] — [Second Observation Title]

**Area:** [Area]

**Observation:**
[Statement]

**Recommendation:**
[Recommendation]

---

## Matters Communicated to Those Charged with Governance

In addition to this management letter, we are communicating the Significant Deficiencies identified above directly to the Audit Committee in accordance with our audit obligations. Specifically:

- **SD-01** (Terminated Account Deprovisioning) — Reportable to Audit Committee per [IIA Standards / AICPA AT-C 205 / SOC 2 engagement terms]
- **SD-02** ([Title]) — Reportable to Audit Committee

These matters will be included in our report to the Audit Committee at the [DATE] meeting.

---

## Management Action Plan Tracking

We request that management provide a formal written response to each finding and observation identified in this letter, including:

1. Whether management agrees or disagrees with the finding (with explanation if disagreeing)
2. The specific remediation action to be taken
3. The name and title of the person responsible for remediation
4. The target completion date

Please return completed management responses to [AUDITOR NAME] at [EMAIL] no later than [DATE — typically 2 weeks after letter issuance].

We will follow up on the status of open management action items in [DATE — next audit / quarterly review].

---

## Prior Year Management Letter Follow-Up

> For continuing engagements, track the status of findings from prior periods.

| Prior Finding | Original Rating | Target Date | Current Status | Evidence of Remediation |
|--------------|----------------|-------------|----------------|------------------------|
| [Prior SD-01] | Significant Deficiency | [DATE] | ☐ Remediated  ☐ In Progress  ☐ Not Started | |
| [Prior CD-01] | Control Deficiency | [DATE] | ☐ Remediated  ☐ In Progress  ☐ Not Started | |

**Repeat Findings:**
> Note: [Finding SD-01 — Terminated Account Deprovisioning] was also identified in our prior year assessment. Management's remediation plan has not yet been fully implemented. Repeat findings of this nature represent an elevated risk and are noted accordingly in our current period assessment.

---

## Closing

This management letter is based on work performed as part of the [engagement type] for the period [START DATE] through [END DATE]. Our procedures were not designed to identify all matters that might be relevant to management's assessment of controls, and accordingly, we are not expressing an opinion on the overall effectiveness of the organization's internal control.

We appreciate the cooperation and assistance of management and staff during our engagement. We are available to discuss any of the matters in this letter at your convenience.

Respectfully submitted,

[AUDITOR NAME]
[TITLE]
[ORGANIZATION / FIRM]
[DATE]

---

```
Acknowledged and Agreed:

Management Representative: _______________________  Date: __________
Title:                    _______________________
```

---

*Management Letter Template Version: 1.0*
*Reference: AICPA AT-C Section 265, IIA Practice Advisory 2440-1*
