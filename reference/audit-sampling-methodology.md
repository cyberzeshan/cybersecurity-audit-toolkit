# Audit Sampling Methodology

**Purpose:** Reference guide for auditors on sampling standards, sample size determination, and selection methods for IT and cybersecurity control testing.
**Applicable Standards:** AICPA AT-C Section 205, AICPA AU-C Section 530, PCAOB AS 2315, IIA Practice Guide: Audit Sampling
**Scope:** All IT general control (ITGC) and application control testing in SOC 2, ISO 27001, and internal audit engagements

---

## Part 1: Sampling Fundamentals

### 1.1 Why We Sample

Testing 100% of transactions (vouching) is ideal but impractical for most controls. Sampling allows the auditor to draw a conclusion about a population based on a representative subset. The goal is not to find every exception — it is to determine whether the control is operating effectively based on the rate of exceptions observed.

### 1.2 Key Sampling Concepts

| Term | Definition |
|------|------------|
| **Population** | The entire set of items from which the sample is drawn (e.g., all provisioning requests in the audit period) |
| **Sample** | The subset of items actually tested |
| **Sampling Risk** | The risk that the auditor's conclusion based on the sample differs from the conclusion that would be reached by testing 100% |
| **Tolerable Deviation Rate** | The maximum exception rate the auditor is willing to accept and still conclude the control is effective |
| **Expected Deviation Rate** | The exception rate the auditor expects to find based on prior experience or preliminary testing |
| **Precision** | The allowable margin of error in projecting sample results to the population |

### 1.3 Sampling vs. Non-Sampling Risk

Audit risk has two components related to testing:

- **Sampling risk** — Can be managed by increasing sample size or using statistical methods
- **Non-sampling risk** — Cannot be reduced by sampling; it is the risk of a flawed test procedure, missed evidence, or incorrect evaluation. Addressed by quality workpaper review, not larger samples.

---

## Part 2: Types of Sampling

### 2.1 Statistical vs. Non-Statistical Sampling

| Attribute | Statistical Sampling | Non-Statistical (Judgmental) Sampling |
|-----------|---------------------|---------------------------------------|
| Selection method | Random (each item has a known, non-zero probability of selection) | Auditor judgment; no requirement for randomness |
| Projection | Results can be mathematically projected to full population | Results cannot be projected; extrapolation requires judgment |
| Required documentation | Probability of selection, confidence level, precision | Selection rationale, risk basis, professional judgment |
| When to use | Large populations; when precision is critical; regulatory exams | Most internal audits, SOC 2, ISO 27001 engagements |
| Common in | PCAOB engagements, SOX, financial statement audits | IT general controls, SOC 2, ISO 27001, internal IT audits |

> **For most SOC 2 and internal cybersecurity audits:** Non-statistical (judgmental) sampling is appropriate and widely accepted by external auditors, provided sample sizes are appropriate and selection is free from bias.

### 2.2 Non-Statistical Sampling Approaches

| Approach | Method | When to Use | Risk of Bias |
|----------|--------|-------------|-------------|
| **Random** | Random number generator applied to numbered population | Large populations; want objective selection | Low |
| **Systematic** | Select every Nth item (e.g., every 30th record) | When population is sorted in a meaningful way | Moderate (if population sorted by same characteristic as exception) |
| **Stratified** | Divide population into groups; sample from each | When subgroups carry different risk levels | Low if strata are well-defined |
| **Risk-based** | Select items with specific risk characteristics (e.g., all privileged access grants) | Supplementing a random sample with high-risk items | High if used alone without random component |
| **Haphazard** | Select without deliberate method or bias | Rarely appropriate; document no bias | High |

---

## Part 3: Sample Size Standards

### 3.1 Non-Statistical Sample Sizes for IT Controls

The following table is based on AICPA AT-C Section 205 guidance and industry practice for non-statistical (judgmental) sampling in IT control engagements:

#### For Annual-Frequency Controls (tested once per year)

| Population Size | Sample Size |
|----------------|-------------|
| 1 | 1 (100%) |
| 2–5 | 100% (all items) |

#### For Periodic Controls (weekly, monthly, quarterly) — Standard Risk

| Population Size | Sample Size | Basis |
|----------------|-------------|-------|
| 1–25 items | 100% | Full population testing for small populations |
| 26–50 | 5 | Low-risk threshold |
| 51–100 | 10 | Standard internal audit practice |
| 101–250 | 15 | Standard guidance |
| 251–500 | 20–25 | AICPA AT-C 205 standard range |
| > 500 | 25 | Standard maximum for moderate-risk controls |

#### For High-Risk or Highly-Relied-Upon Controls

| Population Size | Sample Size |
|----------------|-------------|
| 1–25 | 100% |
| 26–100 | 15–20 |
| 101–500 | 25–30 |
| > 500 | 30–40 |

### 3.2 Common Sample Sizes by Control Type

| Control Type | Typical Population Size | Standard Sample Size |
|-------------|------------------------|----------------------|
| User provisioning (new hires) | 50–1,000+ per year | 25 |
| User deprovisioning (terminations) | 50–500+ per year | 25 |
| Access reviews (quarterly = 4 reviews) | 4 occurrences | Test all 4 (100%) |
| Change management (production changes) | 100–2,000+ per year | 25 |
| Critical vulnerability remediation | Varies | 25 (or all critical items if < 25) |
| Vendor security assessments | 10–100 vendors | 10–15 (Tier 1 = 100%) |
| Patch management (OS patches) | Varies | 5 critical patches during period |
| Incident response (incidents) | Varies | 10–15 or all if < 15 |

### 3.3 Adjusting Sample Size

Increase sample size when:
- Expected deviation rate is higher than zero (prior year exceptions found)
- Control risk is high (key control with significant financial or data risk)
- Prior year found a pattern of exceptions (systemic vs. isolated)
- The engagement requires a high level of assurance (external SOC 2, regulatory)

Decrease sample size when:
- Strong automated controls exist with no manual override (automated controls may require only 1–5 items to verify configuration)
- Population is very small (full population testing below 25)
- The control is not heavily relied upon (supplementary / compensating control)

---

## Part 4: Population Completeness

Before drawing a sample, you must verify that the population is complete. An incomplete population can produce a biased or misleading sample.

### 4.1 Population Completeness Procedures

| Method | How to Apply | When Adequate |
|--------|-------------|---------------|
| **Reconciliation to independent source** | Compare population count to another source (e.g., HR new-hire count, ITSM ticket total) | Best method; always preferred |
| **Trend reasonableness** | Compare population size to prior year and assess reasonableness | Supplementary; not sufficient alone |
| **Count check** | Re-count items in provided population; confirm no duplicates | Minimum acceptable; combined with other methods |
| **Written management assertion** | Obtain written confirmation from client that population is complete | Acceptable when combined with at least one independent check |

### 4.2 Documenting Population Completeness

The workpaper must document:
1. The total count of the population
2. The source system and export method
3. The completeness verification method used
4. The result of the verification
5. Any items excluded from the population and the rationale

---

## Part 5: Selection Techniques

### 5.1 Random Number Generation

**Tool Options:**
- Excel: `=RANDBETWEEN(1, N)` — generates a random integer between 1 and N
- Excel: `=RAND()` combined with `RANK()` to randomly sort a list
- Python: `random.sample(range(1, N+1), k)` — generates k unique random numbers
- R: `sample(1:N, k, replace=FALSE)`
- Random.org: Free online random number generator (audit-defensible)
- Commercial audit software: CaseWare, IDEA, ACL/Galvanize

**Documentation Required:**
- Tool used
- Range of numbers (1 to N, where N = population size)
- Numbers generated
- Items selected based on those numbers
- Screenshot or export of the random selection output

### 5.2 Stratified Selection — Step by Step

1. Identify the strata and define boundaries clearly (e.g., Tier 1 vendors, privileged accounts, terminations in Q4)
2. Determine the sample allocation across strata (risk-weighted)
3. Apply random selection within each stratum independently
4. Document stratum boundaries, sample sizes per stratum, and selection method for each

### 5.3 Systematic Selection

1. Sort the population by a neutral characteristic (e.g., ticket number, date, alphabetical name — NOT by a characteristic that could correlate with exceptions)
2. Calculate the interval: N ÷ n (e.g., 500 items, 25 sample = every 20th item)
3. Select a random starting point between 1 and the interval
4. Select every Nth item from the starting point

> **Caution:** Do not use systematic selection if the population is sorted by a characteristic that might correlate with the exception being tested. For example, sorting by approver name and selecting every 20th item could inadvertently exclude all items from one approver.

---

## Part 6: Evaluating Sample Results

### 6.1 Exception Rate Calculation

```
Exception Rate (%) = (Number of Exceptions ÷ Sample Size) × 100

Example: 3 exceptions in a sample of 25
Exception Rate = (3 ÷ 25) × 100 = 12%
```

### 6.2 Comparing to Tolerable Deviation Rate

| Tolerable Deviation Rate | Application |
|------------------------|-------------|
| 3% | High-risk controls; heavily relied upon; regulated environments (PCI-DSS) |
| 5% | Standard threshold for most SOC 2 and internal audit controls |
| 7–10% | Lower-risk controls; supplementary controls; detective-only controls |

**Outcome Determination:**
- Exception rate < Tolerable Rate → Sample supports conclusion that control is effective
- Exception rate > Tolerable Rate → Sample does not support effectiveness conclusion; investigate exceptions; expand testing or conclude deficiency

### 6.3 When Exception Rate Exceeds the Tolerable Rate

Options when exceptions exceed the tolerable rate:

1. **Expand the sample:** Test additional items to determine if the exception is isolated or systemic. If expanded testing yields a lower exception rate that falls within tolerance, this may support a qualified conclusion.
2. **Report the deficiency:** Classify per the deficiency classification guide and report accordingly.
3. **Investigate root cause:** Understand whether the exceptions share a common cause. A single root cause affecting a small subset is classified differently than systemic failure.
4. **Evaluate compensating controls:** Determine whether compensating controls mitigate the risk of the primary control failure.

### 6.4 One Exception in a Small Sample

One exception in a sample of 25 (4%) is at the edge of a 5% tolerable rate. Apply the following judgment:

- If the exception is isolated (unique circumstances; one control owner; one time period) → Control Deficiency; note in report
- If the exception suggests a pattern or root cause that likely affects more items → Expand sample; investigate; consider elevated classification
- Never dismiss an exception simply because it is "only one" — one exception in a five-item sample is 20%

---

## Part 7: Automated Control Testing

Automated controls (system-enforced controls) are tested differently from manual controls.

### 7.1 Why Automated Controls Require Fewer Items

When a control is fully automated (the system enforces it without human intervention), there is no deviation risk from human non-compliance. The risk is in the configuration, not the execution.

**For automated controls:**
- Test the configuration once (verify the setting) — typically 1–3 items
- Confirm the system was not changed or overridden during the audit period
- Supplement with a small sample of transactions to confirm the automated control fired correctly

### 7.2 Automated Control Testing Approach

| Step | Procedure |
|------|-----------|
| 1. Obtain configuration | Screenshot or export of system configuration showing the control setting |
| 2. Verify the setting | Confirm configuration matches policy requirement |
| 3. Verify stability | Confirm no changes to configuration during audit period (change log review) |
| 4. Test a sample | Test 1–5 transactions to confirm the automated control executed as configured |
| 5. Confirm no override mechanism | Verify there is no manual bypass available to users |

**Note:** If an automated control can be bypassed by administrators, the bypass capability must also be tested (who has bypass access? Was bypass used? Was use reviewed?).

---

## Part 8: SOC 2 vs. Internal Audit Sampling Comparison

| Attribute | SOC 2 Type II (CPA Firm) | Internal Audit |
|-----------|-------------------------|----------------|
| Standard sample sizes | AICPA AT-C 205 | IIA Practice Guide: Audit Sampling |
| Minimum for large populations | 25 (moderate risk) | 20–25 (moderate risk) |
| Approach | Non-statistical judgmental | Non-statistical judgmental |
| Tolerable deviation rate | Typically 5% | Typically 5–7% |
| Random selection required? | Yes (unbiased selection) | Yes (unbiased selection) |
| Can exceptions be excluded? | No — exceptions must be reported | No — exceptions must be reported |
| Population completeness | Must be verified and documented | Must be verified and documented |

---

*Audit Sampling Methodology Version: 1.0*
*Reference: AICPA AT-C Section 205, AICPA AU-C Section 530, PCAOB AS 2315, IIA Practice Guide: Audit Sampling (2013)*
