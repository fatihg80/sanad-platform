# Expert Review Register

**Version:** 0.1  
**Status:** Active

## Purpose

Identify where Sanad requires qualified specialist input so the Project Manager can deliberately engage the correct expert before a decision is treated as approved.

## Review Classes

- **Clinical Expert Review**: specialist physician, clinical governance lead, or specialty lead.
- **Legal / Regulatory Review**: qualified counsel familiar with applicable jurisdictions and healthcare regulation.
- **Privacy / Data Protection Review**: privacy counsel, DPO, or equivalent specialist.
- **Security Review**: security architect, application-security specialist, or independent assessor.
- **Public Health / Evaluation Review**: public-health specialist, epidemiologist, health-services researcher, or biostatistician.
- **Finance / Tax Review**: qualified accountant, tax adviser, or finance lead.
- **Sanctions / Compliance Review**: sanctions, AML, or compliance specialist.
- **Insurance / Indemnity Review**: medical indemnity or insurance specialist.
- **Procurement / Commercial Review**: procurement or commercial-contract specialist.
- **UX / Accessibility Review**: product/UX specialist with mobile, accessibility, and low-resource experience.
- **Infrastructure / SRE Review**: cloud/platform architect or SRE.
- **Clinical Informatics Review**: health-informatics specialist for coding, interoperability, and clinical data semantics.
- **Research Ethics Review**: ethics committee/IRB or qualified research-governance adviser.

## Mandatory Expert Review Map

| ID | Decision / Artifact | Required Expert | Why Expert Input Is Required | Blocking Point |
|---|---|---|---|---|
| ER-01 | Pilot specialty selection | Clinical Governance + Specialty Experts + Public Health | Determines clinical suitability, case mix, safety, and measurable outcomes | Before specialty approval |
| ER-02 | Specialty-specific case template | Specialty Expert + Clinical Governance | Determines minimum safe clinical information | Before pilot UAT |
| ER-03 | Priority / emergency boundary | Clinical Governance + Legal | Patient-safety and liability consequences | Before live clinical use |
| ER-04 | Consultant eligibility | Clinical Governance + Regulator/Legal + Indemnity Expert | Cross-border professional-practice eligibility | Before consultant activation |
| ER-05 | Clinical responsibility / liability model | Healthcare Legal Counsel + Clinical Governance | Cannot be inferred from software workflow | Before agreements/go-live |
| ER-06 | Patient consent model | Legal + Clinical Governance + Privacy | Consent requirements vary by jurisdiction and data use | Before live data collection |
| ER-07 | Data controller / processor roles | Privacy Counsel / DPO | Determines contractual and regulatory obligations | Before vendor/facility DPA |
| ER-08 | Hosting / data residency | Privacy + Legal + Security + Infrastructure | Cross-border transfer, support access, and security implications | Before production architecture |
| ER-09 | DPIA | Privacy/DPO + Security + Clinical Governance | High-risk health-data processing | Before production where required |
| ER-10 | Retention schedule | Legal + Clinical Governance + Privacy | Clinical/legal record obligations | Before production policy approval |
| ER-11 | Threat model / security architecture | Security Architect | Independent challenge of security assumptions | Before implementation freeze |
| ER-12 | Penetration/security assessment | Independent Security Specialist | Validate implementation, not only design | Before go-live |
| ER-13 | Offline clinical-data model | Security + UX + Clinical + Infrastructure | Balances usability, safety, device-loss, sync risk | Before offline scope approval |
| ER-14 | Diagnostic image processing | Specialty Expert / Radiology or relevant clinician + Security/Tech | Compression/transformation can change clinical meaning | Before image transforms |
| ER-15 | Clinical coding / interoperability | Clinical Informatics Expert | Prevents incorrect semantic mapping | Before coding/FHIR commitments |
| ER-16 | Evaluation protocol | Public Health / Research + Clinical | Methodology, bias, outcome validity | Before pilot data collection |
| ER-17 | Minimum evaluation dataset | Research + Privacy + Clinical | Balance evidence with minimisation | Before analytics/reporting implementation |
| ER-18 | Ethics determination | Research Ethics / IRB | Determines research vs service-evaluation obligations | Before publication-oriented data collection |
| ER-19 | Partner/facility selection | Clinical + Operations + Compliance | Safety, legitimacy, neutrality, local capacity | Before facility onboarding |
| ER-20 | Sanctions/payment process | Sanctions/Compliance + Finance | Cross-border payments and restricted entities | Before payments/contracts |
| ER-21 | Entity structure and tax | Legal + Tax/Accounting | Organisational liability and funding implications | Before incorporation/funding contracts |
| ER-22 | Consultant/facility/vendor agreements | Legal Counsel | Binding allocation of rights and liabilities | Before signature |
| ER-23 | Insurance/indemnity | Insurance/Indemnity Specialist + Legal | Coverage may vary by activity/jurisdiction | Before live clinical activity |
| ER-24 | Vendor security/privacy due diligence | Security + Privacy + Procurement | Vendor claims require validation | Before vendor selection |
| ER-25 | Build vs Buy vs Partner final decision | Technology + Clinical + Security + Privacy + Commercial | Cross-functional strategic decision | Before implementation commitment |
| ER-26 | Accessibility/mobile UX | UX/Accessibility + Local Users | Adoption and safe usability on low-cost devices | Before pilot UAT closure |
| ER-27 | Production SLO/RTO/RPO | Infrastructure/SRE + Operations + Clinical | Recovery/availability targets must match service model | Before production sign-off |

## Project Manager Action Rule

For every item marked as expert-dependent, the Project Manager should:

1. identify the named expert role;
2. schedule review before the blocking point;
3. provide the relevant document and decision questions;
4. record written advice or approval;
5. update affected documents;
6. link the resulting decision in the Decision Register;
7. record review date and next review trigger.

## Evidence Standard

A statement such as “reviewed with legal” is insufficient for material decisions.

Prefer a traceable record containing:

- expert name/role or organisation;
- jurisdiction/domain;
- date;
- question reviewed;
- advice/decision summary;
- affected document;
- follow-up action;
- approval/reference where appropriate.

## Scope Guardrail

Expert involvement should close real project decisions. It should not be used to expand the pilot beyond its approved scope.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
