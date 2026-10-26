# Executive Summary

**Independent simulation.** Fictional insurer; no real personal data. Not legal advice.

## The question
Example Mutual Insurance DAC (fictional, about 200,000 policyholders) wants an AI tool to score motor and home claims and prioritise them for handlers. Can this be done in line with GDPR, and what should the insurer put in place first?

## What I did
1. Defined the use case, data subjects and data sources.
2. Built a data inventory of 18 items (D01 to D18), including health data, fraud flags and AI outputs.
3. Mapped the data flow and its controls with a diagram.
4. Wrote a six-activity record of processing (GDPR Article 30).
5. Completed a Data Protection Impact Assessment (Article 35) with eight risks, measures and residual risk.
6. Wrote an AI governance note covering the EU AI Act, oversight and monitoring.

## Key findings
- **A DPIA is required.** The tool profiles people, handles health data and a fraud flag, and uses a third-party AI service at scale.
- **Highest risk:** unauthorised access to claimant and health data (score 12, High). With encryption, role-based access, MFA and logging it falls to Medium (6).
- **No risk stays High** after the proposed measures, but two Medium risks (data access and vendor processing) need ongoing monitoring.
- **Four items must be verified before use:** the Article 9 condition for health data, the Article 22 position on automated decisions, the AI provider's data location and training restrictions, and retention periods for scores and logs.
- **EU AI Act:** probably not high-risk under Annex III, but the classification must be checked and good-practice controls applied anyway.

## Recommendation
Proceed only with human review of every recommendation, health data excluded from scoring unless justified, an Article 28 contract with no model training on claim data, and bias and accuracy testing before go-live.

## Skills shown
Data inventory, ROPA, DPIA, risk scoring, control design, GDPR and EU AI Act analysis, clear written deliverables.

## Limits
All organisations, systems and figures are fictional. I have not verified every legal point; items marked [verify] need checking against current law and DPC guidance.
