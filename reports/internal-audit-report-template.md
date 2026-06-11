# Internal Audit Report — Template

---

```
================================================================================
INTERNAL AUDIT REPORT
================================================================================
Report Title:       [e.g., Cybersecurity Controls Audit — Logical Access and
                    Vulnerability Management]
Audit Reference:    [e.g., IA-2025-003]
Organization:       [ORGANIZATION NAME]
Audit Period:       [START DATE] – [END DATE]
Report Date:        [DATE]
Classification:     CONFIDENTIAL — For Internal Distribution Only
================================================================================
Distribution:       Chief Information Security Officer
                    Chief Technology Officer
                    Chief Financial Officer (if applicable)
                    Audit Committee Chair
                    [Other stakeholders as appropriate]
================================================================================
```

---

## 1. Executive Summary

### 1.1 Audit Purpose and Background

This report presents the results of the [TITLE] internal audit conducted by the [Internal Audit / GRC] team for the period [START DATE] through [END DATE]. The audit was conducted in accordance with the International Standards for the Professional Practice of Internal Auditing (IIA Standards) and the [ORGANIZATION NAME] Internal Audit Charter.

The audit was commissioned to provide independent assurance on the design and operating effectiveness of [ORGANIZATION NAME]'s cybersecurity controls, with particular focus on [describe scope, e.g., logical access management and vulnerability management].

### 1.2 Overall Audit Rating

> Assign an overall rating to the audit area. Ratings communicate the aggregate control health to management at a glance.

| Overall Rating | Criteria |
|:---|:---|
| **Satisfactory** | Controls are adequately designed and operating effectively. Minor observations noted with no significant risks. |
| **Needs Improvement** | Controls are generally in place but one or more significant deficiencies exist that, if unaddressed, could escalate to material risk. |
| **Unsatisfactory** | Multiple significant deficiencies or a material weakness identified. Material risk to the organization exists. Immediate management attention required. |

**Overall Audit Rating:** ☐ Satisfactory  ☑ Needs Improvement  ☐ Unsatisfactory

**Rationale:**
[2–3 sentences explaining the overall rating. Reference the number and severity of findings. Example:]

> The audit identified [X] findings across the areas tested, including [Y] significant deficiencies and [Z] control deficiencies. While most controls are operating effectively, systemic gaps were identified in [area], which represent elevated risk if not remediated. Detailed findings and management action plans are presented in Section 4.

### 1.3 Finding Summary

| # | Finding Title | Rating | Area | Management Response |
|---|--------------|--------|------|---------------------|
| FIND-01 | [e.g., Terminated accounts not disabled within 24-hour SLA] | Significant Deficiency | Access Control | Accepted — See Section 4.1 |
| FIND-02 | [e.g., Critical vulnerabilities not remediated within policy SLA] | Significant Deficiency | Vulnerability Mgmt | Accepted — See Section 4.2 |
| FIND-03 | [e.g., Emergency changes lack retroactive approval] | Control Deficiency | Change Management | Accepted — See Section 4.3 |

---

## 2. Audit Scope and Objectives

### 2.1 Objectives

This audit was designed to:

1. Evaluate the design and operating effectiveness of logical access controls, including provisioning, deprovisioning, privileged access management, and periodic access reviews
2. Assess the vulnerability management program's ability to identify, track, and remediate vulnerabilities within defined SLAs
3. [Additional objectives as applicable]

### 2.2 Scope

**In-Scope Systems and Processes:**
- [System 1, e.g., Okta (Identity Provider)]
- [System 2, e.g., AWS Production Environment]
- [System 3, e.g., Tenable Vulnerability Management]
- [Process: User provisioning and deprovisioning]
- [Process: Quarterly access reviews]
- [Process: Vulnerability scanning and remediation]

**Out of Scope:**
- [e.g., Physical access controls (covered by separate audit — IA-2025-001)]
- [e.g., Development environments]

**Geographic Scope:** [e.g., All U.S.-based operations; UK operations excluded pending local audit]

**Audit Period:** [START DATE] – [END DATE]

### 2.3 Audit Standards and Methodology

This audit was conducted in accordance with:
- International Standards for the Professional Practice of Internal Auditing (IIA Standards 2024)
- AICPA Trust Services Criteria (for SOC 2-aligned testing)
- [Other applicable standards]

**Methodology:** The audit included:
- Inquiry and interviews with key process owners and management
- Review of policies, procedures, and documentation
- Process walkthroughs (at least one transaction traced per key control)
- Control testing using statistical and judgmental sampling techniques
- Data analytics where applicable

**Sampling Approach:** Sample sizes were determined based on AICPA AT-C Section 205 non-statistical sampling guidance, calibrated to control risk level. Sample sizes ranged from [X] to [X] items per control.

---

## 3. Areas of Strength

> Identify 2–4 areas where controls are well-designed and operating effectively. This demonstrates objectivity and provides balance.

The audit identified the following areas where controls are functioning effectively:

**3.1 Multi-Factor Authentication (MFA) Enforcement**
MFA is enforced for 100% of user accounts across all in-scope systems. Configuration review and testing of a sample of 25 accounts confirmed that no exceptions exist. This is a strong control that significantly reduces the risk of credential-based attacks.

**3.2 Change Management Authorization**
Testing of 25 change requests found that 24 of 25 (96%) were authorized by the Change Advisory Board prior to production deployment and had associated test evidence. The one exception was an emergency change with a documented retroactive approval (see Finding FIND-03).

**3.3 [Third Area of Strength]**

---

## 4. Findings and Recommendations

> Each finding follows the CCCE format: Criteria, Condition, Cause, Effect. Each is rated and includes a management response and action plan.

---

### Finding FIND-01: [Finding Title]

**Rating:** ☑ Significant Deficiency  ☐ Control Deficiency  ☐ Material Weakness
**Area:** [e.g., Logical Access — Deprovisioning]
**Framework Reference:** [e.g., SOC 2 CC6.3 / ISO 27001 A.5.18 / NIST AC-02(2)]

---

**Criteria:**
Per [Organization Name]'s Identity Management Procedure (v2.1, Section 4.3), user accounts for terminated employees must be disabled within 24 hours of the HR-recorded termination date. This aligns with industry best practice and SOC 2 CC6.3 requirements.

**Condition:**
Testing of the user deprovisioning control included a sample of 25 terminated employees selected from the HR termination list for the audit period. Of the 25 items tested:
- **18 (72%)** — accounts disabled within 24 hours — Pass
- **5 (20%)** — accounts disabled 2–7 days after termination — Exception
- **2 (8%)** — accounts disabled more than 7 days after termination — Exception

**Exception rate: 7 of 25 (28%) — exceeds tolerable threshold of 5%**

Notable exceptions included two employees with access to financial systems and customer PII whose accounts remained active for 9 and 14 days, respectively.

**Cause:**
The root cause is a structural process gap: there is no automated integration between the HRIS (Workday) and the identity management system (Okta). Termination notification to IT relies on manual email from HR, which is subject to delays and oversight failures.

**Effect:**
Terminated employees retained active system credentials beyond the policy-required window, creating an exposure period of up to 14 calendar days. During this time, they theoretically retained the ability to access corporate systems, including email, financial reporting tools, and customer data repositories. This represents a risk of data theft or sabotage by departing employees, and a direct exception to SOC 2 CC6.3, which is reportable to the SOC 2 user entities.

---

**Recommendations:**

| Priority | Recommendation | Owner | Target Date |
|----------|---------------|-------|-------------|
| High | Implement automated HRIS-to-IAM integration: Workday termination triggers automatic Okta account suspension within 1 hour | IT / HR | [DATE] |
| High | Implement daily automated reconciliation: cross-reference HRIS terminations against Okta active accounts; send exception report to IT Security for same-day remediation | IT Security | [DATE] |
| Medium | Configure SIEM alerting for terminated employee authentication: alert if a terminated user's account is used after their HR termination date | Security Ops | [DATE] |

**Management Response:**

> [Paste management's written response here]
>
> Management accepts this finding. We acknowledge the process gap in our HRIS-IAM notification workflow. We have initiated a project to integrate Workday with Okta via SCIM provisioning, with an estimated completion date of [DATE]. In the interim, we will implement a daily HR-to-IT notification procedure effective immediately, with IT Security acknowledging each notification within 2 hours.
>
> **Management Action Owner:** [Name, Title]
> **Target Completion Date:** [DATE]

**Internal Audit Response to Management:**
Management's response is reasonable. Internal Audit will follow up on completion of the HRIS-IAM integration at the [Q3 2025] audit committee meeting.

---

### Finding FIND-02: [Finding Title]

**Rating:** ☑ Significant Deficiency  ☐ Control Deficiency  ☐ Material Weakness
**Area:** [e.g., Vulnerability Management — Remediation SLA]
**Framework Reference:** [SOC 2 CC7.5 / ISO 27001 A.8.8 / PCI-DSS Req 6.3.3]

---

**Criteria:** [State the policy or standard]

**Condition:** [State what was found — exception count and rate]

**Cause:** [Root cause]

**Effect:** [Risk and impact]

---

**Recommendations:**

| Priority | Recommendation | Owner | Target Date |
|----------|---------------|-------|-------------|
| | | | |

**Management Response:** [To be completed by management]

---

### Finding FIND-03: [Finding Title]

**Rating:** ☐ Significant Deficiency  ☑ Control Deficiency  ☐ Material Weakness
**Area:** [e.g., Change Management — Emergency Changes]
**Framework Reference:** [SOC 2 CC8.1]

---

**Criteria:** [Statement]

**Condition:** [Exception found]

**Cause:** [Root cause]

**Effect:** [Risk and impact]

---

**Recommendations:**

| Priority | Recommendation | Owner | Target Date |
|----------|---------------|-------|-------------|
| | | | |

**Management Response:** [To be completed]

---

## 5. Management Action Plan Summary

| Finding | Priority | Action | Owner | Target Date | Status |
|---------|----------|--------|-------|-------------|--------|
| FIND-01 | High | HRIS-to-IAM automated integration | [Name] | [DATE] | Not Started |
| FIND-01 | High | Daily reconciliation report | [Name] | [DATE] | Not Started |
| FIND-02 | High | [Action] | [Name] | [DATE] | Not Started |
| FIND-03 | Medium | [Action] | [Name] | [DATE] | Not Started |

---

## 6. Audit Team and Acknowledgments

**Internal Audit Team:**
| Name | Role | Responsibilities |
|------|------|-----------------|
| [Name] | Lead Auditor | Overall audit direction, report review and approval |
| [Name] | Senior Auditor | Fieldwork, control testing, workpaper preparation |
| [Name] | Staff Auditor | Evidence collection, sample testing |

**Management Participants:**
| Name | Title | Area |
|------|-------|------|
| [Name] | CISO | Audit sponsor, final management review |
| [Name] | IT Manager | Process walkthroughs, evidence provision |
| [Name] | HR Manager | Termination and HRIS data |

---

## 7. Appendices

- **Appendix A:** Audit Program — [Title]
- **Appendix B:** Sample Selection Workpaper
- **Appendix C:** Control Testing Results Summary
- **Appendix D:** Management Response Letters

---

```
================================================================================
Report Prepared By:   ___________________________  Date: ______________
Report Reviewed By:   ___________________________  Date: ______________
Report Approved By:   ___________________________  Date: ______________
(Chief Audit Executive / Audit Director)
================================================================================
```

---

*Internal Audit Report Template Version: 1.0*
*Reference: IIA Standards 2400–2440, IIA Practice Advisory 2420-1*
