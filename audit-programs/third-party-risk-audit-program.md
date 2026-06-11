# Third-Party Risk Management (TPRM) Audit Program

**Domain:** Vendor / Third-Party Risk Management
**Framework Alignment:** SOC 2 CC9.2, ISO 27001 A.5.19–A.5.23, NIST SP 800-53 SA-9, PCI-DSS v4 Req 12.8
**Audit Period:** [START DATE] – [END DATE]
**Auditor:** [NAME]
**Organization:** [ORGANIZATION NAME]

---

## Audit Objectives

1. Verify that a complete and current vendor inventory exists with risk tiering applied
2. Confirm that security assessments are performed on vendors commensurate with their risk tier
3. Assess whether vendor contracts include adequate information security requirements
4. Verify that ongoing monitoring of critical vendors is occurring
5. Evaluate the organization's response capability when a vendor security incident occurs

---

## Pre-Audit Evidence Requests

| # | Item | Source | Format | Due Date |
|---|------|--------|--------|----------|
| 1 | Complete vendor/third-party inventory with risk tier classification | TPRM platform / spreadsheet | Export | |
| 2 | TPRM policy and vendor management procedures | Policy repository | PDF | |
| 3 | Risk tiering methodology document | TPRM team | PDF | |
| 4 | Security assessments / questionnaire responses for sample vendors | TPRM file system | Per vendor | |
| 5 | SOC 2 reports / ISO 27001 certs / security certifications for critical vendors | TPRM file system | Per vendor | |
| 6 | Sample vendor contracts and data processing agreements (DPAs) | Legal / procurement | Per vendor | |
| 7 | Vendor onboarding approval records for new vendors in audit period | Procurement / TPRM | Export | |
| 8 | List of vendors with access to in-scope systems or sensitive data | IAM / TPRM | Export | |
| 9 | Vendor security incident log for audit period | TPRM / Security | Export | |
| 10 | Fourth-party (sub-processor) inventory for critical vendors | TPRM | Export | |

---

## Section 1: TPRM Program Governance

| # | Audit Procedure | Objective | Evidence Required | Finding |
|---|----------------|-----------|-------------------|---------|
| 1.1 | Obtain the TPRM policy. Verify it is current (reviewed ≤ 24 months), approved by management, and defines program scope. | Policy governance | TPRM policy | |
| 1.2 | Confirm the policy addresses: risk tiering criteria, assessment requirements by tier, contract requirements, ongoing monitoring, and incident notification. | Policy completeness | TPRM policy | |
| 1.3 | Verify that a TPRM program owner is designated with defined responsibilities. | Ownership | RACI, job description | |
| 1.4 | Confirm that the TPRM program is integrated with procurement: no new vendor contracts may be executed without security review approval. | Procurement integration | Procurement policy, approval gate evidence | |
| 1.5 | Verify that the TPRM program encompasses all vendors that (a) store, process, or transmit sensitive/personal data, (b) have access to in-scope systems, or (c) provide critical services. | Program scope | Program scope documentation, vendor inventory | |

---

## Section 2: Vendor Inventory and Risk Tiering

| # | Audit Procedure | Objective | Evidence Required | Finding |
|---|----------------|-----------|-------------------|---------|
| 2.1 | Obtain the full vendor inventory. Verify it is current — all vendors added in the audit period are included. | Inventory completeness | Vendor inventory, new vendor onboarding records | |
| 2.2 | Verify that each vendor is risk-tiered. Confirm tiering criteria are documented (e.g., Tier 1 = access to sensitive data / critical services; Tier 2 = moderate data access; Tier 3 = no data access). | Risk tiering | Tiering methodology, vendor inventory with tiers | |
| 2.3 | Test a sample of 10 vendors across all tiers. Evaluate whether the assigned tier is consistent with the tiering criteria. Document any misclassifications. | Tier accuracy | Vendor profiles, tiering criteria | |
| 2.4 | Verify that all vendors with access to personal data (subject to GDPR, CCPA, HIPAA, etc.) are identified in the inventory. | Regulatory coverage | Vendor inventory, data processing register | |
| 2.5 | Confirm that the vendor inventory is reviewed and updated at least annually (or upon significant change). | Inventory currency | Last review date, review records | |

---

## Section 3: Vendor Security Assessments

| # | Audit Procedure | Objective | Evidence Required | Finding |
|---|----------------|-----------|-------------------|---------|
| 3.1 | Obtain the list of Tier 1 (critical) vendors. Verify the count is reasonable and all material vendors with sensitive data access are Tier 1. | Critical vendor identification | Vendor inventory, Tier 1 list | |
| 3.2 | For Tier 1 vendors: verify a current security assessment is on file (completed within 12 months of audit period end). Assessment methods: SOC 2 Type II review, ISO 27001 cert review, or completed security questionnaire (CAIQ, SIG, or equivalent). | Tier 1 assessment currency | Assessment files, dates | |
| 3.3 | Select a sample of 10 Tier 1 vendors. For each: (a) confirm assessment is on file, (b) verify assessor reviewed and documented findings, (c) confirm risks identified in assessment have treatment plans. | Tier 1 assessment quality | Sample assessment files, review evidence | |
| 3.4 | For Tier 2 vendors: verify assessments are performed at least every 24 months (or upon contract renewal). | Tier 2 assessment cadence | Assessment dates, contract renewal records | |
| 3.5 | Confirm that SOC 2 reports accepted from vendors are reviewed for: report period coverage, scope alignment, qualified opinions, and exceptions noted. | SOC 2 review quality | SOC 2 review checklists, reviewer notes | |
| 3.6 | Verify that any control gaps or findings from vendor assessments are tracked and remediation plans are obtained from the vendor. | Finding tracking | Assessment finding tracker, vendor remediation plans | |
| 3.7 | Confirm that new vendors undergo security assessment before contract execution and go-live. | Pre-onboarding assessment | New vendor onboarding records, assessment dates vs contract dates | |

---

## Section 4: Contract Security Requirements

| # | Audit Procedure | Objective | Evidence Required | Finding |
|---|----------------|-----------|-------------------|---------|
| 4.1 | Obtain a sample of 10 vendor contracts (prioritize Tier 1). Verify each contract includes mandatory security clauses. | Contract completeness | Sample contracts | |
| 4.2 | For each sampled contract, verify the following security provisions are present: | Clause-by-clause review | | |
| | (a) Data protection and confidentiality obligations | | Contract clauses | |
| | (b) Data Processing Agreement (DPA) or equivalent (required for personal data processors) | | DPA / GDPR processor agreement | |
| | (c) Security incident notification requirement (≤ 72 hours for personal data breaches) | | Incident notification clause | |
| | (d) Right to audit or equivalent (SOC 2 requirement, pen test results, or questionnaire) | | Right-to-audit clause | |
| | (e) Minimum information security requirements (encryption, access controls, vulnerability management) | | Security requirements annex | |
| | (f) Sub-processor / sub-contractor restrictions and notification requirements | | Sub-processor clause | |
| | (g) Data return / destruction upon contract termination | | Data disposal clause | |
| 4.3 | Identify any contracts missing critical security provisions. Document as findings with risk level. | Gap identification | Contract review results | |
| 4.4 | Confirm that legacy contracts (pre-policy) have a remediation plan to add security provisions at next renewal. | Contract remediation | Contract renewal schedule, gap register | |

---

## Section 5: Ongoing Vendor Monitoring

| # | Audit Procedure | Objective | Evidence Required | Finding |
|---|----------------|-----------|-------------------|---------|
| 5.1 | Verify that continuous monitoring exists for Tier 1 vendors. This may include: threat intelligence feeds, cybersecurity ratings (SecurityScorecard, BitSight), or regular check-ins. | Continuous monitoring | Monitoring platform reports, rating history | |
| 5.2 | Confirm that changes in a vendor's security posture (significant rating drops, public breach disclosures) trigger a re-assessment. | Event-driven reassessment | Re-assessment trigger procedure, re-assessment records | |
| 5.3 | Verify that annual re-assessments are scheduled and tracked for all Tier 1 vendors. Inspect reassessment completion for the audit period. | Annual re-assessment | Re-assessment schedule, completion records | |
| 5.4 | Confirm that vendor-provided SOC 2 reports are reviewed each cycle (typically annually). Inspect evidence that bridge letters are obtained when SOC 2 report coverage has a gap. | SOC 2 continuity | Report review records, bridge letters | |
| 5.5 | Verify that vendor access to in-scope systems is inventoried and reviewed. Confirm access is revoked or reduced when vendor relationship ends or changes. | Vendor access management | Vendor access list, access review records | |
| 5.6 | Inspect vendor performance reviews or QBRs (quarterly business reviews). Confirm security topics are included in vendor governance meetings. | Governance integration | QBR agendas/minutes, security agenda items | |

---

## Section 6: Fourth-Party Risk (Sub-Processors)

| # | Audit Procedure | Objective | Evidence Required | Finding |
|---|----------------|-----------|-------------------|---------|
| 6.1 | For Tier 1 vendors: verify a sub-processor list is obtained and reviewed. Confirm material sub-processors (e.g., cloud hosting providers, backup vendors) are identified. | Fourth-party identification | Sub-processor inventory from vendors | |
| 6.2 | Confirm that contracts require vendors to notify the organization before adding new sub-processors for services involving sensitive data. | Sub-processor notification | Contract sub-processor clauses | |
| 6.3 | Verify that material concentration risk from shared sub-processors is identified (e.g., multiple critical vendors using the same cloud provider). | Concentration risk | Sub-processor analysis | |

---

## Section 7: Vendor Incident Response

| # | Audit Procedure | Objective | Evidence Required | Finding |
|---|----------------|-----------|-------------------|---------|
| 7.1 | Verify that the incident response plan (IRP) includes a procedure for responding to vendor security incidents. | Vendor IR integration | IRP, vendor incident section | |
| 7.2 | Inspect the vendor incident log for the audit period. For any vendor security incidents: verify the organization was notified per contractual SLA and a response was executed. | Vendor incident response | Vendor incident log, notification records | |
| 7.3 | Confirm that the business impact of vendor incidents was assessed and escalated appropriately. | Impact assessment | Incident records, escalation evidence | |
| 7.4 | Verify that vendor incidents are included in the organization's post-incident review process. | Lessons learned | Post-incident review records | |

---

## Vendor Assessment Sample Results

| # | Vendor | Tier | Assessment Type | Assessment Date | Expiry | Gaps Found | Risk Treatment | Status |
|---|--------|------|----------------|----------------|--------|------------|---------------|--------|
| 1 | | | | | | | | |
| 2 | | | | | | | | |
| 3 | | | | | | | | |

---

## Audit Conclusions

**Overall TPRM Assessment:**

| Area | Effective | Partially Effective | Not Effective |
|------|-----------|--------------------|--------------| 
| Program Governance | | | |
| Vendor Inventory & Tiering | | | |
| Security Assessments | | | |
| Contract Requirements | | | |
| Ongoing Monitoring | | | |
| Fourth-Party Risk | | | |
| Vendor Incident Response | | | |

**Key Findings:**
1.
2.
3.

---

*Audit Program Version: 1.0 | Aligned to: SOC 2 CC9.2, ISO 27001 A.5.19–A.5.23, NIST SP 800-53 SA-9*
