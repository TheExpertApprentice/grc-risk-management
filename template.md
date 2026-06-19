# Risk Acceptance Template

**License:** CC BY-SA 4.0 — Free to use and adapt.

> **Guidance Note:** A formal risk acceptance is not a waiver to ignore security. It is a governance mechanism to acknowledge a known deficiency, quantify the exposure, implement compensating controls, and assign accountability for the residual risk until a permanent fix is viable. This template is designed to survive scrutiny from external auditors and regulators.
> 
> While the example in this repository focuses on a **third-party vendor risk**, this template applies equally to various real-life scenarios like **internal legacy systems** (e.g., an end-of-life Student Information System; port opened on internal facing systems). When adapting for legacy systems for instance, the constraint language typically shifts from contractual terms to technical debt, migration timelines, and lack of vendor support patches.

---

## 1. Risk Identification

| Field | Description |
|---|---|
| **Risk ID** | [Reference to central Risk Register, e.g., RSK-2024-042] |
| **Date Raised** | [YYYY-MM-DD] |
| **Raised By** | [Name and Title of Assessor/Analyst] |
| **Source** | [e.g., Annual External Audit, Penetration Test, Vendor Assessment] |
| **Asset / Vendor** | [Name of the system, application, or third-party vendor] |
| **Data Classification** | [e.g., Public, Internal, Confidential, Restricted/PII] |

## 2. Risk Description

**The Finding:**
[Describe the specific security deficiency. What is missing or misconfigured?]

**The Threat:**
[Describe the threat actor or event that could exploit this deficiency.]

**The Impact:**
[Describe the business impact if the risk materialises. Consider confidentiality, integrity, availability, financial loss, and regulatory penalties (e.g., POPIA, GDPR).]

## 3. Justification for Acceptance (The Constraint)

**Why can this not be remediated immediately?**
[Detail the specific business, financial, or technical constraints preventing immediate resolution. Examples: Vendor roadmap delays, active contract lock-in, prohibitive migration costs, lack of legacy system patches.]

**Options Evaluated and Rejected:**
1. **[Option A]:** [Why it was rejected]
2. **[Option B]:** [Why it was rejected]

## 4. Compensating Controls

[List the interim measures implemented to reduce the likelihood or impact of the risk while it remains accepted. These must be verifiable by an auditor.]

| Control Objective | Compensating Control Description | Status |
|---|---|---|
| [e.g., Access Restriction] | [e.g., IP whitelisting to restrict access to campus networks only] | [Active / Planned] |
| [e.g., Anomaly Detection] | [e.g., Increased logging and weekly manual review of access logs] | [Active] |

## 5. Risk Assessment

| Metric | Pre-Compensating Controls (Inherent) | Post-Compensating Controls (Residual) |
|---|---|---|
| **Likelihood** | [High / Medium / Low] | [High / Medium / Low] |
| **Impact** | [High / Medium / Low] | [High / Medium / Low] |
| **Overall Rating** | **[Critical / High / Medium / Low]** | **[Critical / High / Medium / Low]** |

## 6. Remediation Plan & Expiration

**Risk Acceptance Expiration Date:** [YYYY-MM-DD - Never accept a risk indefinitely. Maximum 12 months without review.]

**Path to Resolution:**
[Detail the long-term plan to eliminate the risk. E.g., "Migrate to new vendor upon contract expiry in Q3 2025," or "Decommission legacy system post-ERP migration."]

**Milestones:**
- 
- 

## 7. Approvals

> **Guidance Note:** The approver must have the authority to accept the business impact (financial/reputational) if the risk materialises. IT Security advises; the Business owns the risk.

| Role | Name | Signature / Approval Date |
|---|---|---|
| **Risk Owner (Business)** | [e.g., Director of HR, Dean of Faculty] | `redacted` |
| **Advisory (Security/GRC)** | [e.g., CISO, Information Security Manager] | `redacted` |
| **Final Authority (If High/Critical)**| [e.g., Audit & Risk Committee Chair] | `redacted` |
