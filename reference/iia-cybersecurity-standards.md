# IIA Cybersecurity Audit Standards Reference

**Source Documents:**
- IIA International Standards for the Professional Practice of Internal Auditing (IPPF 2024)
- IIA Global Technology Audit Guide (GTAG): Auditing Cybersecurity in a Digital Age (2nd Ed.)
- IIA GTAG: Identity and Access Management
- IIA Practice Guide: IT General Controls
- IIA Three Lines Model (2020)

---

## Part 1: IIA Standards Applicable to Cybersecurity Audits

### Core Mandatory Standards

#### Standard 9.1 — Engagement Planning

> Internal auditors must develop and document a plan for each engagement, including the engagement's objectives, scope, timing, and resource allocations.

**Cybersecurity Application:**
- Define the specific cybersecurity domains in scope (access control, vulnerability management, etc.)
- Document the risk basis for scope selection
- Identify frameworks applicable (SOC 2, ISO 27001, NIST CSF, PCI-DSS)
- Establish timing to align with the audit period and evidence availability

**Required Engagement Plan Elements:**
1. Engagement objectives aligned to business risk
2. Scope — systems, processes, timeframe, frameworks
3. Risk and control assessment (inherent vs. residual risk)
4. Staffing plan with required competencies (CISA, CISSP, etc.)
5. Sampling methodology reference
6. Coordination with external auditors (avoid duplication)

---

#### Standard 9.2 — Risk Assessment in Engagement Planning

> Internal auditors must conduct a preliminary assessment of risks relevant to the activity under review.

**Cybersecurity Risk Domains to Assess in Planning:**

| Domain | Inherent Risk Drivers | Key Controls to Test |
|--------|----------------------|---------------------|
| Identity & Access | Number of users, system criticality, privileged accounts | Provisioning, MFA, access reviews, deprovisioning |
| Vulnerability Management | Attack surface size, patch cycle, internet exposure | Scan frequency, SLA compliance, pen testing |
| Incident Response | Data sensitivity, regulatory obligations, IR maturity | IRP quality, testing cadence, tabletop exercises |
| Change Management | Change velocity, deployment automation, code quality | CAB approval, testing, SoD in deployment |
| Third-Party Risk | Data shared, vendor criticality, contract coverage | Assessments, contracts, ongoing monitoring |
| Data Protection | Volume of PII/regulated data, encryption, DLP | Encryption at rest/in transit, DLP, data classification |

---

#### Standard 9.3 — Engagement Objectives

> Engagement objectives must reflect the results of the preliminary risk assessment.

**Cybersecurity Audit Objective Examples:**

*For Access Control:*
> Assess whether user access to production systems is provisioned, modified, and revoked through a formal, authorized process that enforces the principle of least privilege.

*For Vulnerability Management:*
> Evaluate whether the organization's vulnerability management program identifies, tracks, and remediates security vulnerabilities within policy-defined SLAs, commensurate with the severity and exploitability of identified vulnerabilities.

*For Incident Response:*
> Determine whether the organization has an effective incident response capability that can detect, contain, investigate, and remediate cybersecurity incidents in a timely manner.

---

#### Standard 9.4 — Engagement Scope

> The scope of an engagement must be sufficient to achieve the engagement's objectives.

**Cybersecurity Scope Pitfalls to Avoid:**
- Scoping out cloud environments while systems operate in the cloud
- Testing access controls in Okta but not the underlying systems Okta protects
- Reviewing vulnerability scanning but not penetration testing
- Assessing policy but not operating effectiveness of controls
- Limiting access review testing to one system when 6 are in scope

---

#### Standard 11.1 — Analyzing and Evaluating

> Internal auditors must base conclusions and engagement results on appropriate analyses and evaluations.

**Cybersecurity Analysis Techniques:**

| Technique | Application |
|-----------|-------------|
| Control testing (transaction sampling) | Access provisioning, change management, terminations |
| Configuration review | MFA settings, firewall rules, encryption configuration |
| Data analytics | User account vs. HR roster matching, vulnerability age analysis |
| Walkthrough | Process understanding before testing begins |
| Inquiry | Gap between policy and practice; understanding root causes |
| Direct observation | Live system demonstration; physical access inspection |
| Reperformance | Auditor independently re-runs a control procedure |
| Benchmarking | Compare metrics against industry standards |

---

#### Standard 11.2 — Documenting Information

> Internal auditors must document sufficient, reliable, relevant, and useful information to support the engagement's findings and conclusions.

**Workpaper Documentation Requirements for Cybersecurity Audits:**

Each workpaper must include:
- [ ] Clear identification (audit name, date, auditor, reviewer)
- [ ] Population definition and completeness verification
- [ ] Sampling methodology and sample selected
- [ ] Testing procedures performed
- [ ] Evidence obtained (with exhibit references)
- [ ] Results of testing (pass/fail per item)
- [ ] Exception documentation (CCCE format)
- [ ] Conclusion on control effectiveness
- [ ] Deficiency classification if applicable
- [ ] Cross-reference to other workpapers and evidence index

---

#### Standard 11.4 — Communicating Results

> Internal auditors must communicate the results of engagements.

**Required Elements of Cybersecurity Audit Communications:**

| Element | Description |
|---------|-------------|
| Objectives | What the engagement was designed to assess |
| Scope | What was included and excluded |
| Methodology | How testing was performed |
| Findings | Criteria, Condition, Cause, Effect (CCCE) for each finding |
| Conclusions | Overall assessment / rating |
| Recommendations | Actionable, prioritized |
| Management Responses | Written responses to all findings |
| Distribution | Appropriate stakeholders (management, Audit Committee, Board) |

---

#### Standard 11.5 — Communicating Quality of Information

> If an engagement communication is not in conformance with the Standards, the internal auditor must disclose the deviation and the impact on the engagement.

**Application:** If evidence was not obtained for a specific control (e.g., evidence unavailable, system not accessible), document:
- What was intended to be tested
- Why it could not be tested
- The impact on the audit conclusion
- Whether the scope limitation affects the overall opinion

---

#### Standard 11.6 — Errors and Omissions

> If a final communication contains a significant error or omission, the chief audit executive must communicate corrected information to all parties who received the original communication.

---

#### Standard 11.7 — Significant Risk Communication

> If internal auditors conclude that management has accepted a level of risk that may be unacceptable to the organization, they must discuss the matter with senior management.

**Cybersecurity Application:**
- When management formally accepts risk of an unpatched critical vulnerability
- When management declines to remediate a Material Weakness
- When compensating controls are insufficient for the risk level

If management does not address the unacceptable risk, internal audit must communicate the matter to the Board or Audit Committee.

---

## Part 2: IIA GTAG — Cybersecurity Audit Framework

The IIA GTAG: Auditing Cybersecurity in a Digital Age provides guidance organized around the NIST Cybersecurity Framework (CSF) functions. The following maps IIA GTAG audit considerations to the five CSF functions:

### IDENTIFY

**Focus Areas:**
- Asset inventory and classification (software, hardware, data, people)
- Business environment understanding (critical functions, dependencies)
- Governance framework (policies, roles, risk appetite)
- Risk assessment process

**IIA GTAG Key Questions:**
1. Does the organization maintain a current, complete inventory of all hardware, software, and data assets?
2. Is the organization's risk appetite for cybersecurity formally defined and communicated?
3. Are dependencies on critical third parties and supply chain identified?
4. Is the cybersecurity risk assessment process formally documented, performed at least annually, and used to drive control prioritization?

### PROTECT

**Focus Areas:**
- Identity management and access control
- Security awareness and training
- Data security (encryption, DLP, classification)
- Information protection processes (policy, procedures, configuration)
- Maintenance (patching, vulnerability management)
- Protective technology (firewalls, EDR, WAF)

**IIA GTAG Key Questions:**
1. Are access rights granted based on least privilege and business need?
2. Are MFA and strong authentication enforced for all systems?
3. Is sensitive data encrypted at rest and in transit?
4. Are systems patched per a defined, risk-based schedule?
5. Are employees trained and tested on security awareness annually?

### DETECT

**Focus Areas:**
- Anomalies and events detection (SIEM, IDS/IPS, UBA)
- Continuous security monitoring
- Detection processes (incident classification, triage)

**IIA GTAG Key Questions:**
1. Is a Security Information and Event Management (SIEM) system deployed and actively monitored?
2. Are detection use cases tested and tuned to reduce false positive fatigue?
3. Is the mean time to detect (MTTD) tracked and benchmarked?
4. Are logs retained for a minimum of 12 months with 90 days accessible?

### RESPOND

**Focus Areas:**
- Response planning (IRP)
- Communications (internal, external, regulatory)
- Analysis (forensics, post-incident review)
- Mitigation (containment, eradication)
- Improvements (lessons learned)

**IIA GTAG Key Questions:**
1. Is a formal, tested Incident Response Plan in place?
2. Are communication templates and escalation paths pre-defined?
3. Are post-incident reviews performed after significant incidents?
4. Is there a breach notification procedure mapped to regulatory requirements (GDPR 72-hour, state breach laws)?

### RECOVER

**Focus Areas:**
- Recovery planning (BCP/DRP)
- Improvements (updated plans post-incident)
- Communications (status updates during recovery)

**IIA GTAG Key Questions:**
1. Are Recovery Time Objectives (RTOs) and Recovery Point Objectives (RPOs) formally defined and tested?
2. Are BCP/DR tests performed at least annually and documented?
3. Is backup integrity tested regularly (restore tests)?
4. Are lessons from recovery exercises incorporated into updated plans?

---

## Part 3: IIA Three Lines Model — Cybersecurity Context

The IIA Three Lines Model (2020) describes the roles of the three lines of defense in managing cybersecurity risk:

```
┌─────────────────────────────────────────────────────────────────┐
│                   GOVERNING BODY (BOARD)                        │
│  Accountability for oversight of cybersecurity risk & controls  │
├──────────────────────────────────────────────────────────────────┤
│                        MANAGEMENT                               │
│  ┌─────────────────────┐   ┌─────────────────────────────────┐  │
│  │   FIRST LINE        │   │       SECOND LINE               │  │
│  │   Operations        │   │       Risk & Compliance         │  │
│  │                     │   │                                 │  │
│  │  • IT teams running │   │  • CISO / Security function     │  │
│  │    systems          │   │  • GRC team                     │  │
│  │  • Engineers        │   │  • Risk management              │  │
│  │    implementing     │   │  • Policy & standard-setting    │  │
│  │    controls         │   │  • Compliance monitoring        │  │
│  │  • Responsible for  │   │  • Risk assessments             │  │
│  │    control design   │   │  • Third-party risk program     │  │
│  │    and operation    │   │  • Security metrics reporting   │  │
│  └─────────────────────┘   └─────────────────────────────────┘  │
├──────────────────────────────────────────────────────────────────┤
│                       THIRD LINE                                │
│                    Internal Audit                               │
│                                                                 │
│  • Independent, objective assurance on risk and controls        │
│  • Tests operating effectiveness of 1st and 2nd line controls   │
│  • Reports to Audit Committee (not management)                  │
│  • Covers cybersecurity as a key audit area                     │
│  • May use co-sourcing with specialized cyber audit expertise   │
└──────────────────────────────────────────────────────────────────┘
```

**Internal Audit's (Third Line) Cybersecurity Responsibilities:**
1. Audit the design and operating effectiveness of cybersecurity controls
2. Assess the second line's risk management and compliance monitoring effectiveness
3. Evaluate whether the CISO has appropriate resources, authority, and independence
4. Report significant cybersecurity findings to the Audit Committee without management filtering
5. Avoid performing management functions (implementing controls, running the security program) to maintain independence

**Independence Boundary:** Internal Audit should NOT design, implement, or operate cybersecurity controls. Doing so creates a self-review threat to independence.

---

## Part 4: Competency Requirements for Cybersecurity Auditors

Per IIA Standard 7.2 (Competence), cybersecurity auditors must have or develop:

### Core Competencies

| Competency Area | Knowledge Required |
|----------------|-------------------|
| Risk-based auditing | Inherent vs. residual risk, risk ranking, audit universe |
| Control frameworks | SOC 2, ISO 27001, NIST CSF, NIST SP 800-53, PCI-DSS |
| IT general controls | Access management, change management, operations, development |
| Sampling methodology | AICPA sampling standards, sample size determination |
| Evidence evaluation | Sufficiency, appropriateness, reliability |
| Finding classification | Control deficiency, significant deficiency, material weakness |
| Workpaper standards | IIA, AICPA documentation requirements |

### Technical Knowledge (Domain-Specific)

| Domain | Recommended Knowledge |
|--------|----------------------|
| Identity & Access | IAM platforms (Okta, Azure AD), PAM tools, RBAC concepts |
| Vulnerability Management | Scanning tools (Tenable, Qualys), CVSS scoring, patch management |
| Network Security | Firewall architecture, segmentation, TLS/encryption |
| Cloud Security | AWS/Azure/GCP shared responsibility, cloud IAM, CSA CAIQ |
| Application Security | OWASP Top 10, SDLC, SAST/DAST |
| Incident Response | NIST IR lifecycle, SIEM platforms, forensics basics |

### Certifications Supporting Cybersecurity Audit Competency

| Certification | Body | Focus |
|--------------|------|-------|
| CISA | ISACA | IT audit, control, and assurance |
| CISSP | (ISC)² | Broad cybersecurity domains |
| CISM | ISACA | Information security management |
| CIA | IIA | Internal audit professional standards |
| CEH / OSCP | EC-Council / Offensive Security | Penetration testing / ethical hacking |
| AWS/Azure/GCP Security Specialty | Cloud providers | Cloud security architecture and controls |
| CompTIA Security+ | CompTIA | Broad cybersecurity foundations |

---

## Part 5: Quick Reference — IIA Standards Numbering (2024)

| Standard | Topic | Cybersecurity Relevance |
|----------|-------|------------------------|
| 5.0 | Independence and Objectivity | Auditor must not have operational responsibility for cyber controls |
| 7.0 | Proficiency and Due Care | Cyber auditors need technical competency; co-source if not available |
| 9.1 | Engagement Planning | Risk-based scope selection for cyber audit |
| 9.2 | Risk Assessment | Cyber risk assessment drives audit priority |
| 9.3 | Engagement Objectives | Must be specific to cybersecurity control objectives |
| 11.1 | Analyzing and Evaluating | Testing, sampling, configuration review |
| 11.2 | Documenting Information | Workpaper completeness and quality |
| 11.4 | Communicating Results | Findings must address CCCE; rated; management response |
| 11.7 | Significant Risk Communication | Escalate unacceptable cyber risk to Board if management declines to act |
| 12.1 | Follow-Up | Track remediation of cyber audit findings |

---

*IIA Cybersecurity Standards Reference Version: 1.0*
*Sources: IIA IPPF 2024, IIA GTAG: Auditing Cybersecurity in a Digital Age (2nd Ed.), IIA Three Lines Model 2020*
