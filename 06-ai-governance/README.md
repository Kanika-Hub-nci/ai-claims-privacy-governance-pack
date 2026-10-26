# AI Governance Note: AI Claims Pre-Assessment

**Independent simulation.** Fictional insurer; no real personal data. A learning exercise, not legal advice and not a conformity assessment.

## 1. What the system does
The tool scores incoming motor and home claims, assigns a handling priority and gives an explanation (inventory D07, D16, D17). It makes recommendations only. A claims handler makes the final decision.

## 2. EU AI Act: likely classification (to be verified)
- **Annex III high-risk list:** the insurance entries cover risk assessment and pricing for **life and health** insurance, and credit scoring (which excludes fraud detection). A motor and home claims triage tool does not obviously fall in either, so it is **probably not high-risk under Annex III**. [verify against the final legal text and the Commission's guidance]
- **If the design changes** (for example, it starts to decide claims, or uses health data to score), the classification must be reassessed.
- **Obligations that apply anyway:** AI literacy for staff who use the system (Art 4), and prohibited practices must be avoided (Art 5).
- **Application dates** for the high-risk rules have been under review. Check the current dates before relying on them.
- **Voluntary good practice:** the insurer should follow the high-risk standards (risk management, data governance, logging, human oversight, accuracy testing) because of the fairness and GDPR risks in the DPIA.

## 3. Governance controls

| Area | Control | Link to the pack |
|---|---|---|
| Accountability | Named model owner (Claims Analytics), approval before go-live, annual review | DPIA section 6 |
| Human oversight | Handler reviews every recommendation, can override and records why (D14) | DPIA R3 |
| Explainability | Each score comes with an explanation (D17) that the handler can read | DPIA R2 |
| Fairness | Bias and accuracy testing across claim types and customer groups before launch and on a schedule | DPIA R2 |
| Data governance | Minimised inputs (D16); health data excluded from scoring unless justified | DPIA section 3 |
| Vendor control | Art 28 contract; no training on claim data without approval; data location confirmed | DPIA R6, inventory D18 |
| Monitoring | Track error rates, overrides, complaints and drift; suspend the tool if serious problems appear | Use case section 10 |
| Logging | Access and activity logs kept and reviewed (D15) | ROPA activity 6 |
| Incident handling | Model incidents handled through the security incident process with a 72-hour breach check | DPIA R8 |
| Transparency | Claimants told about AI use and how to request human review | DPIA R5 |

## 4. Framework mapping (NIST AI RMF)
**Govern:** owner, policy, approval. **Map:** use case, data and affected people (sections 1 to 3 of the pack). **Measure:** bias, accuracy and drift testing. **Manage:** override process, monitoring, suspension criteria.

## 5. Open items
EU AI Act classification confirmed; Article 22 position; test plan and thresholds; vendor location and training restrictions; retention for scores and logs.

*Independent portfolio exercise based on a fictional use case.*
