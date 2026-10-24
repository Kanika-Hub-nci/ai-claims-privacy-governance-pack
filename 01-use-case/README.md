# Use Case: AI Claims Pre-Assessment

**Independent simulation.** Fictional organisation; no real personal data is used.

## 1. Organisation

Example Mutual Insurance DAC is a fictional Irish motor and home insurer with approximately 200,000 policyholders and a centralised claims-handling team. These figures are invented for this exercise.

## 2. The AI tool

The AI claims pre-assessment tool analyses incoming motor and home insurance claims and assigns a preliminary risk score and handling priority. It provides recommendations to claims handlers, who review the available evidence and make the final claims decisions.

## 3. Purpose

The tool is intended to help the insurer process routine claims more efficiently and identify claims that may require additional evidence, specialist review or fraud investigation. Its purpose is to support human decision-making, not automatically approve or reject claims.

## 4. Data subjects

- Policyholders submitting insurance claims.
- Claimants who may not be the policyholder.
- Third parties involved in an incident, such as other drivers, passengers, witnesses or property owners.
- Individuals whose information appears in claim documents, photographs or correspondence.

## 5. Personal data used

The proposed tool may process:

- **Identification and contact details:** name, address, telephone number and email address.
- **Policy information:** policy number, policy type, coverage and policy status.
- **Claim details:** claim reference, date and location of incident, description of damage, claimed amount and supporting evidence.
- **Claims history:** previous claims, relevant claim outcomes and information needed to assess the current claim.
- **Photographs and documents:** vehicle damage, property damage, repair estimates, invoices and correspondence.
- **Potentially sensitive information:** injury reports or medical documents may contain health data, which is special-category personal data under GDPR Article 9.

The insurer should establish whether health data is genuinely necessary for each claim type and restrict access accordingly. Photographs and documents may also contain information about third parties, so unnecessary information should be removed or redacted where appropriate.

Information suggesting possible fraud must be handled carefully. A fraud risk score is not proof of wrongdoing, and information relating to criminal allegations or offences requires specific legal assessment.

## 6. Where the data comes from

The proposed data sources include:

- Customer claims submitted through the insurer's website or customer portal.
- Telephone claims reported to customer service or claims staff.
- Information entered by claims handlers into the claims management system.
- Photographs, repair estimates and invoices supplied by customers or third-party repair garages.
- Relevant policy and claims records already held by the insurer.
- Additional information obtained from authorised third parties where necessary and lawful.

The insurer should document the source of each data category and confirm that its collection and use are lawful and transparent.

## 7. Who sees the output

The AI-generated score, priority and supporting flags may be available to:

- Claims handlers responsible for reviewing the claim.
- Claims managers overseeing workload and escalations.
- Authorised fraud investigation staff, where further review is justified.
- Approved technical support personnel, where access is necessary and appropriately controlled.

Access should be role-based and limited to what each person needs. The insurer should log access to sensitive claim information and ensure that a low or high AI score is not treated as a definitive conclusion about a claimant.

## 8. Systems and storage

For this simulation, the proposed architecture consists of:

- A claims management system holding claim records and supporting documents.
- A secure cloud database for relevant processing data and AI outputs.
- A third-party AI model service that analyses the submitted information.
- Identity and access management, audit logging and security monitoring services.

The service providers are fictional and have not been selected. Before implementation, the insurer must identify each provider, establish whether it acts as a processor or controller for the relevant processing, review contractual safeguards and subprocessors, confirm data locations and international transfers, and establish whether claim data may be retained or used to train AI models.

## 9. Retention

**Assumption for this exercise:** Claim records are retained for up to seven years after claim closure, subject to the insurer's approved retention schedule and any applicable legal, regulatory or litigation requirements.

This period is illustrative, not a verified Irish legal requirement. The insurer should separately define retention periods for raw AI inputs, generated scores, audit logs, temporary files and vendor-held data. Data should be deleted or anonymised when no longer necessary, subject to lawful retention obligations and any documented legal hold.

## 10. Human oversight

The AI tool provides recommendations only and does not automatically approve, reject or settle claims. An authorised claims handler reviews the claim evidence, considers the AI output critically, and makes the final decision under the insurer's procedures.

Handlers should be able to override the recommendation, record their reasoning where appropriate, and escalate uncertain or potentially unfair outcomes. The insurer should test the tool for accuracy, bias and performance across relevant claim types and customer groups, monitor errors and complaints, and suspend or restrict use if serious problems emerge.

The insurer must also verify whether any other part of the workflow makes decisions solely by automated means and whether GDPR Article 22 or other legal requirements apply.

## 11. Assumptions and limits

- The organisation, policyholder count, systems, providers and retention periods are fictional.
- No real personal data or actual insurance claims are used.
- The tool is assumed to support, rather than replace, human claims decisions.
- The actual data flows, lawful basis, any Article 9 condition, vendor arrangements and AI regulatory classification have not been verified.
- A DPIA screening should be completed, with a full DPIA undertaken where required by GDPR Article 35.
- The insurer should assess necessity, proportionality, data minimisation, transparency, security, fairness and risks to claimants before deployment.
- The AI Act's applicability depends on the system's intended purpose and design; no definitive classification is made here.
- This is an independent learning exercise, not legal advice, a completed statutory DPIA or proof of GDPR or EU AI Act compliance.
