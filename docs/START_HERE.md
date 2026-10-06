# Sanad Documentation Manual: Start Here

**Version:** 1.0  
**Status:** Active  
**Audience:** All project participants

## 1. Why This Manual Exists

Sanad is a multidisciplinary project.

People using this repository may come from:

- medicine;
- public health;
- law and regulation;
- data protection;
- cybersecurity;
- software engineering;
- product management;
- research and evaluation;
- operations;
- finance;
- procurement;
- partner organisations.

This repository is therefore organised so that no single profession is expected to understand every document before contributing.

The purpose of this manual is to explain:

1. what each folder is for;
2. which documents matter to each role;
3. where a person should start;
4. how a document moves from Draft to Approved;
5. when expert review is required;
6. how decisions are recorded;
7. how the documentation connects to implementation and pilot operations.

---

# 2. First Rule: Do Not Read the Repository Like a Book

You do not need to read every document from top to bottom.

Use this path:

```text
README.md
   ↓
docs/START_HERE.md
   ↓
docs/00-governance/PROJECT_STATUS.md
   ↓
Your role-specific documents
   ↓
Relevant open decisions / expert reviews
   ↓
Evidence / review
   ↓
Approved decision
   ↓
Implementation / pilot
```

---

# 3. Recommended Starting Path for Everyone

## Step 1: Understand the project

Read:

1. `README.md`
2. `docs/START_HERE.md`
3. `docs/00-governance/PROJECT_STATUS.md`
4. `docs/00-governance/SCOPE_GUARDRAILS.md`
5. `docs/00-governance/GLOSSARY.md`

After these documents, a contributor should understand:

- what Sanad is;
- what it is not;
- the current project phase;
- the pilot boundary;
- the main terminology.

## Step 2: Understand your role

Read:

- `RACI_MATRIX.md`
- `STAKEHOLDER_REGISTER.md`
- `STAKEHOLDER_ENGAGEMENT_MATRIX.md`
- `EXPERT_REVIEW_REGISTER.md`

This shows:

- where you are Responsible;
- where you are Accountable;
- where you are Consulted;
- where your approval is required.

## Step 3: Review your specialist area

Use the role paths below.

## Step 4: Review open decisions

Read:

- `DECISION_REGISTER.md`
- `ISSUE_REGISTER.md`
- `DEPENDENCY_REGISTER.md`
- `ASSUMPTIONS_REGISTER.md`
- `RISK_REGISTER.md`

Do not assume an item is approved because it appears in a document.

## Step 5: Provide evidence or review

Use:

- `EXPERT_REVIEW_REQUEST_TEMPLATE.md`
- relevant scorecard/questionnaire;
- evidence collection documents.

## Step 6: Record the outcome

A material review should update:

- the owning document;
- Decision Register;
- Risk/Issue/Dependency register where relevant;
- Changelog;
- ADR where the decision is architectural.

---

# 4. Folder-by-Folder Guide

## 00-governance

### Purpose

Controls how the project is managed and how decisions are made.

### Contains

- project status;
- scope;
- RACI;
- stakeholders;
- risks;
- assumptions;
- dependencies;
- issues;
- decisions;
- expert reviews;
- quality;
- communication;
- change governance.

### Who should use it

Everyone, especially:

- Project Manager;
- Project Lead;
- Clinical Governance;
- Legal;
- Technology Lead;
- Operations Lead.

### Key rule

This folder answers:

> Who decides, who reviews, what is open, what is blocked, and what is the current state?

---

## 01-product

### Purpose

Explains what product/service Sanad is trying to create and why.

### Main document

- `PRD.md`

### Who should use it

- Product;
- Clinical;
- Public Health;
- Founding Team;
- Technology;
- Operations.

### Key rule

Product documents define **what and why**, not detailed implementation.

---

## 02-requirements

### Purpose

Turns product intent into explicit system requirements.

### Contains

- SRS;
- functional/non-functional requirements;
- access-control matrix;
- measurable NFRs.

### Who should use it

- Technology;
- QA;
- Security;
- Product;
- Clinical reviewers.

### Key rule

A feature should not be built merely because it was discussed verbally. It should trace back to a requirement.

---

## 03-clinical

### Purpose

Defines the clinical service workflow and safety boundaries.

### Contains

- clinical workflow;
- case template;
- professional verification;
- response/escalation model;
- clinical safety hazard log;
- specialty-selection framework.

### Who should use it

- Clinical Governance;
- Specialty Leads;
- Local Doctors;
- Consultants;
- Public Health;
- Product;
- Legal where clinical responsibility is affected.

### Key rule

Technology cannot approve clinical decisions.

---

## 04-architecture

### Purpose

Describes how the system may be structured technically.

### Contains

- C4 architecture;
- domain model;
- data architecture;
- API/integration principles.

### Who should use it

- Software Architects;
- Engineers;
- Security;
- DevOps/SRE;
- Technical Product Leads.

### Key rule

Architecture remains Proposed until the platform and hosting decisions are closed.

---

## 05-security

### Purpose

Protects patients, clinicians, data, systems, and operational safety.

### Contains

- privacy requirements;
- threat model;
- security architecture;
- data-flow inventory;
- DPIA template;
- retention;
- audit events;
- hosting/data residency.

### Who should use it

- Security;
- Privacy/DPO;
- Legal;
- Technology;
- Clinical Governance.

### Key rule

Security and privacy are design constraints, not tasks left until deployment.

---

## 06-decisions

### Purpose

Stores important product/technical decision evidence and ADRs.

### Contains

- Build vs Buy vs Partner;
- ADRs;
- platform evidence;
- vendor evaluation;
- vendor demonstration script.

### Who should use it

- Project Lead;
- Technology Lead;
- Clinical Governance;
- Security;
- Privacy;
- Procurement.

### Key rule

A decision should record alternatives and consequences, not only the final choice.

---

## 07-research

### Purpose

Stores evidence, literature, source analysis, pilot evaluation, and field-research instruments.

### Contains

- founding source notes;
- platform evidence;
- specialty evidence;
- evaluation protocol;
- minimum dataset;
- questionnaires.

### Who should use it

- Public Health;
- Researchers;
- Clinical;
- Project Manager;
- Product.

### Key rule

Evidence here informs decisions. It does not automatically become an approved requirement.

---

## 08-engineering

### Purpose

Defines how software should be built and maintained.

### Contains

- engineering standards;
- test strategy;
- CI/CD;
- environment strategy;
- configuration management.

### Who should use it

- Engineering;
- QA;
- DevOps;
- Security;
- Technical Lead.

### Key rule

This folder defines engineering discipline, not business scope.

---

## 09-operations

### Purpose

Defines how the live service is operated.

### Contains

- monitoring;
- backup/DR;
- incident response;
- notifications;
- support;
- training;
- release management;
- pilot runbook.

### Who should use it

- Operations;
- Technology;
- Clinical Governance;
- Support;
- Project Manager.

### Key rule

A technically working product is not operationally ready until these processes exist.

---

## 10-delivery

### Purpose

Turns plans into a controlled route toward the pilot.

### Contains

- roadmap;
- MVP plan;
- backlog;
- UAT;
- readiness;
- scorecards;
- traceability;
- launch governance.

### Who should use it

- Project Manager;
- Product;
- Technology;
- Clinical;
- Operations.

### Key rule

This folder answers:

> What must happen before we can safely move to the next stage?

---

## 11-contracts

### Purpose

Defines technical interface contracts and legal agreement requirements.

### Contains

- API contracts;
- event contracts;
- data contracts;
- service contracts;
- legal agreement requirements.

### Who should use it

- Engineering;
- Integration Teams;
- Legal;
- Procurement;
- Privacy;
- Vendors.

### Key rule

Technical contracts can be designed by engineering.

Binding legal contracts require qualified legal counsel.

---

## 12-implementation

### Purpose

Provides the execution map after the major decisions are approved.

### Contains

- implementation lifecycle;
- development execution plan;
- testing and verification execution;
- security assurance execution;
- deployment and release execution;
- production-readiness handover.

### Who should use it

- Engineering;
- QA;
- Security;
- DevOps/SRE;
- Project Manager;
- Product.

### Key rule

This folder does not duplicate detailed standards from 08/09/10.

It tells the delivery team **in what order to execute them**.

---

# 5. Role-Specific Reading Paths

## Project Manager

Read first:

1. README
2. Project Status
3. Scope Guardrails
4. RACI
5. Stakeholder Register
6. Expert Review Register
7. Decision / Risk / Issue / Dependency Registers
8. Roadmap
9. Implementation Lifecycle
10. Go-Live Checklist

Primary responsibility:

- orchestrate;
- engage experts;
- close dependencies;
- preserve scope;
- maintain decision traceability.

---

## Clinical Expert / Specialty Lead

Read:

1. README
2. Scope Guardrails
3. PRD
4. Clinical Workflow
5. Case Template
6. Clinical Safety Hazard Log
7. Specialty Selection Framework
8. Evaluation Protocol
9. Required Expert Review items

Do not approve:

- legal interpretations;
- security architecture;
- infrastructure decisions

unless specifically qualified.

---

## Legal / Regulatory Expert

Read:

1. README
2. Scope Guardrails
3. Clinical Workflow
4. Legal and Regulatory Question Register
5. Data Flow Inventory
6. Privacy Requirements
7. Hosting/Data Residency Options
8. Legal Agreement Requirements
9. Expert Review Register

Expected output:

- written advice;
- jurisdiction;
- conditions;
- blockers;
- agreement requirements.

---

## Privacy / DPO

Read:

1. Data Classification and Privacy Requirements
2. Data Flow Inventory
3. DPIA Template
4. Retention Schedule
5. Hosting/Data Residency
6. Access Control Matrix
7. Threat Model
8. Vendor Evidence

---

## Security Expert

Read:

1. Threat Model
2. Security Architecture
3. Access Control Matrix
4. Offline Strategy ADR
5. Data Flow Inventory
6. Engineering Standards
7. CI/CD
8. Security Assurance Execution Plan

---

## Software Engineer / Architect

Read:

1. PRD
2. SRS
3. Clinical Workflow
4. Domain Model
5. C4 Architecture
6. Data Architecture
7. ADRs
8. Contracts
9. Engineering Standards
10. Implementation folder

---

## Public Health / Research / Evaluation

Read:

1. PRD
2. Pilot Evaluation Protocol
3. Minimum Evaluation Dataset
4. Specialty Evidence Review
5. Specialty Questionnaire
6. Risk / Stakeholder documents
7. Ethics-related expert review items

---

## Operations / Support

Read:

1. Clinical Workflow
2. Response/Escalation Model
3. Notification Policy
4. Operations Runbook
5. Support Model
6. Training Plan
7. Backup/DR
8. Incident Response
9. Go-Live Checklist

---

# 6. Document Lifecycle

```text
Need identified
   ↓
Draft created
   ↓
Relevant disciplines review
   ↓
Required Expert Review if applicable
   ↓
Evidence / changes
   ↓
Proposed decision
   ↓
Approval by accountable role
   ↓
Document status updated
   ↓
Implementation / operation
   ↓
Review after evidence or incident
   ↓
Update / Supersede / Retire
```

---

# 7. How to Comment or Propose a Change

When proposing a material change:

1. identify the document;
2. identify the exact section;
3. state the issue;
4. provide evidence/reason;
5. identify affected documents;
6. identify expert review if required;
7. update Decision/Risk/Issue register where necessary.

Avoid undocumented decisions in:

- WhatsApp;
- private email;
- meetings;
- verbal discussions.

A discussion may happen anywhere, but the resulting decision should return to the repository.

---

# 8. How to Know Whether You Can Approve Something

Ask:

1. Is this within my professional competence?
2. Am I Accountable or only Consulted?
3. Is this marked Required Expert Review?
4. Does a regulator/legal/clinical authority need to approve it?
5. Is evidence still missing?

If uncertain, leave the item **Open / Proposed** and escalate through the Project Manager.

---

# 9. When Implementation Begins

The execution order is:

```text
Approved scope and requirements
        ↓
Closed architecture/platform decisions
        ↓
Implementation planning
        ↓
Development
        ↓
Automated testing
        ↓
Security verification
        ↓
Staging / UAT
        ↓
Clinical + operational acceptance
        ↓
Deployment readiness
        ↓
Pilot go-live
        ↓
Monitoring / evaluation
        ↓
Evidence review
        ↓
Continue / Modify / Pause / Stop
```

Detailed execution guidance is under:

`docs/12-implementation/`

---

# 10. The Most Important Rule

Do not confuse:

- **written** with **approved**;
- **technical possibility** with **clinical safety**;
- **clinical preference** with **legal permission**;
- **vendor claim** with **verified evidence**;
- **pilot success** with **number of cases processed**.

Sanad is intentionally designed so these distinctions remain visible.
