# Sample Selection Workpaper

**Engagement:** [ENGAGEMENT NAME]
**Audit Period:** [START DATE] – [END DATE]
**Control / Test Area:** [e.g., User Access Provisioning — CC6.1]
**Auditor:** [NAME]
**Date Prepared:** [DATE]

---

## Purpose

This workpaper documents the population definition, completeness verification, sampling methodology, and sample selection for [CONTROL / TEST AREA]. It provides the audit trail required to demonstrate that the sample was selected in a manner free from bias and is appropriate for the risk level of the control being tested.

---

## Step 1: Population Definition

### 1.1 Population Description

| Field | Detail |
|-------|--------|
| Population Name | [e.g., User provisioning requests — audit period] |
| Audit Period | [e.g., January 1, 2025 – December 31, 2025] |
| Population Count | [e.g., 847 provisioning requests] |
| System of Record | [e.g., ServiceNow ITSM — Incident/Request module] |
| Export Method | [e.g., Exported via IT Request report by ITSM Admin; filtered by category = "Access Request"; date range = audit period] |
| Export Date | [DATE] |
| Population Preparer | [Name — control owner / IT team member who provided the export] |

### 1.2 Population Completeness Verification

> Before sampling, verify that the population provided is complete. An incomplete population can lead to a biased or invalid sample.

| Completeness Check | Method | Result | Pass/Fail |
|-------------------|--------|--------|-----------|
| Count reconciliation | Compare ITSM export count (847) against HR new-hire count (312) + internal transfer count (211) + contractor additions (324) | Total = 847; agrees ✓ | Pass |
| Date range verification | Confirm all records fall within audit period start/end dates | Reviewed min/max dates in export: 2025-01-02 to 2025-12-28 ✓ | Pass |
| Duplicate check | Sorted by ticket ID; confirmed no duplicate records | No duplicates found ✓ | Pass |
| Missing fields | Reviewed for null values in key fields (Date, Requestor, Approver) | 3 tickets missing approver field — flagged for investigation | Finding |
| Completeness assertion | Obtained written confirmation from IT Manager that no additional records exist outside this export | Email confirmation on file (Exhibit A) ✓ | Pass |

**Completeness Conclusion:** The population of [X] items is considered complete and appropriate for sampling. [Note any exceptions to completeness and how they were resolved.]

---

## Step 2: Population Stratification

> Stratify the population when certain subgroups carry higher risk and should be represented in (or excluded from) the sample independently.

### Strata Identified

| Stratum | Description | Count | % of Population | Sampling Approach |
|---------|-------------|-------|-----------------|-------------------|
| Privileged | Requests for admin, root, or elevated access | 42 | 5% | Risk-based: include all in sample pool; select 10 |
| Standard | Regular user access requests | 805 | 95% | Random: select 15 from this stratum |
| **Total** | | **847** | **100%** | **25 total items** |

**Stratification Rationale:** Privileged access grants represent elevated risk (broader access, higher potential impact if misprovisioned). Separate stratification ensures they are not underrepresented in the sample.

---

## Step 3: Sampling Approach Selection

### 3.1 Approach Selected

☐ **Statistical (Random) Sampling** — Results can be extrapolated to the full population. Requires random number generator and documentation of selection process. Preferred for large populations and medium-to-high risk controls.

☑ **Judgmental (Non-Statistical) Sampling** — Results cannot be extrapolated to the full population. Auditor uses professional judgment. Acceptable for most internal audit engagements, SOC 2, and ISO 27001.

☐ **Haphazard Sampling** — Items selected without a deliberate method (e.g., every 10th item). Must document no intentional bias. Least preferred.

**Rationale for Selected Approach:**
[e.g., Judgmental sampling is appropriate for this engagement. The population is well-structured with clear stratification. Professional judgment is applied to ensure representation of high-risk items. Statistical projection to the population is not required for this engagement's objectives.]

---

## Step 4: Sample Size Determination

### 4.1 Sample Size Inputs

| Factor | Assessment | Impact on Sample Size |
|--------|------------|----------------------|
| Control risk | ☐ Low  ☑ Moderate  ☐ High | Moderate → standard sample size |
| Population size | 847 items (> 500) | Large population → upper range of size guidance |
| Expected exception rate | < 2% based on prior year results | Low expected rate → no inflation needed |
| Tolerable deviation rate | 5% (established by engagement lead) | Standard threshold |
| Control reliance | ☑ Reliance intended  ☐ No reliance | Reliance → use standard guidance minimum |

### 4.2 Sample Size Selected

**Final Sample Size: 25 items**

**Basis:** Per AICPA AT-C Section 205 non-statistical sampling guidance: population > 500, moderate risk, tolerable deviation rate 5% → sample size of 25 is appropriate.

| Stratum | Sample Size | Selection Method |
|---------|-------------|-----------------|
| Privileged (n=42) | 10 | Random number generator |
| Standard (n=805) | 15 | Random number generator |
| **Total** | **25** | |

---

## Step 5: Sample Selection

### 5.1 Random Selection Method

**Tool Used:** [e.g., Excel RAND() function / Python random.sample() / Random.org / Audit software]

**Selection Documentation:**

For the **Privileged stratum** (n=42, selecting 10):
1. Assigned sequential numbers 1–42 to sorted privileged request list
2. Generated 10 random numbers between 1–42 using [tool]
3. Random numbers generated: [list the 10 numbers]
4. Items corresponding to those numbers were selected

For the **Standard stratum** (n=805, selecting 15):
1. Assigned sequential numbers 1–805 to sorted standard request list
2. Generated 15 random numbers between 1–805 using [tool]
3. Random numbers generated: [list the 15 numbers]
4. Items corresponding to those numbers were selected

### 5.2 Items Selected

| # | Ticket ID | Date | Requestor | Access Type | System | Stratum | Selection Method |
|---|-----------|------|-----------|-------------|--------|---------|-----------------|
| 1 | | | | | | Privileged | Random |
| 2 | | | | | | Privileged | Random |
| 3 | | | | | | Privileged | Random |
| 4 | | | | | | Privileged | Random |
| 5 | | | | | | Privileged | Random |
| 6 | | | | | | Privileged | Random |
| 7 | | | | | | Privileged | Random |
| 8 | | | | | | Privileged | Random |
| 9 | | | | | | Privileged | Random |
| 10 | | | | | | Privileged | Random |
| 11 | | | | | | Standard | Random |
| 12 | | | | | | Standard | Random |
| 13 | | | | | | Standard | Random |
| 14 | | | | | | Standard | Random |
| 15 | | | | | | Standard | Random |
| 16 | | | | | | Standard | Random |
| 17 | | | | | | Standard | Random |
| 18 | | | | | | Standard | Random |
| 19 | | | | | | Standard | Random |
| 20 | | | | | | Standard | Random |
| 21 | | | | | | Standard | Random |
| 22 | | | | | | Standard | Random |
| 23 | | | | | | Standard | Random |
| 24 | | | | | | Standard | Random |
| 25 | | | | | | Standard | Random |

---

## Step 6: Item Substitution (If Applicable)

> If a selected item cannot be tested (e.g., evidence unavailable, item is out of scope), a substitution may be made. All substitutions must be documented.

| Original Item | Reason for Substitution | Replacement Item | Approval |
|--------------|------------------------|-----------------|----------|
| | | | |

**Substitution Policy:** No more than [3] substitutions are permitted per sample without re-evaluating sample size. Items removed because they are exceptions (not available / not found) should NOT be substituted — they remain as exceptions.

---

## Step 7: Results Summary

> Complete after testing. Reference the control testing workpaper for full results.

| Stratum | Tested | Exceptions | Exception Rate | Tolerable Rate | Pass/Fail |
|---------|--------|------------|---------------|----------------|-----------|
| Privileged | 10 | | | 5% | |
| Standard | 15 | | | 5% | |
| **Combined** | **25** | | | **5%** | |

---

## Evidence Index

| Exhibit | Description | Obtained From | Date |
|---------|-------------|---------------|------|
| Exhibit A | Population export from ServiceNow | IT Manager | |
| Exhibit B | HR completeness confirmation email | HR Business Partner | |
| Exhibit C | Random number generator output / selection log | Auditor | |
| Exhibit D | Sampling methodology reference (AICPA AT-C 205) | Reference library | |

---

*Sample Selection Workpaper Version: 1.0 | Reference: AICPA AT-C Section 205, IIA Practice Guide: Audit Sampling*

```
Prepared By:  _________________________  Date: ______________
Reviewed By:  _________________________  Date: ______________
```
