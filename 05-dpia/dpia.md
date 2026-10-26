# Data Protection Impact Assessment: AI Claims Pre-Assessment

**Independent simulation.** Fictional insurer; no real personal data. A learning exercise, not legal advice or a completed statutory DPIA.

**Controller:** Example Mutual Insurance DAC (fictional)  |  **Version:** 0.1  |  **Date:** 26 October 2026

## 1. Why a DPIA is needed (screening)
The AI tool scores individual claims and assigns a handling priority, which is a form of profiling. It processes health data (D05, injury and medical documents), which is special category data under Article 9, and it may produce a fraud flag (D08) that relates to alleged offences. The scoring influences how claims are handled and could affect claimants financially. It applies new technology (a third-party AI model service) at scale, to about 200,000 policyholders plus claimants and third parties. Under GDPR Article 35(3) and the Data Protection Commission's guidance on processing likely to be high risk, these factors together mean a DPIA is required before deployment.

## 2. Description of the processing
- **Nature:** Claims arrive through the portal, by phone or via handlers, and are stored in the claims management system and document store. Relevant inputs (D16) are sent to a third-party AI service, which returns a risk score and priority (D07) and an explanation (D17). A handler reviews the claim and decides. Data is later deleted or anonymised under the retention schedule.
- **Scope:** Inventory items D01 to D18; ROPA activities 1 and 2 are the core of this DPIA, with activity 4 (fraud review) for D08. About 200,000 policyholders, plus claimants and third parties. Assumed retention is 7 years after claim closure; periods for scores, inputs and logs are still to be defined.
- **Context:** Policyholders expect their data to be used to handle claims, but may not expect AI scoring or fraud flagging. Some claimants may be vulnerable, for example people who are injured or in distress. Third parties have no relationship with the insurer.
- **Purposes:** Process routine claims more efficiently, and identify claims needing more evidence, specialist review or fraud investigation. The tool supports human decisions and does not approve or reject claims.

## 3. Necessity and proportionality
- **Lawful basis (assumed):** Contract for core claims handling; legitimate interests for risk scoring and fraud review, supported by a legitimate interests assessment. For health data, an Article 9 condition is also needed, for example explicit consent, or the insurance provisions of the Data Protection Act 2018. [verify]
- **Data minimisation:** Only the fields the model needs are sent (D16); bank details (D09), call recordings (D13) and raw correspondence (D12) are not sent. Health data is used only where the claim type needs it, and should be excluded from scoring unless justified.
- **Transparency:** The privacy notice and claim forms tell people that AI is used to prioritise claims, that a person makes the final decision, and how to ask for a review.
- **Individuals' rights:** Access, rectification, objection and human review are handled through the DPO. Claimants can ask a handler to reconsider a prioritisation. Whether any step is solely automated must be verified against Article 22.
- **Processors and transfers:** The AI provider is a processor under an Article 28 contract that prohibits using claim data for model training without approval. Data location, subprocessors and transfers outside the EEA must be confirmed. [verify]
- **Retention:** Claim records for 7 years after closure (illustrative). Scores, explanations, inputs, logs and vendor data need separate defined periods.
- **Is there a less intrusive way?** Partly. Manual triage with rules-based checks would use less data, but is slower and less consistent. The AI approach is proportionate only if health data is excluded from scoring unless needed, humans review every recommendation, and the model is tested for bias and accuracy.

## 4. Consultation
Simulated for this exercise; a real DPIA would record actual views.
- **DPO:** would ask for the Article 9 condition to be confirmed, a legitimate interests assessment, and Article 22 verification.
- **Claims staff:** would raise workload, and the need to override scores without penalty.
- **IT security:** would raise access control, logging and vendor security.
- **AI provider:** would need to confirm data location, subprocessors and no training on claim data.
- **Customer representatives:** would ask for plain-language information about AI use and an easy route to human review.

## 5. Risk assessment

Scale: Likelihood (1 Remote – 4 Almost certain) x Severity (1 Minimal – 4 Severe). Score 1–4 Low, 5–9 Medium, 10–16 High.

| # | Risk to individuals | Likelihood | Severity | Score | Level |
|---|---|---|---|---|---|
| R1 | Unauthorised access to claimant and special category (injury/medical) data | 3 | 4 | 12 | High |
| R2 | Biased or inaccurate risk score leads to unfair treatment or delayed claim | 3 | 3 | 9 | Medium |
| R3 | Decision made without meaningful human review (Art 22) | 2 | 4 | 8 | Medium |
| R4 | Data kept longer than necessary | 3 | 2 | 6 | Medium |
| R5 | Claimant not told how data and the AI score are used | 3 | 2 | 6 | Medium |
| R6 | Third-party/processor misuse or breach (Art 28) | 2 | 4 | 8 | Medium |
| R7 | Model leaks personal data from training or logs | 2 | 3 | 6 | Medium |
| R8 | Breach not notified within 72 hours (Art 33) | 2 | 3 | 6 | Medium |

## 6. Measures to reduce risk

| # | Measure | Effect on risk | Owner |
|---|---|---|---|
| R1 | Encryption in transit and at rest; RBAC and MFA; access logging and quarterly access reviews | Reduced | IT Security |
| R2 | Bias testing and accuracy monitoring; explanations (D17) shown to handlers; periodic model review | Reduced | Claims Analytics |
| R3 | Handler must review every recommendation and can override; override notes kept (D14); Article 22 position verified | Reduced | Claims Operations |
| R4 | Retention schedule with automated deletion | Reduced | Data Governance |
| R5 | Plain-language privacy notice and claimant information on AI use | Reduced | DPO |
| R6 | Art 28 contract, no model training on claim data, security due diligence, annual review | Reduced | IT Vendor Management / DPO |
| R7 | Minimised inputs; no raw identifiers in logs; vendor retention limits | Reduced | Claims Analytics |
| R8 | Incident response plan with 72-hour notification process and drills | Reduced | IT Security |

## 7. Residual risk and sign-off

| # | Residual likelihood | Residual severity | Score | Level | Accepted? |
|---|---|---|---|---|---|
| R1 | 2 | 3 | 6 | Medium | Yes |
| R2 | 2 | 2 | 4 | Low | Yes |
| R3 | 1 | 4 | 4 | Low | Yes |
| R4 | 1 | 2 | 2 | Low | Yes |
| R5 | 1 | 2 | 2 | Low | Yes |
| R6 | 2 | 3 | 6 | Medium | Yes |
| R7 | 1 | 3 | 3 | Low | Yes |
| R8 | 1 | 3 | 3 | Low | Yes |

**Conclusion:** after the measures above, no risk remains High. Residual Medium risks (R1, R6) are accepted with ongoing monitoring. Prior consultation with the DPC under Article 36 is not expected to be required, provided the open items below are resolved.

**Open items to verify before deployment:** Article 9 condition; Article 22 position; AI provider location, subprocessors and training restrictions; retention periods for scores, inputs and logs.

**DPO advice (simulated):** measures agreed, subject to the open items.
**Sign-off (simulated):** Controller representative [role], Date [date]. Review due: 12 months or on any material change.

*This DPIA is an independent portfolio exercise based on a fictional use case.*
