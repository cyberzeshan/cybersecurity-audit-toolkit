# Control Testing Workpaper — Template

```
================================================================================
CONTROL TESTING WORKPAPER
================================================================================
Engagement:     [ENGAGEMENT NAME / CLIENT]
Audit Period:   [START DATE] – [END DATE]
Control ID:     [e.g., CC6.1-01 / ISO A.5.15 / AC-02 / PCI Req 7.2]
Control Title:  [e.g., User Access Provisioning and Quarterly Review]
Framework:      ☐ SOC 2 TSC  ☐ ISO 27001  ☐ NIST SP 800-53  ☐ PCI-DSS  ☐ Other: ____
Auditor:        [AUDITOR NAME]
Date Prepared:  [DATE]
Review Status:  ☐ Prepared   ☐ In Review   ☐ Reviewed   ☐ Approved
================================================================================
```

---

## 1. Control Objective

> State what the control is designed to prevent or detect. Be specific.

**Example:**
> To ensure that access to production systems is granted only upon authorized request, is commensurate with the user's job responsibilities (principle of least privilege), and is reviewed quarterly to identify and remove inappropriate access.

[YOUR CONTROL OBJECTIVE]

---

## 2. Control Description (As Documented)

> Describe the control exactly as the organization has documented it. Do not paraphrase. Quote the policy or control procedure directly.

**Source Document:** [Policy name, version number, section reference]
**Control Frequency:** ☐ Continuous  ☐ Daily  ☐ Weekly  ☐ Monthly  ☐ Quarterly  ☐ Annual  ☐ Event-driven
**Control Type:** ☐ Preventive  ☐ Detective  ☐ Corrective  ☐ Deterrent
**Control Nature:** ☐ Automated  ☐ Manual  ☐ Hybrid (partially automated)
**Control Owner:** [Name and title]
**System(s) Involved:** [IAM platform, ITSM, ERP, etc.]

---

## 3. Population Definition

> Define the complete set of items from which the sample will be drawn.

| Field | Detail |
|-------|--------|
| Audit Period | [e.g., January 1, 2025 – December 31, 2025] |
| Total Population | [e.g., 847 user provisioning requests submitted during the audit period] |
| Population Source | [e.g., IT Service Desk — ServiceNow export dated 2025-01-10] |
| Population Completeness Check | [How was population completeness verified? e.g., Compared count against HRIS new-hire count; reconciled to HR records] |
| Population Stratification | [e.g., Split by: privileged (42) vs standard (805) to ensure privileged access items are included in sample] |

---

## 4. Sampling Methodology

> Document how the sample was selected and the basis for sample size.

**Sampling Approach:**
☐ Statistical (Random) — results can be projected to full population
☑ Judgmental — targeted selection based on risk; results cannot be statistically projected
☐ Haphazard — incidental; must document no bias

**Sample Size:** [e.g., 25 items]
**Basis for Sample Size:** [e.g., AICPA AT-C Section 205 guidance; population > 250, moderate risk = 25 items. See Sampling Methodology reference guide.]
**Selection Method:** [e.g., Random number generator applied to sorted population list; high-risk items selected separately]
**High-Risk Items Selected Outside Sample:** [e.g., All privileged access grants (n=42) were included in the population; 10 were selected based on elevated risk]

### Sample Selected

| # | Item ID | Date | Description | Basis for Selection |
|---|---------|------|-------------|---------------------|
| 1 | [e.g., TKT-2025-0042] | | [e.g., New hire provisioning — Finance Manager] | Random |
| 2 | [e.g., TKT-2025-0187] | | [e.g., Role change — Engineering to DevOps] | Random |
| 3 | [e.g., TKT-2025-0891] | | [e.g., Privileged access grant — Production DB Admin] | Risk-based |
| 4 | | | | |
| 5 | | | | |
| ... | | | | |
| 25 | | | | |

---

## 5. Testing Procedures

> Document each test step to be performed. These procedures should be derived from the audit program.

**Step 1: [Obtain and Inspect the Request]**
- Obtain the access request ticket / provisioning form
- Verify: Request includes business justification
- Verify: Manager or authorized approver is identified on the request
- Verify: Approval was obtained BEFORE access was granted (approval timestamp precedes provisioning timestamp)
- Verify: The access requested is commensurate with the user's role (no unnecessary permissions)

**Step 2: [Verify Implementation in the Identity System]**
- Obtain user account record from the identity system (AD / Okta / IAM platform)
- Verify: Account was created / modified on or after the approval date
- Verify: Access level in the system matches what was approved — no additional permissions
- Verify: No other access was granted to this user at the same time that was not requested

**Step 3: [Inspect the Periodic Access Review]**
- Obtain the most recent access review report covering the user/system
- Verify: The user's account was included in the access review
- Verify: The reviewer certified the access as appropriate (or flagged it for removal)
- Verify: Any flagged access was remediated within the policy-defined SLA (typically 30 days)

**Step 4: [Test for Termination Controls — if applicable]**
- Obtain HR termination record for the user
- Cross-reference against identity system — confirm no active accounts remain
- Verify: Account was disabled within 24 hours of HR termination date

---

## 6. Results

> Document testing results for each sample item and each test step.

| # | Item ID | Step 1: Request & Authorization | Step 2: System Implementation | Step 3: Access Review | Step 4: Termination | Exception? | Notes |
|---|---------|--------------------------------|------------------------------|-----------------------|--------------------|-----------|-------|
| 1 | | ☐ Pass ☐ Fail ☐ N/A | ☐ Pass ☐ Fail ☐ N/A | ☐ Pass ☐ Fail ☐ N/A | ☐ Pass ☐ Fail ☐ N/A | ☐ Yes ☐ No | |
| 2 | | ☐ Pass ☐ Fail ☐ N/A | ☐ Pass ☐ Fail ☐ N/A | ☐ Pass ☐ Fail ☐ N/A | ☐ Pass ☐ Fail ☐ N/A | ☐ Yes ☐ No | |
| 3 | | ☐ Pass ☐ Fail ☐ N/A | ☐ Pass ☐ Fail ☐ N/A | ☐ Pass ☐ Fail ☐ N/A | ☐ Pass ☐ Fail ☐ N/A | ☐ Yes ☐ No | |
| 4 | | ☐ Pass ☐ Fail ☐ N/A | ☐ Pass ☐ Fail ☐ N/A | ☐ Pass ☐ Fail ☐ N/A | ☐ Pass ☐ Fail ☐ N/A | ☐ Yes ☐ No | |
| 5 | | ☐ Pass ☐ Fail ☐ N/A | ☐ Pass ☐ Fail ☐ N/A | ☐ Pass ☐ Fail ☐ N/A | ☐ Pass ☐ Fail ☐ N/A | ☐ Yes ☐ No | |
| ... | | | | | | | |

**Summary:**
- Total items tested: ___
- Items with no exceptions: ___
- Items with exceptions: ___
- **Exception rate: ___% (tolerable rate for this risk level: ___%)** 

---

## 7. Exception Detail

> For every exception identified, complete one block below.

---

**Exception #[n]** — Item ID: [TKT-XXXX-XXXX]

| Field | Detail |
|-------|--------|
| Step Failed | [e.g., Step 1 — Access was granted before approval was documented] |
| Criteria | [State the exact expectation that was not met] |
| Condition Found | [Describe exactly what was found] |
| Root Cause | [e.g., IT admin provisioned based on verbal instruction without waiting for ticket approval] |
| Impact | ☐ High  ☐ Medium  ☐ Low — [Explain: e.g., access level was appropriate; issue is procedural] |
| Compensating Control | [e.g., Quarterly access review performed on 2025-04-15 confirmed access was appropriate] |
| Management Response | [Obtain from control owner and paste here] |
| Remediation Plan | [e.g., Automate provisioning workflow to require ticket approval before access is granted] |
| Target Remediation Date | [DATE] |

---

## 8. Conclusion

**Control Effectiveness:**
☐ **Effective** — Control is designed and operating effectively. No exceptions noted.
☐ **Effective with Minor Exception** — Control is substantially effective. Exception(s) noted; no material impact on control objective.
☐ **Not Effective** — Control is not operating effectively. Deficiency identified. See findings section.
☐ **Unable to Test** — [Explain reason]

**Overall Assessment Narrative:**

[Provide 2–4 sentences summarizing: what was tested, what was found, and overall conclusion. Reference exception rate relative to tolerable threshold. If effective: state that. If not effective: state what specific step failed and why it constitutes a deficiency.]

**Example:**
> The user access provisioning control was tested over a sample of 25 items drawn from a population of 847 provisioning requests. Twenty-four of 25 items passed all testing steps. One exception was identified (4% rate): access was provisioned two days before manager approval was documented, representing a procedural gap. Given that the access granted was appropriate and a compensating quarterly access review confirmed appropriateness, this exception does not represent a material risk. The exception rate of 4% is within the tolerable threshold of 5% established for this moderate-risk control.

---

## 9. Deficiency Classification (Complete if Exception Identified)

☐ **Control Deficiency** — Design or operating gap that is less than significant; isolated occurrence; compensating controls exist
☐ **Significant Deficiency** — Deficiency or combination that is less than a material weakness but warrants governance attention; systemic pattern
☐ **Material Weakness** — Reasonable possibility that a material misstatement, significant loss, or regulatory breach will not be prevented or detected; no effective compensating controls

**Classification Rationale:** [Explain why this classification was selected. Reference exception rate, pattern vs. isolated, and whether compensating controls exist.]

---

## 10. Evidence Index

> List all supporting documentation obtained and referenced in this workpaper.

| Exhibit | Description | Source System / Document | Obtained By | Date Obtained |
|---------|-------------|--------------------------|-------------|---------------|
| Exhibit A | [e.g., Access provisioning tickets — 25 items] | ServiceNow export | | |
| Exhibit B | [e.g., Active directory user account listings for sample users] | IT AD export | | |
| Exhibit C | [e.g., Q1–Q4 Access Review reports] | SharePoint | | |
| Exhibit D | [e.g., HR Termination list for audit period] | HRIS export | | |
| Exhibit E | [e.g., IAM access role configuration screenshot] | Okta console | | |

---

```
================================================================================
Workpaper Prepared By:  _________________________  Date: ______________
Workpaper Reviewed By:  _________________________  Date: ______________
Workpaper Approved By:  _________________________  Date: ______________
================================================================================
```

---

## Quick Reference: Sample Size Guide

| Population Size | Low Risk | Moderate Risk | High Risk |
|:---------------|:--------:|:-------------:|:---------:|
| 1–25 | 100% | 100% | 100% |
| 26–50 | 5 | 10 | 15 |
| 51–100 | 10 | 15 | 20 |
| 101–250 | 15 | 20 | 25 |
| 251–500 | 20 | 25 | 30 |
| 500+ | 25 | 30 | 40 |

*Based on AICPA AT-C Section 205 / PCAOB AS 2315 guidance for non-statistical sampling. Adjust upward for higher tolerable rate of deviation or lower risk tolerance.*

---

*Template Version: 1.0 | Aligned to: IIA Standards, AICPA AT-C 205, PCAOB AS 2315*
