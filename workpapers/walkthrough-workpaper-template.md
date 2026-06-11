# Process Walkthrough Workpaper — Template

**Engagement:** [ENGAGEMENT NAME]
**Audit Period:** [START DATE] – [END DATE]
**Process Name:** [e.g., User Access Provisioning / Change Management / Incident Response]
**Framework Reference:** [e.g., SOC 2 CC6.1 / ISO 27001 A.5.15 / NIST AC-02]
**Auditor:** [NAME]
**Date of Walkthrough:** [DATE]
**Walkthrough Participants:** [Names, titles, contact information]

---

## Purpose of the Walkthrough

A walkthrough is a process inquiry and observation procedure designed to:

1. Confirm the auditor's understanding of how the control process actually operates (not just how it is documented)
2. Identify control design deficiencies or gaps between policy and practice
3. Confirm that the control can operate effectively before investing in transaction-level testing
4. Satisfy the requirement that at least one transaction is traced end-to-end through each key control

> A walkthrough is NOT a substitute for control testing. It validates design; control testing validates operating effectiveness.

---

## Section 1: Pre-Walkthrough Preparation

### 1.1 Documents Reviewed Before Walkthrough

| Document | Version | Date | Reviewed By |
|----------|---------|------|-------------|
| [Access Control Policy] | v[X.X] | | |
| [Identity Management Procedure] | v[X.X] | | |
| [Process flowchart / system diagram] | | | |
| [Prior year walkthrough workpaper] | | | |
| [Prior year audit findings related to this process] | | | |

### 1.2 Key Questions Prepared for Walkthrough

> Prior to the walkthrough, prepare the questions you intend to ask. Questions should be open-ended and designed to probe how the process really works.

1. Walk me through what happens from the moment an employee submits an access request to when they receive access. Who does what?
2. What system is used to submit and approve access requests? Is it automated or manual?
3. What happens if a manager is unavailable — can access be provisioned without approval?
4. How do you ensure that access granted matches only what was requested?
5. What controls prevent IT from granting access without an approved ticket?
6. How does the process change for privileged access compared to standard access?
7. What happens on an employee's last day — who initiates account deactivation, and how?
8. How often are access reviews performed? What does that process look like?
9. What happens when the access review identifies someone with inappropriate access?
10. Have there been any process changes in this area during the past 12 months?

---

## Section 2: Process Walkthrough Narrative

> Document the process exactly as described by the process owner during the walkthrough. Use the participant's own words where possible. Note any differences between documented policy and how the process actually works.

### 2.1 Process Initiation

**How does the process begin?**

[Narrative: Describe who initiates the process, what triggers it, and what the first step is.]

Example: Access requests are initiated by the requesting employee's manager via the ServiceNow IT portal. The manager submits a "New Access Request" form specifying the user's name, role, and systems needed. Employees cannot submit requests on their own behalf.

**Participant Statement:** "[Quote the participant directly if notable]"

**Policy Alignment:** ☐ Consistent with documented policy ☐ Inconsistent — [note gap]

---

### 2.2 Authorization / Approval

**How is the request reviewed and approved?**

[Narrative: Who approves, how, through what system, what information is reviewed before approving?]

**Participant Statement:** 

**Policy Alignment:** ☐ Consistent ☐ Inconsistent — [note gap]

---

### 2.3 Implementation / Control Execution

**How is the approved request carried out?**

[Narrative: Who implements the access? What system do they use? What prevents over-provisioning?]

**Participant Statement:**

**Policy Alignment:** ☐ Consistent ☐ Inconsistent — [note gap]

---

### 2.4 Verification / Quality Check

**How is accuracy verified after the control is executed?**

[Narrative: Is there a secondary check? Who confirms the access was implemented correctly?]

**Participant Statement:**

**Policy Alignment:** ☐ Consistent ☐ Inconsistent — [note gap]

---

### 2.5 Exception Handling

**What happens when the normal process cannot be followed?**

[Narrative: Emergency access, system outages, missing approver scenarios — how are exceptions handled?]

**Participant Statement:**

**Policy Alignment:** ☐ Consistent ☐ Inconsistent — [note gap]

---

### 2.6 Process Conclusion / Record Keeping

**How is the process closed out and documented?**

[Narrative: What records are kept? Where? For how long? Who can access them?]

**Participant Statement:**

**Policy Alignment:** ☐ Consistent ☐ Inconsistent — [note gap]

---

## Section 3: Transaction Trace (End-to-End)

> Select ONE recent transaction and trace it completely through the process from initiation to completion. This confirms the process works as described.

### 3.1 Transaction Selected

| Field | Detail |
|-------|--------|
| Transaction ID | [e.g., TKT-2025-0744] |
| Transaction Date | |
| Description | [e.g., New hire — Data Analyst — Finance team] |
| Selection Basis | [e.g., Most recent provisioning ticket as of walkthrough date] |

### 3.2 End-to-End Trace

| Step | Expected | Observed | Evidence | Pass/Fail |
|------|----------|----------|----------|-----------|
| 1. Request submitted | Manager submits via ServiceNow portal | | Exhibit WT-01 — ServiceNow ticket screenshot | |
| 2. Business justification included | Justification in request | | Exhibit WT-01 | |
| 3. Approval obtained before provisioning | Approval timestamp < provisioning timestamp | | Exhibit WT-01, WT-02 | |
| 4. Access provisioned correctly | Access matches approved request | | Exhibit WT-02 — IAM record screenshot | |
| 5. Ticket closed with evidence | Closure notes, attachments in ticket | | Exhibit WT-01 | |
| 6. User appears in next access review | User on access review list | | Exhibit WT-03 — Most recent access review | |

---

## Section 4: Control Design Assessment

> Based on the walkthrough, assess whether the control is designed effectively to achieve the control objective.

### 4.1 Design Evaluation Questions

| Question | Assessment | Notes |
|----------|------------|-------|
| Is the control clearly defined with specific procedures? | ☐ Yes ☐ No | |
| Does the control apply to all relevant scenarios (new hires, transfers, contractors, privileged access)? | ☐ Yes ☐ Partial ☐ No | |
| Are roles and responsibilities clearly assigned? | ☐ Yes ☐ No | |
| Are system/automated controls used where possible to prevent bypass? | ☐ Yes ☐ Partial ☐ No | |
| Is there a mechanism to detect if the control fails? | ☐ Yes ☐ No | |
| Does the control address the risk it is intended to mitigate? | ☐ Yes ☐ Partial ☐ No | |
| Are there compensating controls for gaps in the primary control? | ☐ Yes ☐ No ☐ N/A | |

### 4.2 Design Gaps Identified

| # | Gap Description | Root Cause | Severity | Recommendation |
|---|----------------|------------|----------|----------------|
| | | | | |

---

## Section 5: Policy vs. Practice Gaps

> Document any differences between the documented policy/procedure and how the process actually operates.

| # | Policy States | Actual Practice | Gap Severity | Implication |
|---|--------------|----------------|-------------|-------------|
| | | | ☐ High ☐ Med ☐ Low | |

---

## Section 6: Process Flowchart

> Insert or attach the process flowchart if one exists. If none exists, sketch the process as understood from the walkthrough.

```
[Walkthrough Process Flow — Example: User Access Provisioning]

  [Employee's Manager]         [IT Service Desk]         [IAM System]          [Access Review]
        |                             |                       |                       |
  Submits request via         Receives ticket,          Automated or          Quarterly review
  ServiceNow portal   ──────> reviews for           ──> manual account  ──>  by system owner;
        |                    completeness                 provisioning         certify or revoke
        |                             |                       |                       |
  Receives access             Confirms approval          Records change         Flags exceptions
  notification       <──────  before provisioning <───   in audit log   <───   for remediation
```

---

## Section 7: Walkthrough Conclusion

**Overall Design Effectiveness:**
☐ **Effectively Designed** — Control is well-designed to achieve its objective. No significant gaps identified between policy and practice. Proceed to control testing.
☐ **Design Gaps Noted** — Minor gaps between policy and practice identified. Control can still be tested with awareness of gaps. Findings noted.
☐ **Material Design Deficiency** — Control is not designed effectively to achieve its objective. Recommend remediation before testing operating effectiveness. Finding reported.

**Proceed to Control Testing?**
☐ Yes — proceed with sample-based testing
☐ No — design deficiency identified; testing effectiveness would not be meaningful. Report design deficiency.

**Auditor Observations:**

[2–4 sentences summarizing the walkthrough, key observations, any deviations from policy noted, and the overall conclusion on design effectiveness.]

---

## Section 8: Evidence Index

| Exhibit | Description | Obtained From | Date |
|---------|-------------|---------------|------|
| WT-01 | ServiceNow access request ticket (traced transaction) | IT Manager | |
| WT-02 | IAM system screenshot showing account provisioning | IT Administrator | |
| WT-03 | Most recent quarterly access review report | System Owner | |
| WT-04 | Walkthrough meeting notes / recording consent | Auditor | |

---

*Walkthrough Workpaper Version: 1.0 | Reference: IIA Practice Guide — Evaluating IT Controls, PCAOB AS 2110*

```
Prepared By:  _________________________  Date: ______________
Reviewed By:  _________________________  Date: ______________
```
