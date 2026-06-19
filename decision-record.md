# Decision Record: EduPay Risk Acceptance

**Status:** $\textcolor{ForestGreen}{\textsf{Production-tested}}$ (Anonymised for the XUST universe)

This document captures the "meeting where it was challenged." It outlines the judgment layer behind the [worked example](worked-example.md), detailing why the decision was made, the political realities navigated, and how the decision was defended against anticipated scrutiny.

---

## 1. The Context and Constraints

**The Trigger:** An external audit finding flagged that EduPay, XUST's payroll vendor, lacked MFA and encryption at rest. 

**The Reality:** 
- **Financial:** Terminating the contract and migrating to a new vendor would cost R4.5 million. The entire IT security budget for the year is R1.2 million.
- **Operational:** Migrating a payroll system takes 9-12 months. The risk would exist during the migration regardless.
- **Political:** The Director of HR (the business owner) refused to halt payroll operations or absorb the cost of a rushed migration. IT cannot force a business unit to abandon a critical operational tool without executive backing.

## 2. Options Rejected

| Option | Why it was rejected |
|---|---|
| **Demand immediate vendor remediation** | The vendor is a small regional player. They simply do not have the engineering capacity to build MFA and encryption at rest in less than 18 months. Demanding the impossible is not a control. |
| **Implement an SSO Overlay (Okta/Entra ID)** | EduPay's legacy architecture does not support SAML 2.0 or OIDC. We could not force our own MFA onto their platform. |
| **Refuse to accept the risk (IT Security veto)** | Security does not own the business risk; the business does. Refusing to process the risk acceptance would leave the vulnerability undocumented and unmanaged, effectively hiding it from the Board. |

## 3. The Decision Defended

We chose to formally accept the risk, apply IP whitelisting as a compensating control, and escalate the sign-off to the Audit & Risk Committee.

### Anticipated Challenge 1: The External Auditor
**Auditor's likely challenge:** *"IP whitelisting does not solve the lack of encryption at rest. The data is still vulnerable if the vendor's database is compromised."*

**My Defense:** *"Agreed. That is why the residual risk remains rated as 'High'. We are not claiming the risk is mitigated; we are claiming it is governed. We have reduced the likelihood of credential stuffing via the IP whitelist, and we have forced the business to acknowledge the remaining exposure at the Board level. The expiration date on this acceptance is tied to the contract renewal, forcing a hard Go/No-Go decision next year."*

### Anticipated Challenge 2: The Information Regulator (POPIA)
**Regulator's likely challenge (in the event of a breach):** *"You knew the vendor lacked basic security controls for special personal information. Why did you continue to use them?"*

**My Defense:** *"Under POPIA, security measures must be 'appropriate, reasonable technical and organisational measures' (Section 19). 'Reasonable' includes considering the cost and operational impact. Terminating a payroll system mid-contract and failing to pay 3,400 staff is not a reasonable immediate response to a vendor roadmap delay. We implemented the maximum technical controls available to us (IP whitelisting, VPN enforcement, password complexity) and initiated an RFP process for a replacement system."*

### Anticipated Challenge 3: The Audit & Risk Committee (Council)
**Council Member's likely challenge:** *"Why am I being asked to sign off on a broken IT system? Fix it."*

**My Defense:** *"You are not signing off on a broken IT system; you are signing off on a business constraint. HR requires this system to run payroll, but the vendor cannot meet our security standards. IT cannot fix the vendor's code. By signing this, you acknowledge that XUST accepts the financial and reputational exposure of using this vendor until the contract expires, at which point we will migrate."*

## 4. Where the Argument is Weakest

The weakest point in this decision is the reliance on the vendor's IP whitelisting implementation. If the vendor's own infrastructure is compromised (e.g., a supply chain attack or a misconfigured firewall on their end), our IP whitelisting provides zero protection for the unencrypted data at rest. 

We are accepting a high degree of third-party risk based entirely on the vendor's promise that their internal network is secure, which we cannot independently verify. This is why the risk rating remains High and requires Board-level visibility.
