# Sanad

**Sanad** is a provider-to-provider tele-expertise initiative designed to connect doctors working inside Sudan with Sudanese specialist consultants based abroad.

The project aims to create a structured, secure, and accountable way for local doctors to access specialist advice, particularly in settings where conflict, workforce displacement, and limited connectivity have reduced access to senior clinical expertise.

> **Current stage:** Evidence collection, expert review, decision closure, and pilot preparation.  
> **Working model:** Doctor-to-doctor tele-expertise, not direct-to-patient telemedicine.

## Current Phase: Evidence and Decision Closure

The pre-implementation documentation baseline is substantially established.

The project is now using that baseline to collect real evidence and close the decisions that cannot be responsibly made from desk assumptions alone, including:

- pilot specialty;
- partner facilities;
- platform / vendor choice;
- legal and regulatory feasibility;
- hosting and data residency;
- consultant eligibility and indemnity;
- evaluation and research governance.

A central **Expert Review Register** identifies which decisions require clinical, legal, privacy, security, research, commercial, finance, insurance, infrastructure, UX, or health-informatics expertise. The Project Manager is expected to engage those specialists before the corresponding decision gate is closed.

## Why Sanad

Sudan's health system has experienced significant disruption, including the loss and displacement of specialist healthcare professionals. At the same time, many experienced Sudanese consultants now practise abroad and remain willing to support colleagues inside Sudan.

Remote clinical support already happens through phone calls and messaging applications, but these interactions are often informal, unpaid, undocumented, difficult to audit, and difficult to evaluate.

Sanad aims to provide a more structured model.

## Intended Service

A typical case is expected to follow this pathway:

1. A verified doctor inside Sudan submits a structured clinical case.
2. The case is routed to an appropriate specialist consultant.
3. The consultant reviews the information and provides documented advice.
4. The local treating doctor decides how to manage the patient.
5. The local doctor records the relevant outcome.
6. The case is closed and may be included in clinical quality review and evaluation.

The local treating doctor remains responsible for the patient's care and clinical decisions.

## Initial Pilot

The current concept proposes a limited pilot with:

- one medical specialty;
- one Sudanese state;
- approximately 3 to 5 participating health facilities;
- approximately 20 to 40 doctors inside Sudan;
- approximately 10 to 20 specialist consultants abroad;
- approximately 300 to 500 clinical cases;
- six months of live service after an initial preparation period.

The specialty, location, participating organisations, hosting model, and final technology platform are not yet finalised.

## What Sanad Is Intended to Support

- Structured clinical case submission
- Specialist case review
- Written clinical advice
- Routine and priority workflows
- Secure exchange of relevant clinical images and results
- Case follow-up and outcome documentation
- Clinical governance and audit
- Incident and safety reporting
- Second opinions
- Virtual multidisciplinary team discussions
- Case-based clinical teaching
- Evaluation and research
- Evidence that may support future policy and telemedicine regulation

## What Sanad Is Not, at This Stage

The initial phase is not intended to provide:

- direct doctor-to-patient telemedicine;
- emergency medical services;
- guaranteed 24/7 specialist cover;
- direct prescribing by remote consultants;
- patient billing or payment services.

## Core Principles

### Patient safety
Clinical safety takes priority over speed, convenience, or scale.

### Respect for local clinical responsibility
Doctors working directly with patients understand the local context, available resources, and patient circumstances. Sanad supports their judgement rather than replacing it.

### Confidentiality
The service should collect only information necessary for safe clinical support and evaluation.

### Accountability
Relevant advice, decisions, incidents, and system actions should be appropriately documented and reviewable.

### Neutrality
The project is intended to support healthcare professionals regardless of political or geographic affiliation.

### Evidence
The project should measure its impact and use evidence to improve the service and inform future decisions.

## Clinical Governance

Clinical governance is a core part of the service model, not an optional feature. The planned model includes:

- verification of participating doctors and consultants;
- standardised case templates;
- defined response expectations;
- clinical audit;
- incident reporting;
- complaints processes;
- second opinions;
- professional conduct requirements;
- patient consent;
- data minimisation;
- ongoing feedback and quality improvement.

Detailed governance requirements remain subject to review by appropriately qualified clinical, legal, and regulatory experts.

## Technology Approach

Technology is intended to support the clinical and operational model, not define it.

The system must be appropriate for environments where connectivity may be weak or intermittent. Important considerations include:

- mobile-first access;
- low-bandwidth operation;
- safe offline capability where appropriate;
- Arabic and English interfaces;
- role and context-based access;
- audit logs;
- clinical image and document handling;
- data protection;
- simple workflows that minimise burden on clinicians.

The repository currently contains a candidate custom-platform architecture and a formal **Build vs Buy vs Partner** assessment. These are working decisions, not final procurement or implementation commitments.

## Research and Evaluation

The pilot is intended to generate evidence, not only deliver individual consultations. Evaluation may include:

- number and type of cases;
- response times;
- changes in clinical management;
- referrals avoided where measurable;
- safety events and near misses;
- user satisfaction;
- consultant retention;
- training activity;
- cost per case;
- operational feasibility;
- policy implications.

Any research or publication activity must be subject to appropriate ethics, consent, privacy, and governance requirements.

## Key Stakeholders

Potential stakeholders include:

- doctors and health workers inside Sudan;
- Sudanese specialist consultants abroad;
- hospitals and health facilities;
- Sudan Medical Council;
- federal and state health authorities;
- Sudan Medical Specialization Board;
- professional medical associations;
- humanitarian organisations and NGOs;
- academic and research partners;
- legal and data protection advisers;
- technology partners;
- funders and donors.

## Repository Structure

The numbering reflects the project's **working lifecycle and dependency order**, not the date a folder was created.

```text
docs/
├── START_HERE.md
├── 00-governance/
│   └── Governance, scope, stakeholders, risks, experts, project control
├── 01-product/
│   └── Product purpose, scope, and product requirements
├── 02-requirements/
│   └── System requirements, access control, measurable NFRs
├── 03-clinical/
│   └── Clinical workflow, safety, verification, specialty design
├── 04-research/
│   └── Source evidence, field evidence, evaluation, questionnaires
├── 05-architecture/
│   └── C4, domain model, data architecture, integration principles
├── 06-security/
│   └── Privacy, threat model, security architecture, data protection
├── 07-decisions/
│   └── ADRs, Build/Buy/Partner, vendor/platform evidence and decisions
├── 08-contracts/
│   └── Technical contracts and legal agreement requirements
├── 09-delivery/
│   └── Roadmap, backlog, UAT, stage gates, readiness, launch governance
├── 10-engineering/
│   └── Engineering standards, implementation playbook, testing, CI/CD
└── 11-operations/
    └── Monitoring, support, backup/DR, incident response, live operations
```

See [the documentation index](docs/README.md) for direct links to all current project documents.

## Documentation Map

| Layer | Purpose | Open |
|---|---|---|
| 00 Governance | Project control, stakeholders, experts, risks, scope, decisions | [Open folder](docs/00-governance/) |
| 01 Product | Product purpose, scope, and PRD | [Open folder](docs/01-product/) |
| 02 Requirements | SRS, access model, functional and non-functional requirements | [Open folder](docs/02-requirements/) |
| 03 Clinical | Clinical workflow, safety, professional verification, specialty design | [Open folder](docs/03-clinical/) |
| 04 Research & Evidence | Source material, desk research, field evidence, evaluation | [Open folder](docs/04-research/) |
| 05 Architecture | C4, domain, data, and integration architecture | [Open folder](docs/05-architecture/) |
| 06 Security & Privacy | Privacy, threat model, security architecture, data protection | [Open folder](docs/06-security/) |
| 07 Decisions | ADRs, platform/vendor evidence, Build/Buy/Partner decisions | [Open folder](docs/07-decisions/) |
| 08 Contracts | Technical contracts and legal agreement requirements | [Open folder](docs/08-contracts/) |
| 09 Delivery | Roadmap, backlog, stage gates, UAT, readiness, launch governance | [Open folder](docs/09-delivery/) |
| 10 Engineering & Implementation | Build, test, secure, configure, deploy, hand over | [Open folder](docs/10-engineering/) |
| 11 Operations | Monitor, support, recover, and operate the live service | [Open folder](docs/11-operations/) |

For the complete clickable document-level index, open **[docs/README.md](docs/README.md)**.

## How to Navigate This Repository

If you are new to the project, do **not** start by opening random technical documents.

Start with:

1. [README](README.md)
2. [Documentation Manual / Start Here](docs/START_HERE.md)
3. [Project Status](docs/00-governance/PROJECT_STATUS.md)
4. [Scope Guardrails](docs/00-governance/SCOPE_GUARDRAILS.md)
5. Your role-specific reading path defined in `docs/START_HERE.md`

The documentation manual explains:

- what every folder is for;
- which documents matter to each profession;
- where a clinician, lawyer, privacy specialist, researcher, engineer, or project manager should start;
- how documents move from Draft to Approved;
- how expert reviews are requested;
- how decisions are recorded;
- how documentation leads into implementation and pilot operations.

## Current Documentation

The repository now includes working drafts for:

- Product Requirements Document (PRD)
- Software Requirements Specification (SRS)
- Clinical Workflow Specification
- Clinical Safety Hazard Log
- Access Control Matrix
- Non-Functional Requirements Catalog
- C4 Architecture
- Domain Model
- Data Architecture
- API and Integration Principles
- Data Classification and Privacy Requirements
- Threat Model
- Security Architecture
- Architecture Decision Records
- Engineering Standards
- Test Strategy
- CI/CD Strategy
- Observability and Monitoring
- Backup and Disaster Recovery
- Security Incident Response
- MVP Scope and Delivery Plan
- Product and Technical Roadmap
- Requirements Traceability Matrix
- Multidisciplinary Documentation Manual / Start Here
- Stakeholder Register and Engagement Matrix
- Internal and External Factors Analysis
- Engineering & Implementation Playbook

## Why This Documentation-First Method

Sanad is not only a software product. It combines clinical practice, public health, cross-border professional work, sensitive health data, low-connectivity operations, research/evaluation, and multiple organisations.

For that reason, the project is being developed through a documentation-first and evidence-driven method before major implementation commitments are made.

The purpose is to:

- keep the clinical problem and service model ahead of technology choices;
- separate source facts from assumptions and engineering proposals;
- expose legal, clinical, privacy, security, and operational dependencies early;
- give specialists clear points at which their expertise is required;
- make important decisions traceable;
- reduce rework after vendor/platform selection;
- preserve an exit path if a vendor or architectural choice proves unsuitable;
- create a foundation that can mature beyond the pilot without rebuilding governance from scratch.

The expected result is not “more documentation.” The expected result is a safer and more sustainable pilot in which product, clinical, technical, legal, and operational decisions can be explained and tested.

## Expert Involvement

The core team does not approve specialist matters outside its competence.

Documents that require specialist judgement are marked **Required Expert Review** and linked to a central Expert Review Register.

Examples include:

- clinical workflow and specialty selection;
- medical liability and consent;
- professional eligibility and indemnity;
- privacy and cross-border data processing;
- security architecture and penetration testing;
- evaluation methodology and research ethics;
- sanctions, payments, insurance, and tax;
- health-informatics standards;
- accessibility and low-resource usability.

The Project Manager is responsible for engaging the required expert before the relevant decision gate is closed.

## Documentation Discipline

The founding prospectus is preserved separately from later product and engineering interpretation.

Working documents identify whether statements are:

- source-derived;
- proposed;
- approved;
- engineering recommendations;
- clinical/legal dependencies;
- or still TBD.

## Project Origin and Documentation Roles

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**

- Email: [elafsabri515@gmail.com](mailto:elafsabri515@gmail.com)
- LinkedIn: [linkedin.com/in/elaf-sabri-khalil-68097024a](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

The repository and the documentation layers were created from the founding materials supplied by Dr. Elaf.

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**

- Email: [Fabdalla782@gmail.com](mailto:Fabdalla782@gmail.com)
- LinkedIn: [linkedin.com/in/alfatihabdalla](https://www.linkedin.com/in/alfatihabdalla)
- GitHub: [github.com/fatihg80](https://github.com/fatihg80)

Alfatih Abdalla participated in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His role in this repository is limited to structuring the repository, defining its documentation layers and methodology, and providing product/technical analysis based on Dr. Elaf's source materials. He is **not represented as the founder or owner of Sanad**.

See [AUTHORS.md](AUTHORS.md) and [NOTICE.md](NOTICE.md) for the attribution boundary. Contributors should also follow [CONTRIBUTING.md](CONTRIBUTING.md).

## Important Notice

This repository contains working project materials.

Nothing in this repository should be interpreted as final clinical guidance, legal advice, regulatory approval, or confirmation that the service is ready for clinical deployment.

Clinical, legal, regulatory, data protection, professional, and patient-safety requirements must be reviewed and approved by appropriately qualified parties before any live clinical service begins.

## Status

**Project:** Sanad  
**Primary model:** Provider-to-provider tele-expertise  
**Geographic focus:** Sudan  
**Stage:** Evidence collection / decision closure / pilot preparation  
**Repository purpose:** Product, clinical, architecture, governance, security, engineering, operations, research, and delivery documentation

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. This attribution does **not** represent him as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
