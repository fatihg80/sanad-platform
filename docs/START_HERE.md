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

The numbering expresses the primary working sequence. Some folders remain active throughout the project, especially Governance, Research, Security, Delivery, and Operations.

## 00-governance

**Purpose:** Controls project scope, ownership, stakeholders, risks, expert involvement, and decision governance.

**Use it to answer:** Who decides? What is open? What is blocked? Which expert must be involved?

## 01-product

**Purpose:** Defines what Sanad is trying to achieve and why.

**Main focus:** Product scope, users, value, and PRD.

## 02-requirements

**Purpose:** Converts product intent into explicit, testable system requirements.

**Main focus:** SRS, access control, functional requirements, measurable NFRs.

## 03-clinical

**Purpose:** Defines the clinical operating model and patient-safety boundaries.

**Main focus:** Workflow, templates, professional verification, safety hazards, priority/escalation.

**Rule:** Technology cannot approve clinical decisions.

## 04-research

**Purpose:** Holds the evidence that informs decisions.

**Main focus:** Founding source, literature, field questionnaires, facility/doctor/consultant evidence, evaluation protocol, minimum dataset.

**Rule:** Evidence informs a decision; it is not automatically an approved requirement.

## 05-architecture

**Purpose:** Translates approved needs into a coherent technical design.

**Main focus:** C4, domain model, data architecture, integration principles.

## 06-security

**Purpose:** Defines privacy, security, data-protection, and safety controls that constrain architecture and implementation.

**Main focus:** Threat model, security architecture, DPIA, retention, data flows, hosting/data residency.

## 07-decisions

**Purpose:** Records material choices and the evidence behind them.

**Main focus:** ADRs, Build vs Buy vs Partner, vendor/platform evidence and scoring.

**Rule:** Alternatives and consequences must remain visible.

## 08-contracts

**Purpose:** Defines boundaries before implementation and procurement commitments.

**Main focus:** API, event, data, and service contracts plus legal agreement requirements.

**Rule:** Engineering owns technical contracts; qualified counsel approves binding legal agreements.

## 09-delivery

**Purpose:** Converts approved scope and decisions into an executable project route.

**Main focus:** Roadmap, backlog, scorecards, traceability, UAT, stage gates, readiness, launch governance.

**Use it to answer:** What happens next, and what must be true before we advance?

## 10-engineering

**Purpose:** Defines how the selected solution is built or adapted, tested, secured, configured, deployed, and handed over.

**Main focus:** Engineering standards, implementation playbook, test strategy, CI/CD, environments, configuration.

## 11-operations

**Purpose:** Defines how the live service is monitored, supported, recovered, trained, and operated.

**Main focus:** Runbooks, monitoring, backup/DR, support, incident response, training, release operations.

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
9. Engineering & Implementation Playbook
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
8. Engineering & Implementation Playbook

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
10. Engineering & Implementation Playbook

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

Detailed execution guidance is in:

`docs/10-engineering/IMPLEMENTATION_PLAYBOOK.md`

---

# 10. The Most Important Rule

Do not confuse:

- **written** with **approved**;
- **technical possibility** with **clinical safety**;
- **clinical preference** with **legal permission**;
- **vendor claim** with **verified evidence**;
- **pilot success** with **number of cases processed**.

Sanad is intentionally designed so these distinctions remain visible.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
