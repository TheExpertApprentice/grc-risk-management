# Risk Acceptance: EduPay Third-Party Vendor (Worked Example)

**Status:** $\textcolor{ForestGreen}{\textsf{Production-tested}}$ (Anonymised for the XUST universe)

This document is a fully completed example of the Risk Acceptance Template, demonstrating how to document a complex third-party vendor risk within the constraints of XUST (X University of Science and Technology).

---

## 1. Risk Identification

| Field | Description |
|---|---|
| **Risk ID** | RSK-2024-089 (Linked to Central Risk Register) |
| **Date Raised** | 2024-03-15 |
| **Raised By** | Senior GRC Analyst |
| **Source** | Annual External Audit Finding (Ref: EXT-AUD-24-12) |
| **Asset / Vendor** | EduPay (SaaS Payroll and HR Management Platform) |
| **Data Classification** | Restricted / Special Personal Information (Staff PII, Banking Details, Salaries) |

## 2. Risk Description

**The Finding:**
During the annual supplier security assessment initiated by the external audit, it was identified that EduPay, XUST's payroll vendor, does not support Multi-Factor Authentication (MFA) for administrative logins, nor does it provide encryption at rest for the database housing XUST employee data. This violates XUST Information Security Policy (Sec. 4.2) and ISO 27001 A.5.20 (Addressing information security within supplier agreements).

**The Threat:**
Credential stuffing, phishing of HR staff, or a breach of the vendor's infrastructure could lead to unauthorised access to the payroll system.

**The Impact:**
Exposure of banking details and salaries for 3,400 XUST staff members. This constitutes a severe data breach under the Protection of Personal Information Act (POPIA), potentially leading to Information Regulator fines, reputational damage, and financial fraud against employees.

## 3. Justification for Acceptance (The Constraint)

**Why can this not be remediated immediately?**
EduPay is a regional vendor tailored for the South African higher education sector. They have acknowledged the deficiency but stated that MFA and encryption-at-rest are on their development roadmap for Q3 2025. 

XUST is currently 10 months into a 24-month contract with EduPay. The cost to terminate the contract early and migrate to an enterprise-grade alternative (e.g., Workday or SAP) is estimated at R4.5 million, which exceeds the entire annual IT security budget and the HR operational budget combined. A migration would also take a minimum of 9 months to implement, during which the risk would remain.

**Options Evaluated and Rejected:**
1. **Immediate Contract Termination & Migration:** Rejected by the Director of Finance due to prohibitive costs (R4.5m) and unacceptable disruption to payroll processing.
2. **Implementation of a SAML/SSO overlay (e.g., Okta/Entra ID):** Rejected because EduPay's legacy architecture does not support SAML 2.0 or OIDC integration.

## 4. Compensating Controls

To reduce the likelihood of exploitation while the vendor updates their platform, the following interim controls have been implemented:

| Control Objective | Compensating Control Description | Status |
|---|---|---|
| **Access Restriction** | EduPay has configured IP whitelisting on their tenant. The administrative portal can now only be accessed from the XUST internal HR subnet or via the staff VPN. | Active |
| **Credential Security** | HR staff accessing EduPay are required to use complex, 16-character passphrases managed by the enterprise password manager, mitigating credential reuse. | Active |
| **Anomaly Detection** | IT Security has configured an alert in Wazuh to monitor VPN logins by HR staff outside of standard business hours (07:00 - 18:00). | Active |
| **Data Minimisation** | HR has purged all historical records of former employees older than 5 years from the EduPay system, reducing the blast radius of a potential breach. | Active |

## 5. Risk Assessment

| Metric | Pre-Compensating Controls (Inherent) | Post-Compensating Controls (Residual) |
|---|---|---|
| **Likelihood** | High (No MFA, internet-facing portal) | Medium (Restricted to VPN/Campus IP) |
| **Impact** | High (POPIA violation, 3,400 staff affected) | High (Data is still unencrypted at rest) |
| **Overall Rating** | **Critical** | **High** |

*Note: The impact remains High because compensating controls primarily address the likelihood of access, not the lack of encryption at rest on the vendor's side.*

## 6. Remediation Plan & Expiration

**Risk Acceptance Expiration Date:** 2025-05-01 (Aligns with the end of the current EduPay contract).

**Path to Resolution:**
XUST will not renew the EduPay contract unless the vendor provides independent attestation (e.g., SOC 2 Type II or ISO 27001 certification) proving that MFA and encryption-at-rest have been implemented. Concurrently, the HR department will begin drafting an RFP for a replacement payroll system in Q4 2024 to ensure a viable alternative is available before contract expiry.

**Milestones:**
- **2024-10-01:** HR to issue RFP for alternative payroll solutions (Contingency planning).
- **2025-01-15:** Vendor check-in to assess progress on their Q3 2025 security roadmap.
- **2025-03-01:** Final Go/No-Go decision on EduPay contract renewal based on feature delivery.

## 7. Approvals

*Because the residual risk remains High and involves significant POPIA exposure, this acceptance requires escalation to the Audit & Risk Committee.*

| Role | Name | Signature / Approval Date |
|---|---|---|
| **Risk Owner (Business)** | Redacted, Director of Human Resources | *Approved via AdobeSign (2024-03-18)* |
| **Advisory (Security/GRC)** | [Chris Ejike], Senior GRC Analyst | *Approved via AdobeSign (2024-03-16)* |
| **Final Authority** | Redacted, Chair: Audit & Risk Committee | *Approved via Board Portal (2024-03-25)* |
