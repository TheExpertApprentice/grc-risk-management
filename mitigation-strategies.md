# Risk Mitigation Strategies — Reference Guide

**XUST Enterprise Risk Management**
*A companion reference to the Risk Appetite & Tolerance Practice Note and the XUST Risk Register suite.*

---

> [!NOTE]
> **Purpose.** This reference defines the risk-response options available to risk owners at XUST, the criteria that qualify a risk for each response, the conditions that must hold, and the authority required to endorse the decision. It exists so that every "treat / tolerate / transfer / terminate" decision recorded in a risk register can be justified against a documented standard — not improvised. Response selection is driven by where a risk sits relative to the institution's **risk appetite** and **risk tolerance** (see Practice Note, §5).

---

## The Mitigation Options 

| Code | Strategy | Plain-language intent | Typically used when… |
|:--:|---|---|---|
| **T1** | **Tolerate** (Accept) | Live with it, knowingly | Residual risk is within appetite, or cost of action exceeds the benefit |
| **T2** | **Treat** (Reduce / Mitigate) | Bring it down with controls | Risk exceeds appetite but the activity must continue |
| **T3** | **Transfer** (Share) | Move the financial sting elsewhere | Impact is severe but insurable or contractually shareable |
| **T4** | **Terminate** (Avoid) | Stop doing the risky thing | Risk is intolerable and the activity is not essential |
| **T5** | **Take / Pursue** (Exploit) | Lean in for the upside | The "risk" is an opportunity worth pursuing deliberately |

> The first letter is always **T** — a deliberate memory aid: *Tolerate, Treat, Transfer, Terminate, Take.*

---

## Choosing a response — decision logic

```
            ┌─────────────────────────────────────────────┐
            │   Assess inherent risk (Likelihood × Impact) │
            └───────────────────────┬─────────────────────┘
                                    ▼
                   Is residual within risk appetite?
                          │                   │
                        YES                   NO
                          │                   │
                          ▼                   ▼
                   ┌────────────┐   Is the activity essential?
                   │ T1 Tolerate│        │             │
                   │ (monitor)  │       YES            NO
                   └────────────┘        │             │
                                         ▼             ▼
                            Can controls reduce it?   ┌────────────┐
                                 │          │         │ T4         │
                                YES        NO         │ Terminate  │
                                 │          │         └────────────┘
                                 ▼          ▼
                         ┌────────────┐  Is impact insurable/
                         │ T2 Treat   │  contractually shareable?
                         └────────────┘     │          │
                                           YES         NO
                                            │          │
                                            ▼          ▼
                                     ┌────────────┐  Escalate to
                                     │ T3 Transfer│  RMC / EMC for
                                     └────────────┘  tolerance decision
```

> Opportunities follow a parallel path: where uncertainty carries strategic upside, consider **T5 · Take** rather than defaulting to a downside-only response.

---

## T1 · Tolerate (Accept the risk)

**Definition.** A conscious, documented decision to retain a risk at its current level without further treatment, accepting the potential consequence should it materialise.

**Qualification criteria — tolerate when *any* of the following hold:**
1. The risk is regarded as **unavoidable** and is inherently associated with pursuing a legitimate institutional opportunity.
2. The risk is of **high impact but low likelihood**, resulting in a low overall risk magnitude.
3. The **residual risk already falls within the institution's risk appetite** (refer to the Risk Appetite & Tolerance Practice Note, §5.3).
4. The **cost of further treatment would exceed the benefit** gained (proportionality test).

**Conditions that must be satisfied:**
- The risk magnitude is **Low** as defined in the approved Risk Matrix, *or* the high-impact/low-likelihood profile has been explicitly reviewed.
- The related consequences do **not** expose the University to catastrophic outcomes — loss of life, closure of the institution, de-accreditation of programmes, or material reputational compromise. Such consequences may **never** simply be tolerated regardless of likelihood.
- A **monitoring trigger** is defined: the conditions under which the acceptance will be revisited (e.g. a change in likelihood, a near-miss, a regulatory change).

**Endorsement authority:**
- A management decision to tolerate a **strategic** risk of high impact and low likelihood must be endorsed by the **Risk Management Committee (RMC)**, the **Executive Management Committee (EMC)**, *and* the **Audit & Risk Committee**.
- All **non-strategic** risk acceptances must be endorsed by the **RMC**.
- Every acceptance is recorded in the register with an owner, a date, and a review date — acceptance is **time-bound**, never permanent.

---

## T2 · Treat (Reduce / Mitigate)

**Definition.** The application of one or more controls to reduce a risk's **likelihood**, its **impact**, or both — moving the residual rating into the acceptable zone.

**Qualification criteria — treat when:**
1. The inherent or current residual risk **exceeds the risk appetite**, and
2. The underlying activity is **necessary** and cannot reasonably be terminated, and
3. **Cost-effective controls exist** that can credibly reduce the rating.

**Conditions that must be satisfied:**
- Each proposed control is mapped to whether it reduces **likelihood**, **impact**, or both.
- The **target residual rating** is stated *before* implementation, so effectiveness can be measured against it.
- Controls are classified as **preventive**, **detective**, or **corrective**, and the mix is deliberate (not all detective).
- A **control owner** and an **implementation timeline** are assigned; the treatment is captured in a Risk Treatment Plan.

**Endorsement authority:**
- Operational treatments: approved by the **risk owner** and noted by the **RMC**.
- Treatments requiring **budget** beyond delegated authority: escalated to the **EMC** per the Delegation of Authority.

---

## T3 · Transfer (Share the risk)

**Definition.** Shifting some or all of the financial consequence of a risk to a third party — through insurance, outsourcing, or contractual allocation — without (usually) removing the underlying risk itself.

**Qualification criteria — transfer when:**
1. The potential **impact is severe** enough to threaten financial stability, and
2. The risk is **insurable** or contractually **assignable**, and
3. Transfer is **more cost-effective** than treating the risk to an acceptable level internally.

**Conditions that must be satisfied:**
- It is understood that transfer addresses **financial consequence**, not **accountability** — reputational and regulatory accountability (e.g. under POPIA, the University remains the responsible party) usually **cannot** be transferred.
- The transfer instrument (insurance policy, SLA, indemnity clause) is **reviewed by Legal** and its coverage limits, exclusions, and triggers are documented.
- **Residual retained risk** (deductibles, uninsured portions, counterparty failure) is itself recorded and managed.

**Endorsement authority:**
- Insurance and indemnity arrangements: endorsed by the **CFO** and reviewed by the **Audit & Risk Committee**.
- Contractual transfer to vendors: endorsed via **Supply Chain Management** and **Legal**.

---

## T4 · Terminate (Avoid the risk)

**Definition.** Eliminating the risk entirely by ceasing, withdrawing from, or not commencing the activity that gives rise to it.

**Qualification criteria — terminate when:**
1. The risk is **intolerable** — it exceeds tolerance and cannot be treated or transferred to an acceptable level, *or*
2. The consequences include **catastrophic** outcomes (loss of life, closure, de-accreditation, criminal liability), *and*
3. The activity is **not essential** to the University's mission, or an acceptable alternative exists.

**Conditions that must be satisfied:**
- The **knock-on impact** of terminating the activity (lost opportunity, dependency on it elsewhere) is assessed and documented.
- Where the activity is essential and cannot truly be terminated, this response is **invalid** — the risk must instead be treated and escalated.

**Endorsement authority:**
- Termination of a **strategic** activity or programme: decided by the **EMC** and reported to **Council** via the Audit & Risk Committee.

---

## T5 · Take / Pursue (Exploit the opportunity)

**Definition.** A deliberate decision to accept and actively pursue a risk because its potential **upside** (opportunity) outweighs its downside — the positive counterpart to tolerate.

**Qualification criteria — take when:**
1. The uncertainty carries a credible **opportunity** (new revenue stream, research partnership, competitive advantage), and
2. The potential benefit is **proportionate** to the downside exposure, and
3. The pursuit is **aligned to strategy** and within the institution's capacity to absorb the downside.

**Conditions that must be satisfied:**
- The opportunity is linked to a **strategic objective**.
- Both the **upside target** and the **downside limit** are quantified.
- A trigger is defined for withdrawing if the downside limit is approached.

**Endorsement authority:**
- Endorsed by the **EMC** as part of strategic planning, with material commitments reported to **Council**.

---

## How this links to the rest of the suite

- The **response code (T1–T5)** chosen for each risk should be recorded in the register's mitigating-strategy column.
- Every **T2 Treat** decision should generate a **Risk Treatment Plan** (see companion template).
- The **appetite and tolerance thresholds** that drive these decisions are defined in the **Risk Appetite & Tolerance Practice Note** and visualised in the **XUST Risk Matrix**.

---

<sub>XUST Enterprise Risk Management · GRC Campus portfolio. Fictional composite for demonstration. Aligned to ISO 31000:2018 risk-treatment principles and King IV™ Principle 11 (Risk Governance). Reuse under CC BY-SA 4.0.</sub>
