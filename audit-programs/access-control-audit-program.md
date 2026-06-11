# Logical Access Control Audit Program

**Domain:** Identity & Access Management (IAM)
**Framework Alignment:** SOC 2 CC6, ISO 27001 A.5.15–A.5.18 / A.8.2–A.8.5, NIST SP 800-53 AC, PCI-DSS v4 Req 7–8
**Audit Period:** [START DATE] – [END DATE]
**Auditor:** [NAME]
**Organization:** [ORGANIZATION NAME]
**Systems in Scope:** [List all in-scope systems / identity providers]

---

## Audit Objectives

1. Verify that user access is provisioned, modified, and revoked through a formal, authorized process
2. Confirm that the principle of least privilege is consistently applied
3. Assess the effectiveness of privileged access controls
4. Verify that periodic access reviews are performed and result in action
5. Identify segregation of duties conflicts and orphaned / dormant accounts

---

## Pre-Audit Evidence Requests

Before fieldwork begins, request the following:

| # | Item | Source System | Format | Due Date |
|---|------|---------------|--------|----------|
| 1 | Full export of active user accounts for all in-scope systems | IAM / AD / Okta | CSV/Excel | |
| 2 | List of all privileged / admin accounts with assigned roles | PAM / AD | CSV | |
| 3 | Access provisioning tickets for audit period | ITSM (ServiceNow / Jira) | Export | |
| 4 | HR active employee roster as of audit period end | HRIS | Export | |
| 5 | HR termination list for audit period | HRIS | Export | |
| 6 | HR transfer / role change list for audit period | HRIS | Export | |
| 7 | Q1–Q4 access review reports for all in-scope systems | IAM / SharePoint | PDF/Excel | |
| 8 | Privileged access review reports | PAM / spreadsheet | PDF/Excel | |
| 9 | Access control policy and identity management procedure | Policy repository | PDF | |
| 10 | MFA enrollment and enforcement configuration | IAM / SSO platform | Screenshots | |
| 11 | Password policy configuration for all in-scope systems | AD / Okta / IAM | Screenshots | |

---

## Section 1: Access Control Policy and Governance

| # | Audit Procedure | Objective | Evidence Required | Finding |
|---|----------------|-----------|-------------------|---------|
| 1.1 | Obtain the access control policy. Verify it is current (reviewed within 24 months), approved by management, and distributed to relevant personnel. | Policy governance | Access control policy, version/approval records | |
| 1.2 | Confirm the policy addresses: account provisioning, least privilege, MFA requirements, privileged access, access review frequency, and account termination. | Policy completeness | Policy document | |
| 1.3 | Verify an identity management procedure exists and covers the full user lifecycle (request → approval → provisioning → review → deprovisioning). | Lifecycle governance | Identity management procedure | |
| 1.4 | Confirm that roles and permissions are formally defined (role-based access control model or equivalent job function matrix). | RBAC governance | Role matrix / permission catalog | |
| 1.5 | Verify that a Segregation of Duties (SoD) matrix exists for critical functions (e.g., AP/AR, change management, financial reporting). | SoD governance | SoD matrix, conflicting role documentation | |

---

## Section 2: User Account Provisioning

| # | Audit Procedure | Objective | Evidence Required | Finding |
|---|----------------|-----------|-------------------|---------|
| 2.1 | Define population: all new user accounts provisioned during audit period. Obtain count from ITSM and verify completeness against HR new-hire log. | Population completeness | Provisioning tickets, HR new-hire log | |
| 2.2 | Select a sample of 25 provisioning requests (risk-stratified: include privileged access requests). | Sample selection | Selected ticket list | |
| 2.3 | For each sample item, verify: (a) formal access request submitted, (b) business justification documented, (c) manager or authorized approver approved request, (d) approval timestamp precedes access grant. | Authorization | Request tickets, approval records | |
| 2.4 | For each sample item, verify access granted matches what was requested (no scope creep; no additional permissions added). | Least privilege | Access tickets, IAM provisioning records | |
| 2.5 | For sample items involving role change or transfer: verify old access was removed and new access was appropriate to new role. | Access modification | HRIS transfer records, access change tickets | |
| 2.6 | Verify that no shared / generic accounts were created during the audit period (except documented service accounts with justified use). | Account standards | Account provisioning records, IAM user list | |
| 2.7 | For any exceptions (access granted before approval, scope creep, missing justification): document details in exception log. | Exception tracking | Exception log | |

---

## Section 3: Privileged Access Management

| # | Audit Procedure | Objective | Evidence Required | Finding |
|---|----------------|-----------|-------------------|---------|
| 3.1 | Obtain a current list of all privileged accounts (domain admins, root, local admin, application admin, cloud IAM admin). Verify count is reasonable and documented. | Privilege inventory | Privileged account list | |
| 3.2 | Verify that privileged accounts are managed in a Privileged Access Management (PAM) solution (CyberArk, BeyondTrust, Delinea, or equivalent). If PAM is not implemented, document as a finding. | PAM implementation | PAM tool configuration, account enrollment | |
| 3.3 | Confirm that privileged accounts require MFA at every login. Inspect PAM or IAM MFA enforcement settings. | Privileged MFA | PAM/IAM MFA configuration screenshots | |
| 3.4 | Verify that privileged accounts are distinct from standard user accounts (no dual-purpose admin accounts for daily tasks). | Separation of accounts | Privileged account list cross-referenced against standard user list | |
| 3.5 | Select a sample of 10 privileged accounts. For each, verify: (a) documented business justification, (b) named account owner, (c) formal approval on file, (d) reviewed within the past 6 months. | Privileged account authorization | Account approval records, review records | |
| 3.6 | Inspect PAM session recording and keystroke logging configuration. Verify all privileged sessions are recorded and retained per policy. | Privileged session monitoring | PAM configuration, session log retention settings | |
| 3.7 | Verify that privileged account passwords are rotated per policy (automatically via PAM or manually with evidence). Inspect rotation logs. | Credential rotation | PAM rotation logs, password change records | |
| 3.8 | Confirm that emergency / break-glass accounts exist, are secured, and access is logged and reviewed. | Break-glass controls | Break-glass account documentation, access logs | |
| 3.9 | Verify that just-in-time (JIT) access is implemented for production systems where feasible. | JIT access | PAM JIT configuration, approval workflow | |

---

## Section 4: User Account Deprovisioning

| # | Audit Procedure | Objective | Evidence Required | Finding |
|---|----------------|-----------|-------------------|---------|
| 4.1 | Obtain complete HR termination list for audit period. Define as population. | Population definition | HR termination log | |
| 4.2 | Select a sample of 25 terminated employees (include involuntary terminations and high-risk roles if possible). | Sample selection | Selected termination records | |
| 4.3 | For each sample item, trace to IT deprovisioning ticket. Verify account was disabled within 24 hours (or policy-defined SLA) of HR termination date. | Timely deprovisioning | HR termination date, IT ticket creation/completion date | |
| 4.4 | For each sample item, cross-reference terminated employee against current active account lists in all in-scope systems. Confirm no active accounts remain. | Account removal completeness | Active account exports, HR termination cross-reference | |
| 4.5 | For each sample item, verify revocation of: VPN access, SSO/SAML sessions, remote desktop, physical badge access, and shared credentials. | Access revocation completeness | VPN logs, SSO deprovisioning records, badge access system | |
| 4.6 | For sample items with privileged access: verify privileged accounts were also removed/disabled. | Privileged deprovisioning | PAM deprovisioning records | |
| 4.7 | Perform a completeness test: cross-reference the full HR termination list against IAM active account exports. Flag any accounts not deprovisioned within policy SLA. | Completeness test | Full cross-reference output | |
| 4.8 | Identify any orphaned accounts (accounts with no corresponding active HR record). Report count and details. | Orphaned account detection | IAM vs HR cross-reference | |

---

## Section 5: Periodic Access Reviews

| # | Audit Procedure | Objective | Evidence Required | Finding |
|---|----------------|-----------|-------------------|---------|
| 5.1 | Verify that access reviews were performed for all in-scope systems on the policy-defined schedule (at minimum quarterly for critical systems). | Review schedule compliance | Access review reports Q1–Q4 | |
| 5.2 | Confirm each review was completed by an appropriate reviewer (system owner or manager — not IT who provisioned access). | Reviewer independence | Review reports, reviewer names/titles | |
| 5.3 | Inspect access review reports. Verify that reviewer was presented with current access for each user, not just a list to rubber-stamp. | Review quality | Access review reports, IAM export timestamps | |
| 5.4 | Identify exceptions flagged during reviews (inappropriate access, excess permissions). Verify each exception was remediated within the policy-defined SLA (typically 30 days). | Exception remediation | Review exception log, remediation tickets, before/after access evidence | |
| 5.5 | Confirm that accounts with no recent activity (dormant accounts, typically 90+ days) were flagged and disabled or investigated during reviews. | Dormant account management | Dormant account report, review evidence | |
| 5.6 | Verify that privileged access reviews occur at least every 6 months and are conducted by a different reviewer than the access owner. | Privileged review cadence | Privileged access review reports | |
| 5.7 | For any systems not included in the access reviews: document as a finding with root cause (system not inventoried, no owner, etc.). | Review completeness | System inventory vs review scope comparison | |

---

## Section 6: Authentication Controls

| # | Audit Procedure | Objective | Evidence Required | Finding |
|---|----------------|-----------|-------------------|---------|
| 6.1 | Inspect MFA enrollment reports for all in-scope systems. Verify MFA is enforced (not optional) for 100% of user accounts. | MFA enforcement | IAM/SSO MFA enforcement configuration, enrollment report | |
| 6.2 | Confirm that MFA is enforced for: (a) remote access / VPN, (b) cloud consoles (AWS, Azure, GCP), (c) privileged accounts, (d) email / productivity platforms. | MFA coverage | Platform-specific MFA configuration screenshots | |
| 6.3 | Inspect password policy configuration for all in-scope identity systems. Verify it enforces: minimum 12 characters, complexity requirements, no reuse of last 12 passwords, and lockout after 10 failed attempts (or equivalent). | Password policy | AD/Okta password policy configuration | |
| 6.4 | Verify that service accounts have strong, unique passwords or certificate-based authentication, and credentials are managed in a secrets vault. | Service account security | Secrets management configuration (HashiCorp Vault, AWS Secrets Manager, etc.) | |
| 6.5 | Confirm that single sign-on (SSO) is implemented for in-scope applications where feasible, reducing password sprawl. | SSO coverage | SSO platform application list | |
| 6.6 | Verify that failed authentication attempts are logged and alerts are generated for unusual patterns (e.g., brute force, credential stuffing). | Authentication monitoring | SIEM authentication alerting rules | |

---

## Section 7: Segregation of Duties

| # | Audit Procedure | Objective | Evidence Required | Finding |
|---|----------------|-----------|-------------------|---------|
| 7.1 | Obtain the SoD matrix for critical business processes. Verify it identifies conflicting roles / permissions. | SoD documentation | SoD matrix | |
| 7.2 | Run an automated SoD analysis or manually cross-reference user access against the SoD matrix for in-scope systems. Identify users with conflicting access. | SoD conflict detection | SoD analysis report, IAM access data | |
| 7.3 | For any identified SoD conflicts: verify that (a) a business justification and management approval exists, or (b) a compensating control (monitoring, dual approval) is in place and operating. | SoD conflict remediation | Conflict documentation, compensating control evidence | |
| 7.4 | Verify that developers cannot deploy directly to production without a separate approver. | Code deployment SoD | CI/CD pipeline configuration, deployment approval records | |
| 7.5 | Confirm that financial system administrators cannot also approve financial transactions. | Financial SoD | ERP access controls, role configuration | |

---

## Exception Log

| # | Section | Sample Item | Exception Description | Risk Level | Remediation Required |
|---|---------|-------------|----------------------|------------|---------------------|
| | | | | | |

---

## Audit Conclusions

**Overall IAM Control Assessment:**

| Area | Effective | Partially Effective | Not Effective | N/A |
|------|-----------|--------------------|--------------|----|
| Policy & Governance | | | | |
| User Provisioning | | | | |
| Privileged Access | | | | |
| Deprovisioning | | | | |
| Access Reviews | | | | |
| Authentication Controls | | | | |
| Segregation of Duties | | | | |

**Key Findings:**
1.
2.
3.

**Recommendations:**
1.
2.
3.

---

*Audit Program Version: 1.0 | Aligned to: SOC 2 CC6, ISO 27001 A.5.15–A.5.18, NIST SP 800-53 AC*
