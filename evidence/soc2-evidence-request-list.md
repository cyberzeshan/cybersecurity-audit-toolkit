# SOC 2 Type II — Evidence Request List

**Organization:** [ORGANIZATION NAME]
**Audit Period:** [START DATE] – [END DATE]
**Prepared By:** [AUDITOR NAME / FIRM]
**Date Issued:** [DATE]
**Response Due:** [DATE — typically 2–3 weeks before fieldwork]
**Primary Contact:** [CLIENT CONTACT NAME, TITLE, EMAIL]

---

## Instructions for the Client

Please provide all requested items in electronic format. Where screenshots are required, capture the full screen including system name, date/time, and the specific configuration or setting referenced.

For exports and reports, include a header row identifying each column, and note the date the export was generated. Do not modify exported data.

Organize responses by Evidence Request Number (ER-##). Upload to [SharePoint / shared drive / audit portal] no later than [DATE].

Questions? Contact [AUDITOR NAME] at [EMAIL].

---

## Category 1: Organization and Governance (CC1)

| ER # | Item Requested | Time Period / Scope | Format | Priority |
|------|---------------|--------------------|---------| ---------|
| ER-01 | Current organizational chart showing the security / IT / engineering structure | As of audit period end date | PDF / image | High |
| ER-02 | Information Security Policy — current version | Current, with version number and approval date | PDF | High |
| ER-03 | Code of Conduct / Acceptable Use Policy — current version | Current | PDF | High |
| ER-04 | Employee Code of Conduct acknowledgment log — confirming all employees acknowledged within 30 days of hire and annually | Audit period | Export / report | High |
| ER-05 | Board or Audit Committee meeting minutes showing cybersecurity oversight discussion | Audit period | PDF (redact sensitive business items) | Medium |
| ER-06 | Security awareness training completion report showing % of employees trained | Audit period | Report / export | High |
| ER-07 | Security awareness training content / curriculum summary | Most recent version | PDF / screenshot | Medium |

---

## Category 2: Communications and Information (CC2)

| ER # | Item Requested | Time Period / Scope | Format | Priority |
|------|---------------|--------------------|---------| ---------|
| ER-08 | Asset inventory / CMDB listing all production systems in scope | As of audit period end date | Export (CSV / Excel) | High |
| ER-09 | Data flow diagrams or system architecture diagrams for in-scope systems | Current | PDF / diagram | High |
| ER-10 | Privacy notice / customer-facing privacy policy | Current | PDF / web URL | Medium |
| ER-11 | List of all active security policies and procedures with names, version numbers, owners, and last review dates | Current | Excel / table | High |

---

## Category 3: Risk Assessment (CC3)

| ER # | Item Requested | Time Period / Scope | Format | Priority |
|------|---------------|--------------------|---------| ---------|
| ER-12 | Most recent cybersecurity or enterprise risk assessment report | Completed within audit period or prior 12 months | PDF | High |
| ER-13 | Risk register with current open risks, owners, and remediation status | Current | Excel / export | High |
| ER-14 | Risk assessment methodology document | Current | PDF | Medium |

---

## Category 4: Monitoring Activities (CC4)

| ER # | Item Requested | Time Period / Scope | Format | Priority |
|------|---------------|--------------------|---------| ---------|
| ER-15 | Internal audit plan and schedule for the audit period | Audit period | PDF | Medium |
| ER-16 | Internal audit reports issued during the audit period (or prior 12 months) | Audit period | PDF | High |
| ER-17 | Finding remediation tracker / management action plan status | Current | Excel / report | High |

---

## Category 5: Control Activities (CC5)

| ER # | Item Requested | Time Period / Scope | Format | Priority |
|------|---------------|--------------------|---------| ---------|
| ER-18 | Full list of all security policies and procedures (name, version, owner, review date, next review date) | Current | Excel | High |
| ER-19 | Evidence that all policies were reviewed within the past 24 months (review meeting minutes, email approvals, or version logs) | Audit period | Records | Medium |

---

## Category 6: Logical Access (CC6)

| ER # | Item Requested | Time Period / Scope | Format | Priority |
|------|---------------|--------------------|---------| ---------|
| ER-20 | Full export of all active user accounts in in-scope systems (name, username, role, date created, last login, MFA status) | As of audit period end date | CSV / Excel | High |
| ER-21 | MFA enrollment and enforcement configuration showing MFA is required for all users | As of audit period end date | Screenshots | High |
| ER-22 | Password policy configuration for all identity systems (AD, Okta, or equivalent) | As of audit period end date | Screenshots | High |
| ER-23 | All access provisioning requests and approvals during the audit period (full population) | Full audit period | ITSM export | High |
| ER-24 | List of all privileged / administrative accounts across in-scope systems | As of audit period end date | Export | High |
| ER-25 | Privileged Access Management (PAM) tool configuration — session recording, credential vaulting, MFA enforcement settings | Current | Screenshots | High |
| ER-26 | HR active employee roster as of audit period end date (name, department, role, hire date) | As of audit period end date | Export | High |
| ER-27 | HR termination list for the audit period (name, termination date, role) | Full audit period | Export | High |
| ER-28 | IT deprovisioning tickets corresponding to employee terminations during the audit period | Full audit period | ITSM export | High |
| ER-29 | Quarterly access review reports for all in-scope systems (Q1–Q4 of audit period) | Q1–Q4 of audit period | Reports / documents | High |
| ER-30 | Evidence that exceptions identified in access reviews were remediated (tickets, before/after access screenshots) | Audit period | Per exception | High |
| ER-31 | Network segmentation diagram showing production, development, and corporate network separation | Current | PDF / diagram | High |
| ER-32 | Firewall rule export for production environment firewalls | As of audit period end date | Export / screenshot | High |
| ER-33 | Evidence of annual firewall rule review (approval, reviewer name, date) | Audit period | Records | Medium |
| ER-34 | SSL/TLS certificate scan results or configuration showing TLS 1.2+ enforcement on external-facing services | Most recent scan within audit period | Report | High |
| ER-35 | Endpoint protection (EDR / AV) coverage report showing all endpoints covered | As of audit period end date | Report | High |
| ER-36 | Physical access control log for data center / server room | Full audit period | Export | Medium |
| ER-37 | Physical access review records for server room / data center (showing who was on the access list and review evidence) | Quarterly reviews in audit period | Records | Medium |

---

## Category 7: System Operations (CC7)

| ER # | Item Requested | Time Period / Scope | Format | Priority |
|------|---------------|--------------------|---------| ---------|
| ER-38 | Server hardening baseline documentation (CIS benchmark or equivalent) | Current | PDF | Medium |
| ER-39 | Configuration compliance scan results showing deviation from baseline | Most recent scan within audit period | Report | High |
| ER-40 | SIEM use case / detection rule inventory | Current | PDF / export | Medium |
| ER-41 | Sample of SIEM alerts from audit period and evidence of triage/response (select 3 months) | Sample period within audit period | SIEM export / ticket records | High |
| ER-42 | Log retention configuration showing 12-month retention | Current | Screenshots | Medium |
| ER-43 | Incident Response Policy and Procedures | Current | PDF | High |
| ER-44 | Security incident log for the audit period | Full audit period | Export | High |
| ER-45 | Post-incident review reports for all significant security incidents | Audit period | PDF | High |
| ER-46 | Tabletop exercise or IR drill documentation (agenda, participants, findings, actions) | Most recent (within audit period or prior 12 months) | PDF | Medium |
| ER-47 | Vulnerability management policy | Current | PDF | High |
| ER-48 | Authenticated vulnerability scan reports for in-scope infrastructure | Full audit period (all scan runs) | Reports | High |
| ER-49 | Vulnerability remediation tracker — current open vulnerabilities by severity and age | Current | Export | High |
| ER-50 | Evidence of remediation for sample critical/high vulnerabilities (patch deployment records, rescan results) | Audit period | Per vulnerability | High |
| ER-51 | Most recent penetration test report (internal and external) | Within prior 12 months | PDF | High |
| ER-52 | Penetration test finding remediation tracker with status | Current | Excel / report | High |

---

## Category 8: Change Management (CC8)

| ER # | Item Requested | Time Period / Scope | Format | Priority |
|------|---------------|--------------------|---------| ---------|
| ER-53 | Change management policy and procedures | Current | PDF | High |
| ER-54 | Full population of change requests (all change types) deployed to production during audit period | Full audit period | ITSM export | High |
| ER-55 | CAB (Change Advisory Board) meeting minutes or approval records for normal changes | Audit period | Records | High |
| ER-56 | Test/UAT sign-off records for changes in sample | Per sample item | Records | High |
| ER-57 | Evidence that developers do not have direct write access to production (RBAC configuration / repository branch protection settings) | Current | Screenshots | High |
| ER-58 | Emergency change records with retroactive approvals | Audit period | ITSM export | Medium |

---

## Category 9: Risk Mitigation (CC9)

| ER # | Item Requested | Time Period / Scope | Format | Priority |
|------|---------------|--------------------|---------| ---------|
| ER-59 | Business Continuity Plan (BCP) and Disaster Recovery Plan (DRP) | Current, with version and approval date | PDF | High |
| ER-60 | Business Impact Analysis (BIA) with RTO/RPO definitions for critical systems | Most recent | PDF | High |
| ER-61 | BCP/DR test reports for the audit period | Audit period | PDF | High |
| ER-62 | Third-party / vendor inventory with risk tier classification | Current | Export | High |
| ER-63 | Security assessments for all Tier 1 (critical) vendors — SOC 2 reports, ISO 27001 certs, or completed questionnaires | Within prior 12 months | Per vendor | High |
| ER-64 | Sample of 5 vendor contracts for Tier 1 vendors — including data processing agreements | Current | PDF | High |

---

## Category 10: Additional Criteria (If In Scope)

### Availability (A)

| ER # | Item Requested | Time Period / Scope | Format | Priority |
|------|---------------|--------------------|---------| ---------|
| ER-65 | Uptime / availability monitoring reports for in-scope services | Full audit period | Monthly reports | High |
| ER-66 | SLA documentation showing uptime commitments | Current | PDF / contracts | Medium |
| ER-67 | Backup configuration and most recent backup restore test results | Within prior 6 months | Configuration screenshots, test records | High |

### Confidentiality (C)

| ER # | Item Requested | Time Period / Scope | Format | Priority |
|------|---------------|--------------------|---------| ---------|
| ER-68 | Data classification policy | Current | PDF | High |
| ER-69 | Data inventory / data map showing where confidential data is stored and processed | Current | PDF / diagram | High |
| ER-70 | Data retention and disposal policy | Current | PDF | Medium |
| ER-71 | Sample of data disposal records (media destruction certificates, cloud data deletion evidence) | Audit period | Per sample | Medium |

---

## Evidence Tracking Log

> Use this table to track receipt and review of all requested items.

| ER # | Item | Received? | Date Received | Received From | Reviewed By | Adequate? | Notes |
|------|------|-----------|---------------|---------------|-------------|-----------|-------|
| ER-01 | Org chart | ☐ | | | | ☐ | |
| ER-02 | IS Policy | ☐ | | | | ☐ | |
| ER-03 | AUP | ☐ | | | | ☐ | |
| ... | | | | | | | |

---

*SOC 2 Evidence Request List Version: 1.0*
*Framework: AICPA Trust Services Criteria 2017 (as updated)*
