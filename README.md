# 🔍 Cybersecurity Audit Toolkit

<div align="center">

![SOC2](https://img.shields.io/badge/SOC_2_Type_II-4A154B?style=flat-square&logoColor=white)
![ISO27001](https://img.shields.io/badge/ISO_27001%3A2022-0066CC?style=flat-square&logoColor=white)
![IIA](https://img.shields.io/badge/IIA_Standards-8B0000?style=flat-square&logoColor=white)
![NIST](https://img.shields.io/badge/NIST_SP_800--53A-003087?style=flat-square&logoColor=white)
![PCIDSS](https://img.shields.io/badge/PCI--DSS_v4-FF6B00?style=flat-square&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

**Professional-grade internal audit programs, control testing workpapers, evidence request lists, and audit report templates — aligned to IIA standards and designed to survive regulator and external auditor scrutiny.**

</div>

---

## 📖 Overview

A cybersecurity audit toolkit built for **practitioners who do the actual work** — not consultants who deliver slide decks. Every artifact here is modeled on real audit engagements across finance, healthcare, and technology sectors.

Whether you're running an internal audit function, preparing for a SOC 2 Type II examination, or supporting a regulatory audit, this toolkit gives you the structured, defensible artifacts that auditors demand.

---

## 📂 Repository Structure

```
cybersecurity-audit-toolkit/
│
├── audit-programs/
│   ├── soc2-audit-program.md                # SOC 2 TSC full audit program
│   ├── iso27001-internal-audit-program.md   # ISO 27001 clause & Annex A audit program
│   ├── access-control-audit-program.md      # Logical access control deep-dive audit
│   ├── vulnerability-mgmt-audit-program.md  # Vuln management program audit
│   └── third-party-risk-audit-program.md    # TPRM audit program
│
├── workpapers/
│   ├── control-testing-workpaper-template.md  # Standard control test workpaper
│   ├── sample-selection-workpaper.md          # Statistical & judgmental sampling
│   ├── walkthrough-workpaper-template.md      # Process walkthrough documentation
│   └── deficiency-assessment-workpaper.md     # Control deficiency evaluation & rating
│
├── evidence/
│   ├── soc2-evidence-request-list.md          # SOC 2 Type II client evidence requests
│   ├── iso27001-evidence-catalog.md           # ISO 27001 evidence requirements
│   └── evidence-quality-assessment.md         # How to evaluate evidence sufficiency
│
├── reports/
│   ├── internal-audit-report-template.md      # Full internal audit report format
│   ├── management-letter-template.md          # Control deficiency management letter
│   └── executive-summary-template.md          # C-suite audit summary format
│
└── reference/
    ├── deficiency-classification-guide.md     # Material weakness vs. significant deficiency
    ├── audit-sampling-methodology.md          # AICPA sampling standards for IT audits
    └── iia-cybersecurity-standards.md         # IIA GTAG cyber audit reference
```

---

## 📋 Control Testing Workpaper — Template

```
================================================================================
CONTROL TESTING WORKPAPER
================================================================================
Audit:          [AUDIT NAME / ENGAGEMENT]
Control ID:     [e.g., CC6.1-01 / ISO A.5.15 / AC-02]
Control Title:  [e.g., User Access Provisioning & Quarterly Review]
Framework:      SOC 2 TSC / ISO 27001 / NIST SP 800-53 / PCI-DSS
Auditor:        [AUDITOR NAME]
Date:           [DATE]
Review Status:  ☐ Prepared  ☐ Reviewed  ☐ Approved
================================================================================

CONTROL OBJECTIVE
─────────────────────────────────────────────────────────────────────────────
[State what the control is designed to prevent or detect. Be specific.]

Example: "To ensure that user access to production systems is granted only upon
authorized request, is commensurate with job responsibilities (least privilege),
and is reviewed quarterly to remove or modify inappropriate access."

CONTROL DESCRIPTION (AS DOCUMENTED)
─────────────────────────────────────────────────────────────────────────────
[Describe the control exactly as the organization has documented it. Do not
paraphrase. Quote the policy or control procedure directly.]

Source Document: [Policy name, version, section]
Control Frequency: [Continuous / Daily / Weekly / Monthly / Quarterly / Annual]
Control Type: [Preventive / Detective / Corrective]
Control Nature: [Automated / Manual / Hybrid]
Control Owner: [Name and title of control owner]

POPULATION DEFINITION
─────────────────────────────────────────────────────────────────────────────
Audit Period:       [e.g., January 1, 2024 – December 31, 2024]
Total Population:   [e.g., 847 user provisioning requests during the audit period]
Population Source:  [e.g., IT Service Desk ticketing system — exported 2024-01-10]
Completeness Check: [How was population completeness verified?]

SAMPLING METHODOLOGY
─────────────────────────────────────────────────────────────────────────────
Sampling Approach:  ☐ Statistical (Random)  ☑ Judgmental  ☐ Haphazard
Sample Size:        [e.g., 25 items per AICPA AT-C Section 205 guidance]
Sample Basis:       [Rationale for sample size — risk level, population size]
Selection Method:   [e.g., Random number generator, stratified selection]
High-Risk Items:    [Items selected outside sample due to elevated risk]

Sample Selected:
| # | Item ID | Date | Description | Basis for Selection |
|---|---------|------|-------------|---------------------|
| 1 | TKT-2024-0042 | 2024-02-14 | New hire provisioning - Finance | Random |
| 2 | TKT-2024-0187 | 2024-04-03 | Role change - Engineering → DevOps | Random |
| 3 | TKT-2024-0891 | 2024-09-22 | Privileged access grant - Production DB | Risk-based |
...

TESTING PROCEDURES
─────────────────────────────────────────────────────────────────────────────
Step 1: Obtain and inspect the access provisioning request (ticket/form)
        ├── Verify: Request includes business justification
        ├── Verify: Manager or authorized approver approved the request
        ├── Verify: Approval occurred BEFORE access was granted
        └── Verify: Access granted matches what was requested (no scope creep)

Step 2: Verify implementation of access in the identity system (AD/Okta/IAM)
        ├── Verify: User account created/modified on or after approval date
        ├── Verify: Access level matches approved request
        └── Verify: No additional access granted beyond what was approved

Step 3: Inspect the most recent quarterly access review
        ├── Obtain: Access review report (Q1–Q4 for audit period)
        ├── Verify: All accounts in scope were reviewed
        ├── Verify: Inappropriate access was removed within 30 days of identification
        └── Verify: Manager or authorized reviewer signed off on each review

Step 4: Test for terminated users
        ├── Obtain: HR termination list for audit period
        ├── Cross-reference: Against active accounts in identity provider
        ├── Verify: Accounts disabled within 24 hours of termination
        └── Verify: No terminated users retain active access

RESULTS
─────────────────────────────────────────────────────────────────────────────
| # | Item | Step 1 | Step 2 | Step 3 | Step 4 | Exception? | Notes |
|---|------|--------|--------|--------|--------|-----------|-------|
| 1 | TKT-2024-0042 | ✅ Pass | ✅ Pass | ✅ Pass | N/A | No | |
| 2 | TKT-2024-0187 | ✅ Pass | ⚠️ Except | ✅ Pass | N/A | Yes | Access granted 2 days before approval |
| 3 | TKT-2024-0891 | ✅ Pass | ✅ Pass | ✅ Pass | N/A | No | |

Exceptions Identified: 1 of 25 items (4%)
Exception Rate: 4% (within tolerable threshold of 5% for this control risk level)

EXCEPTION DETAIL
─────────────────────────────────────────────────────────────────────────────
Exception #1: TKT-2024-0187
Criteria: Access was granted on 2024-04-01. Approval was obtained on 2024-04-03.
Finding: Access was provisioned 2 days before manager approval was documented.
Root Cause: Manual provisioning by IT admin based on verbal instruction.
Impact: Low — access level was appropriate; issue is procedural
Compensating Control: Access review conducted 2024-04-15 confirmed appropriateness
Management Response: [Obtain from control owner]
Remediation: Automate provisioning workflow to block access until approval is recorded

CONCLUSION
─────────────────────────────────────────────────────────────────────────────
☐ Control operating effectively — No exceptions requiring reporting
☑ Control operating with minor exception — Exception noted; no material impact
☐ Control not operating effectively — Deficiency identified; see finding
☐ Control not tested — Explain:

Overall Assessment: The access provisioning control is substantially effective.
One exception was identified (4% rate), representing a process gap in the sequencing
of provisioning vs. approval documentation. Given the existence of compensating
controls (access review), this is assessed as a CONTROL DEFICIENCY (not significant
deficiency or material weakness).

DEFICIENCY CLASSIFICATION (if applicable)
─────────────────────────────────────────────────────────────────────────────
☑ Control Deficiency — Exception isolated, compensating controls exist
☐ Significant Deficiency — Reasonable possibility of more than inconsequential error
☐ Material Weakness — Reasonable possibility of material misstatement / serious risk

EVIDENCE INDEX
─────────────────────────────────────────────────────────────────────────────
| Exhibit | Description | Source | Obtained |
|---------|-------------|--------|---------|
| A | Access provisioning tickets (25 items) | ServiceNow export | 2024-01-15 |
| B | Active directory user account listings | IT export | 2024-01-15 |
| C | Q1-Q4 2024 Access Review Reports | SharePoint | 2024-01-15 |
| D | HR Termination List 2024 | HRIS export | 2024-01-16 |

Workpaper Prepared By: _________________ Date: _______
Workpaper Reviewed By: _________________ Date: _______
================================================================================
```

---

## 📊 Control Deficiency Classification Guide

| Classification | Definition | Reporting Requirement | Example |
|:---|:---|:---|:---|
| **Control Deficiency** | Design or operating effectiveness gap that is less than significant | Internal management communication | Access approval occasionally post-dated |
| **Significant Deficiency** | Deficiency (or combination) that is less than material weakness but warrants attention of those charged with governance | Audit Committee | No quarterly access reviews performed |
| **Material Weakness** | Reasonable possibility that a material misstatement or significant risk will not be prevented or detected | Board, external auditors, regulators (SOX/public companies) | Terminated users retain system access for months; no compensating controls |

---

## 📄 License

MIT License — free to use, adapt, and distribute with attribution.

---

<div align="center">
<i>Built by <a href="https://github.com/cyberzeshan">Zeshan Ahmad</a> · GRC Engineer & Cybersecurity SME</i>
</div>
