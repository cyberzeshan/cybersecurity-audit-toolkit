# SOC 2 Type II Audit Program

**Framework:** AICPA Trust Services Criteria (TSC) 2017 (as updated)
**Audit Type:** SOC 2 Type II
**Audit Period:** [START DATE] – [END DATE]
**Auditor:** [AUDITOR NAME]
**Organization:** [ORGANIZATION NAME]
**Date Prepared:** [DATE]

---

## Audit Scope

**In-Scope Systems:**
- [List production systems, platforms, and infrastructure in scope]

**In-Scope Trust Service Categories:**
- [x] Security (CC) — required
- [ ] Availability (A)
- [ ] Confidentiality (C)
- [ ] Processing Integrity (PI)
- [ ] Privacy (P)

**Excluded Systems / Carve-Outs:**
- [List any systems explicitly excluded and rationale]

---

## CC1 — Control Environment (COSO)

### CC1.1 — COSO Principle 1: Commitment to Integrity and Ethical Values

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 1.1.1 | Inspect the code of conduct / acceptable use policy. Confirm it addresses cybersecurity behaviors and is current (updated within 24 months). | Code of conduct, policy version log | |
| 1.1.2 | Select a sample of 25 employees hired or transferred during the audit period. Verify each acknowledged the code of conduct within 30 days. | HR onboarding records, signed acknowledgment logs | |
| 1.1.3 | Inquire of HR leadership regarding how violations of the code of conduct are reported and handled. Inspect 2–3 closed incident cases for evidence of consistent enforcement. | Incident/ethics case log, HR policy | |
| 1.1.4 | Confirm that the ethics/whistleblower hotline is operational and communicated to employees. | Hotline communication records, awareness materials | |

### CC1.2 — COSO Principle 2: Board Independence and Oversight

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 1.2.1 | Obtain and inspect board or audit committee charter. Verify cybersecurity oversight responsibilities are defined. | Board/Audit Committee charter | |
| 1.2.2 | Review board meeting minutes from the audit period. Confirm cybersecurity risk and program updates were presented to the board at least annually. | Board meeting minutes | |
| 1.2.3 | Verify that management provides the board with relevant, sufficient cybersecurity KPIs and risk metrics. | Board reporting packages | |

### CC1.3 — COSO Principle 3: Organizational Structure and Reporting Lines

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 1.3.1 | Obtain the current organizational chart. Verify the CISO / security function has appropriate reporting lines (direct to CTO, CEO, or Audit Committee). | Org chart | |
| 1.3.2 | Confirm that security roles and responsibilities are formally defined. | Role descriptions, RACI matrix | |
| 1.3.3 | Verify security headcount is commensurate with the size and risk profile of the organization. | Headcount report, budget allocation | |

### CC1.4 — COSO Principle 4: Commitment to Competence

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 1.4.1 | Inspect job descriptions for key security roles. Verify required competencies and qualifications are defined. | Job descriptions | |
| 1.4.2 | Select a sample of 5 security team members. Review evidence of relevant certifications or training completed during the audit period. | Training records, certification copies | |
| 1.4.3 | Confirm that annual security awareness training is mandatory and tracked for all employees. Inspect completion rates for the audit period. | LMS training completion reports | |

### CC1.5 — COSO Principle 5: Accountability

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 1.5.1 | Verify that performance objectives for the CISO and security team include measurable security metrics. | Performance reviews, objective-setting documentation | |
| 1.5.2 | Inspect the security metrics dashboard or scorecard used for management reporting. | KPI reports, dashboard screenshots | |

---

## CC2 — Communication and Information

### CC2.1 — Information Quality and Availability

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 2.1.1 | Inspect the asset inventory / CMDB. Verify all production assets are inventoried with owners, classification, and criticality assigned. | CMDB export, asset inventory | |
| 2.1.2 | Confirm that system data flow diagrams and architecture diagrams are current and reflect in-scope systems. | Architecture diagrams, DFDs | |

### CC2.2 — Internal Communication

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 2.2.1 | Verify that security policies are accessible to all employees (e.g., intranet, policy management platform). | Policy repository, access log | |
| 2.2.2 | Inspect evidence that security policy updates are communicated to affected staff. | Policy change notifications, distribution logs | |

### CC2.3 — External Communication

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 2.3.1 | Obtain and review the breach notification policy. Verify it defines notification timelines consistent with applicable regulations (GDPR 72-hour, state breach laws). | Breach notification policy, regulatory mapping | |
| 2.3.2 | Inspect the privacy notice / terms of service. Confirm they accurately describe data handling practices. | Privacy notice, website screenshot | |
| 2.3.3 | Verify that the organization has a responsible disclosure / vulnerability disclosure program. | VDP policy, public disclosure page | |

---

## CC3 — Risk Assessment

### CC3.1 — Risk Assessment Process

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 3.1.1 | Obtain the most recent enterprise risk assessment or cybersecurity risk assessment. Verify it was completed within 12 months of audit period end. | Risk assessment report, date stamp | |
| 3.1.2 | Confirm that the risk assessment methodology is documented (likelihood × impact, risk scoring). | Risk methodology document | |
| 3.1.3 | Verify that in-scope systems and third parties are included in the risk assessment scope. | Risk register, scoping documentation | |

### CC3.2 — Fraud Risk Assessment

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 3.2.1 | Confirm that the risk assessment addresses insider threat and technology-facilitated fraud. | Risk assessment, fraud risk section | |
| 3.2.2 | Verify that controls addressing fraud risks are mapped to identified risks. | Risk-to-control mapping | |

### CC3.3 — Change Management Risk

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 3.3.1 | Confirm that the change management process includes a risk assessment step for significant changes. | Change management policy, CAB procedures | |

### CC3.4 — Risk Response

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 3.4.1 | Inspect the risk register. Verify each identified risk has an assigned owner, response strategy (accept/mitigate/transfer/avoid), and target remediation date. | Risk register | |
| 3.4.2 | Select a sample of 10 risks from the register. Trace to evidence that remediation actions were completed or are being tracked. | Risk register, project tracking system | |

---

## CC4 — Monitoring Activities

### CC4.1 — Ongoing Monitoring

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 4.1.1 | Inspect the security monitoring program. Verify it includes SIEM, IDS/IPS, and endpoint detection capabilities. | SIEM configuration, monitoring policy | |
| 4.1.2 | Review alerts and incidents during audit period. Confirm monitoring is continuous and alerts are triaged. | SIEM alert logs, incident tickets | |
| 4.1.3 | Verify that security metrics are reviewed by management on a regular basis (monthly/quarterly). | Management meeting minutes, KPI dashboards | |

### CC4.2 — Internal Audit Function

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 4.2.1 | Confirm that the internal audit function (or equivalent) reviews security controls at least annually. | Internal audit plan, prior audit reports | |
| 4.2.2 | Inspect prior year audit findings and management responses. Verify remediation was tracked and completed. | Finding tracker, remediation evidence | |

---

## CC5 — Control Activities

### CC5.1 — Control Selection and Development

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 5.1.1 | Confirm that controls are mapped to identified risks and TSC criteria. | Control-to-risk mapping | |
| 5.1.2 | Verify that compensating controls are documented where primary controls have gaps. | Control inventory, compensating control documentation | |

### CC5.2 — Technology General Controls

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 5.2.1 | Inspect the IT general controls framework. Confirm logical access, change management, and operations controls are all addressed. | IT control framework documentation | |
| 5.2.2 | Verify that automated controls are validated through application testing or vendor attestation. | UAT reports, vendor SOC reports | |

### CC5.3 — Policies and Procedures

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 5.3.1 | Inventory all security policies. Verify each has a defined owner, review cycle, and was reviewed within the past 12–24 months. | Policy inventory, version/date log | |
| 5.3.2 | Confirm that procedures exist for all key security processes (access management, incident response, change management, backup, BCP). | Procedure documents, process inventory | |

---

## CC6 — Logical and Physical Access Controls

### CC6.1 — Logical Access Security Measures

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 6.1.1 | Inspect the identity and access management (IAM) platform configuration. Confirm MFA is enforced for all user accounts accessing in-scope systems. | IAM platform screenshots, MFA policy | |
| 6.1.2 | Verify that privileged accounts are managed separately (PAM solution or equivalent) and require additional authentication. | PAM tool configuration, privileged account list | |
| 6.1.3 | Obtain a current list of all active user accounts for in-scope systems. Cross-reference against HR active employee roster. Identify any orphaned accounts. | User account exports, HR roster | |
| 6.1.4 | Select a sample of 25 user provisioning requests during the audit period. Verify each was properly authorized and implemented with least privilege. | Provisioning tickets, access approval records | |
| 6.1.5 | Inspect the password policy configuration. Verify complexity, length, and rotation requirements meet policy. | Password policy configuration, AD/Okta settings | |

### CC6.2 — Prior to Issuing System Credentials

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 6.2.1 | Confirm that new user identity verification is performed before account creation (background checks, manager verification). | Onboarding process documentation, HR records | |
| 6.2.2 | Verify that temporary/default credentials are changed before system access is granted. | System configuration, provisioning process documentation | |

### CC6.3 — Removal or Modification of Access

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 6.3.1 | Obtain HR termination records for the audit period. Select a sample of 25 terminated employees. Verify accounts were disabled within 24 hours of termination. | HR termination log, IT deprovisioning tickets | |
| 6.3.2 | For the same sample, verify that remote access tokens, VPN certificates, and SSO sessions were revoked. | VPN/SSO logs, MDM deprovisioning records | |
| 6.3.3 | Confirm that role changes trigger access reviews. Select 10 internal transfers. Verify old access was removed and new access was approved. | HRIS transfer log, access change tickets | |

### CC6.4 — Physical Access Restrictions

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 6.4.1 | Inspect physical access control logs for in-scope data centers / server rooms during audit period. Confirm only authorized personnel have access. | Badge access logs, physical access list | |
| 6.4.2 | Verify that physical access is reviewed quarterly. Inspect Q1–Q4 review records. | Physical access review reports | |
| 6.4.3 | Confirm that visitor access is logged and escorted. Inspect visitor logs for the audit period. | Visitor log, visitor policy | |

### CC6.5 — Access Discontinuation

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 6.5.1 | Confirm that quarterly logical access reviews were performed for all in-scope systems. Inspect review reports for each quarter. | Access review reports (Q1–Q4) | |
| 6.5.2 | For a sample of access review exceptions identified during reviews, verify that inappropriate access was removed within the policy-defined SLA. | Access review exception log, remediation evidence | |

### CC6.6 — Logical Access Controls — Network and Infrastructure

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 6.6.1 | Obtain and inspect network segmentation diagrams. Verify production, development, and corporate networks are segmented. | Network architecture diagram, firewall rule documentation | |
| 6.6.2 | Review firewall rules for production systems. Verify no overly permissive rules exist (e.g., ANY/ANY). Confirm rules are reviewed at least annually. | Firewall rule exports, firewall review evidence | |
| 6.6.3 | Confirm that remote access (VPN, remote desktop) requires MFA and is limited to authorized users. | VPN configuration, active VPN user list | |

### CC6.7 — Transmission of Data

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 6.7.1 | Verify that all data in transit is encrypted using TLS 1.2 or higher. Inspect SSL/TLS configurations for external-facing services. | SSL/TLS scan results, configuration documentation | |
| 6.7.2 | Confirm that internal service-to-service communication involving sensitive data uses encryption. | Architecture documentation, network configuration | |
| 6.7.3 | Verify that email transmission of sensitive data uses encryption (TLS enforcement, secure email gateway). | Email gateway configuration | |

### CC6.8 — Malware and Ransomware Prevention

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 6.8.1 | Verify endpoint protection (EDR/AV) is deployed on 100% of in-scope endpoints and servers. Inspect coverage reports. | EDR console coverage report | |
| 6.8.2 | Confirm that EDR signature/intelligence updates are current (within 24 hours). | EDR update configuration, last-updated timestamps | |
| 6.8.3 | Verify that execution controls (application allowlisting or equivalent) are implemented on servers. | EDR policy configuration | |

---

## CC7 — System Operations

### CC7.1 — Detection of Configuration Deviations

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 7.1.1 | Confirm that a baseline configuration is defined and documented for all server classes and endpoint types. | Hardening baseline documentation, CIS Benchmark mapping | |
| 7.1.2 | Verify that configuration compliance scanning (CIS/STIG) is performed at least monthly. Inspect scan results. | Configuration compliance scan reports | |
| 7.1.3 | Confirm that configuration deviations are tracked and remediated within defined SLAs. | Deviation tracking, remediation tickets | |

### CC7.2 — Monitoring for Anomalous Activity

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 7.2.1 | Inspect SIEM use cases / detection rules. Confirm coverage of key threat scenarios (authentication anomalies, privilege escalation, data exfiltration). | SIEM rule inventory, use case documentation | |
| 7.2.2 | Review SIEM alert log for the audit period. Confirm alerts are triaged within defined SLAs (e.g., critical: 1 hour, high: 4 hours). | SIEM alert log, ticket creation timestamps | |
| 7.2.3 | Verify that log retention meets policy (minimum 12 months, 90 days hot). | Log retention configuration, storage reports | |

### CC7.3 — Evaluation and Communication of Security Incidents

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 7.3.1 | Obtain and inspect the incident response policy and procedures. Confirm IRP is current and tested. | IRP document, version date | |
| 7.3.2 | Select a sample of 10 security incidents from the audit period. Verify each was triaged, investigated, contained, and closed per IRP. | Incident tickets, post-incident reports | |
| 7.3.3 | Confirm that a post-mortem / lessons learned process exists. Inspect evidence from 2–3 significant incidents. | Post-incident review reports | |
| 7.3.4 | Verify that security incidents triggering regulatory notification obligations are escalated appropriately. | Notification decisions, regulatory submissions (if applicable) | |

### CC7.4 — Incident Response

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 7.4.1 | Confirm that tabletop exercises or IR drills were conducted at least annually. Inspect exercise documentation. | Tabletop exercise reports, attendance records | |
| 7.4.2 | Verify that incident response retainer or external IR support is contracted and available. | IR retainer contract | |

### CC7.5 — Identification and Remediation of Identified Vulnerabilities

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 7.5.1 | Inspect the vulnerability management policy. Confirm SLAs are defined by severity (Critical: 15 days, High: 30 days, Medium: 90 days). | Vulnerability management policy | |
| 7.5.2 | Obtain authenticated vulnerability scan results for in-scope infrastructure during the audit period. | Vulnerability scan reports (Tenable/Qualys/etc.) | |
| 7.5.3 | Select a sample of 25 critical/high vulnerabilities identified during the audit period. Verify each was remediated within policy SLA. | Vuln tracking records, patching evidence | |
| 7.5.4 | Confirm that penetration testing was performed on in-scope systems within the prior 12 months. Review findings and remediation status. | Penetration test report, finding remediation evidence | |

---

## CC8 — Change Management

### CC8.1 — Changes to Infrastructure and Software

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 8.1.1 | Obtain and review the change management policy. Confirm it defines change types (standard, normal, emergency) and required approval levels. | Change management policy | |
| 8.1.2 | Select a sample of 25 changes deployed to production during the audit period. Verify each was properly authorized (CAB/approver) before deployment. | Change tickets, CAB meeting minutes | |
| 8.1.3 | For the same sample, verify that changes were tested in a non-production environment prior to production deployment. | Test records, UAT sign-off | |
| 8.1.4 | Verify that code review / peer review is required for all code changes. Inspect repository pull request records. | GitHub/GitLab PR records, branch protection settings | |
| 8.1.5 | Confirm that developers do not have direct write access to production environments. | Production access list, RBAC configuration | |
| 8.1.6 | Select a sample of 5 emergency changes. Verify retroactive approval and post-implementation review occurred within 48 hours. | Emergency change tickets, retroactive approvals | |

---

## CC9 — Risk Mitigation

### CC9.1 — Identification and Mitigation of Risks from Business Disruption

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 9.1.1 | Obtain and inspect the Business Continuity Plan (BCP) and Disaster Recovery Plan (DRP). Confirm both are current (reviewed within 12 months). | BCP, DRP documents | |
| 9.1.2 | Confirm that Recovery Time Objectives (RTOs) and Recovery Point Objectives (RPOs) are defined for critical systems. | BIA, RTO/RPO documentation | |
| 9.1.3 | Inspect evidence that BCP/DR tests were conducted during the audit period. Verify RTOs/RPOs were achieved or gaps were documented. | DR test reports, BCP exercise documentation | |

### CC9.2 — Third-Party Risk Management

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| 9.2.1 | Obtain the vendor inventory. Confirm all third parties processing, storing, or transmitting sensitive data are identified and risk-rated. | Vendor inventory, risk tiering documentation | |
| 9.2.2 | For a sample of 10 critical vendors: verify a current security assessment (SOC 2, ISO 27001 cert, or questionnaire) is on file and was reviewed within 12 months. | Vendor assessment files, review evidence | |
| 9.2.3 | Confirm that vendor contracts include data processing agreements (DPAs), security requirements, and right-to-audit clauses. | Sample vendor contracts | |
| 9.2.4 | Verify that vendor access to in-scope systems is tracked, approved, and reviewed. | Vendor access list, approval records | |

---

## Availability Criteria (A Series) — If In-Scope

### A1.1 — Availability Commitments

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| A.1.1 | Inspect system availability commitments in SLAs / customer agreements. Confirm uptime commitments are defined. | SLAs, customer agreements | |
| A.1.2 | Obtain uptime monitoring reports for in-scope systems for the audit period. Verify commitments were met or deviations were communicated. | Uptime monitoring reports (Datadog/PagerDuty/etc.) | |

### A1.2 — Environmental Protections

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| A.2.1 | For cloud-hosted systems: verify redundancy architecture (multi-AZ or multi-region) is implemented and tested. | Architecture documentation, availability test records | |
| A.2.2 | Inspect backup configurations. Verify backups are taken per policy, stored off-site/cloud, and restoration has been tested. | Backup configuration, restore test records | |

---

## Confidentiality Criteria (C Series) — If In-Scope

### C1.1 — Identification of Confidential Information

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| C.1.1 | Inspect the data classification policy. Verify confidential data is defined and classification criteria are clear. | Data classification policy | |
| C.1.2 | Confirm that a data inventory / data map exists identifying where confidential data is stored, processed, and transmitted. | Data inventory, data flow diagrams | |

### C1.2 — Disposal of Confidential Information

| # | Audit Procedure | Evidence Required | Ref |
|---|----------------|-------------------|-----|
| C.2.1 | Inspect the data retention and disposal policy. Verify retention schedules are defined per data type. | Retention policy | |
| C.2.2 | Select 5 examples of data disposal during the audit period (media destruction, cloud data deletion). Verify certificates of destruction or equivalent evidence. | Disposal certificates, deletion records | |

---

## Workpaper Index

| WP # | Section | Control | Status | Prepared By | Review Date |
|------|---------|---------|--------|-------------|-------------|
| WP-01 | CC1.1 | Code of Conduct acknowledgment | | | |
| WP-02 | CC6.1 | MFA enforcement | | | |
| WP-03 | CC6.1 | User provisioning sample | | | |
| WP-04 | CC6.3 | Termination access revocation | | | |
| WP-05 | CC6.5 | Quarterly access reviews | | | |
| WP-06 | CC7.5 | Vulnerability remediation SLA | | | |
| WP-07 | CC8.1 | Change management sample | | | |
| WP-08 | CC9.2 | Third-party risk assessments | | | |

---

*Audit Program Version: 1.0 | Framework Alignment: AICPA TSC 2017*
