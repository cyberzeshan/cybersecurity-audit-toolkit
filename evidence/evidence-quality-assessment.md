# Evidence Quality Assessment Guide

**Purpose:** Help auditors evaluate whether evidence obtained is sufficient, appropriate, and reliable to support audit conclusions.
**Applicable Engagements:** SOC 2, ISO 27001, Internal Audit, Regulatory Compliance
**Reference Standards:** IIA Standards (2330), AICPA AT-C Section 205, ISAE 3000

---

## Overview: What Makes Evidence Good?

Evidence must satisfy three core qualities for it to be used to support an audit conclusion:

| Quality | Definition | Key Question |
|---------|------------|-------------|
| **Sufficient** | The quantity of evidence is enough to support the conclusion | "Do I have enough items/coverage to draw this conclusion?" |
| **Appropriate** | The evidence is relevant to the control objective and reliable in its source | "Does this evidence actually prove what I need it to prove?" |
| **Reliable** | The evidence can be trusted based on its source and how it was obtained | "Can I rely on this evidence, or could it have been altered/fabricated?" |

Evidence that fails any one of these criteria must be supplemented or substituted before a conclusion can be drawn.

---

## Section 1: Sufficiency Assessment

### 1.1 Is the Sample Size Sufficient?

Use the following table to evaluate whether the quantity of evidence tested is adequate for the risk level of the control.

| Control Risk Level | Minimum Sample Size (Population > 250) | Basis |
|-------------------|----------------------------------------|-------|
| Low | 15–20 items | Low potential impact; controls not heavily relied upon |
| Moderate | 25 items | Standard SOC 2 / ISO 27001 control; relied upon by auditor |
| High | 30–40 items | High impact; critical control; relied upon for significant risk |
| Population ≤ 25 | 100% (all items) | Test full population for small populations |

### 1.2 Coverage Assessment

For controls that are continuous or event-driven (not periodic), coverage should span the entire audit period, not just a point in time.

| Control Type | Coverage Requirement | Sufficiency Check |
|-------------|---------------------|-------------------|
| Periodic (quarterly review) | Evidence for each required cycle | Were all 4 quarters covered? Were all systems reviewed? |
| Event-driven (provisioning, changes) | Sample spanning full audit period | Does the sample include items from all months? Is early/late period represented? |
| Continuous (monitoring, logging) | Evidence at multiple points during period | Are there no gaps > 30 days in monitoring evidence? |
| One-time (annual policy review) | One occurrence per required cycle | Was it performed in the audit period? |

### 1.3 Sufficiency Red Flags

- Sample contains items from only one or two months of a 12-month audit period
- Population completeness cannot be verified (no reconciliation performed)
- Only management attestation with no supporting corroborating documentation
- Coverage report shows < 95% of assets / users covered (without explanation)

---

## Section 2: Appropriateness Assessment

### 2.1 Relevance: Does the Evidence Prove What You Need?

Evidence must directly address the control objective. Common mismatches:

| Control Objective | Insufficient Evidence | Appropriate Evidence |
|-------------------|----------------------|---------------------|
| Access is reviewed quarterly | Policy stating reviews are required | Completed access review report signed by reviewer |
| MFA is enforced | MFA policy document | IAM platform screenshot showing MFA enforcement setting + user enrollment report |
| Patches applied within SLA | Patch management policy | Patch deployment records with dates + rescan showing vulnerability closed |
| Backup is tested | Backup configuration screenshot | Restore test record showing data was successfully restored and verified |
| Changes are approved before deployment | Change management policy | Individual change tickets showing approval timestamp < deployment timestamp |

### 2.2 Appropriateness Assessment Questions

For each piece of evidence, ask:

1. **Does this evidence show that the control operated, or only that it was designed?**
   - A policy document shows design. A completed approval record shows operation.

2. **Is this evidence for the right time period?**
   - Evidence from outside the audit period does not demonstrate operating effectiveness during the period.

3. **Is this evidence from the right system / scope?**
   - Access review for System A does not demonstrate controls over System B (which is also in scope).

4. **Does the evidence address the specific exception criteria?**
   - If testing approval before provisioning, the evidence must show both the approval timestamp AND the provisioning timestamp, not just that an approval exists.

---

## Section 3: Reliability Assessment

### 3.1 Source Reliability Hierarchy

Evidence reliability depends heavily on its source. Rank evidence from most to least reliable:

| Rank | Source Type | Description | Examples |
|------|-------------|-------------|---------|
| 1 | **Auditor-obtained directly** | Auditor pulls directly from system with own credentials | Auditor-run query in AD, direct system access, auditor-observed real-time |
| 2 | **Third-party originated** | Created or provided by independent third party | SOC 2 report from external auditor, pen test from independent firm, bank confirmation |
| 3 | **System-generated** | Automated output from IT systems with appropriate controls | SIEM log exports, ITSM ticket exports, automated compliance scan reports |
| 4 | **Client-prepared with corroboration** | Provided by client but auditor can verify against another source | HR termination list corroborated against HRIS direct access |
| 5 | **Management attestation with documentation** | Management assertion supported by underlying records | Manager certifies access review; underlying access review spreadsheet provided |
| 6 | **Management attestation only** | Management assertion with no corroborating documentation | Verbal confirmation or written assertion without supporting evidence |

> **Rule:** Never rely solely on Rank 5–6 evidence for key controls. Always seek corroboration from a higher-ranked source.

### 3.2 Reliability Threats to Assess

| Threat | How to Identify | Mitigation |
|--------|-----------------|-----------|
| Evidence may have been altered | Spreadsheet provided rather than system export; inconsistent formatting | Request direct system export; verify with system administrator |
| Evidence may be incomplete | Client provided only a subset without explanation | Request population completeness verification; obtain from source system directly |
| Evidence is from outside audit period | Document date / system timestamp does not match audit period | Verify file timestamps, system export parameters, metadata |
| Evidence could be fabricated | Formatting inconsistencies; metadata shows creation after audit period | Request native system output; observe system demonstration live |
| Screenshot evidence is ambiguous | Screenshot doesn't show system name, date, or context | Request screenshot with visible URL bar, date/time, and system identifier |

### 3.3 Evaluating Screenshots as Evidence

Screenshots are commonly used but carry reliability risk. Apply these standards:

**Acceptable screenshot evidence must include:**
- [ ] Visible system name / URL / application identifier
- [ ] Date and time stamp visible (system clock or browser tab)
- [ ] The specific setting / configuration / data being tested
- [ ] Username or account context visible where relevant

**Screenshots that are NOT acceptable:**
- Cropped to show only the relevant field (no system context)
- Date/time not visible or not readable
- Configuration could have been temporarily changed for the screenshot
- From a test/staging environment rather than production

**When screenshots are insufficient:** Supplement with direct system observation (walk the auditor through the system live) or system-generated export.

---

## Section 4: Evidence Evaluation Checklist

Use this checklist to evaluate each piece of evidence before relying on it in a workpaper.

```
EVIDENCE EVALUATION CHECKLIST
================================================================================
Evidence Item: _____________________________________________
Exhibit Reference: _________________________________________

SUFFICIENCY
[ ] Sample size meets or exceeds minimum for control risk level
[ ] Coverage spans the full audit period (or all required cycles)
[ ] Population completeness was verified before sampling
[ ] No significant coverage gaps exist

APPROPRIATENESS
[ ] Evidence directly addresses the control objective being tested
[ ] Evidence is from the correct time period (within audit period)
[ ] Evidence covers all in-scope systems / users / assets
[ ] Evidence addresses the specific step being tested (not just general control existence)

RELIABILITY
[ ] Source reliability is at least Rank 3 (system-generated or better)
[ ] If client-prepared (Rank 4–5): corroborating source was obtained
[ ] Screenshots include: system name, date/time, and relevant context
[ ] No indicators of alteration or incompleteness identified
[ ] Evidence was obtained directly by auditor or confirmed against direct source

OVERALL ASSESSMENT
[ ] SUFFICIENT — Evidence quantity is adequate
[ ] APPROPRIATE — Evidence is relevant and addresses the objective
[ ] RELIABLE — Evidence source is credible and can be relied upon

[ ] ACCEPTED — Evidence is acceptable for use in workpaper
[ ] SUPPLEMENTAL EVIDENCE NEEDED — [describe what is needed]
[ ] EVIDENCE REJECTED — [describe reason and alternative obtained]

Evaluated By: _____________________  Date: _______________
================================================================================
```

---

## Section 5: Common Evidence Mistakes and Corrections

| Mistake | Why It's a Problem | Correction |
|---------|-------------------|-----------|
| Accepting a policy document as proof a control operates | Policies show design, not operation | Obtain transactional evidence (ticket, log, report) showing the control ran |
| Using a single-point-in-time screenshot for a continuous control | Doesn't demonstrate control operated throughout the period | Obtain multiple snapshots at different points OR a system-generated log for the full period |
| Accepting an access review report without validating what was reviewed | Review may not have covered all systems or all users | Confirm: (a) systems in scope, (b) user count matches account export, (c) reviewer certified the right data |
| Not verifying population completeness before sampling | Sample may exclude significant items | Always reconcile the provided population against an independent source |
| Relying on a vendor's self-attestation for security controls | Self-attestation is management assertion only | Require SOC 2 Type II, ISO 27001 cert, or third-party-validated questionnaire |
| Accepting screenshots without date or system context | Evidence cannot be tied to the audit period or confirmed as production | Require retake with full context visible, or obtain system-generated export instead |
| Testing only operating effectiveness when a design deficiency exists | Testing operation of a poorly designed control is misleading | Address design deficiency first; note design gap in workpaper regardless of operating results |

---

## Section 6: Evidence Documentation Standards

### 6.1 Labeling Evidence

Each piece of evidence in a workpaper must be:

1. **Labeled** with an Exhibit reference (e.g., Exhibit A, WP-03-B)
2. **Described** — one sentence explaining what the exhibit is and why it is relevant
3. **Sourced** — system, person, and date obtained
4. **Cross-referenced** — from the procedure that used it, to the exhibit

### 6.2 Evidence Retention Requirements

| Engagement Type | Minimum Retention | Standard |
|----------------|-------------------|----------|
| SOC 2 (CPA firm) | 7 years | AICPA standards |
| ISO 27001 Internal Audit | 3 years (or per ISMS policy) | ISO 27001 Clause 7.5 |
| Internal Audit (IIA) | 5–7 years | IIA Standard 2330.A1 |
| PCI-DSS Audit | 3 years | PCI-DSS Requirement 12.3 |
| Regulatory (HIPAA, GDPR) | Per regulatory requirement | Regulation-specific |

### 6.3 Sensitive Evidence Handling

- **Personal Data in Evidence:** Minimize retention of personal identifiable information (PII). Anonymize or pseudonymize where the audit objective can still be met.
- **System Credentials:** Never document system credentials in workpapers. Use credential reference labels.
- **Client Confidential Data:** Store all client evidence in secured, access-controlled systems. Do not store on personal devices.

---

*Evidence Quality Assessment Guide Version: 1.0*
*Reference: IIA Standards 2330, AICPA AT-C Section 205, ISAE 3000, PCAOB AS 2301*
