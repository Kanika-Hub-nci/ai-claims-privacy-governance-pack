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
| R1 | Encryption in transit and at rest; RBAC and MFA; access logging and quarterly access reviews | Reduced | Security Lead |
| R2 | Bias testing and accuracy monitoring; SHAP explanations shown to handlers; periodic model review | Reduced | Model Owner |
| R3 | Handler must review every referral and can override; record of overrides kept | Eliminated for solely automated decisions | Claims Manager |
| R4 | Retention schedule with automated deletion | Reduced | Data Governance |
| R5 | Plain-language privacy notice and claimant information on AI use | Reduced | DPO |
| R6 | Art 28 contract, security due diligence, annual review | Reduced | Procurement / DPO |
| R7 | Pseudonymisation; no raw identifiers in logs or training data | Reduced | Model Owner |
| R8 | Incident response plan with 72-hour notification process and drills | Reduced | Security Lead |

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

**Conclusion:** after the measures above, no risk remains High. Residual Medium risks (R1, R6) are accepted with ongoing monitoring. Prior consultation with the DPC under Art 36 is not required.

**DPO advice:** [Role: DPO] – advice recorded; measures agreed.
**Sign-off:** Controller representative [role], Date [date]. Review due: 12 months or on any material change.

*This DPIA is an independent portfolio exercise based on a fictional use case.*
