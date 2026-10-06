# MVP Scope and Delivery Plan

**Version:** 0.1  
**Status:** Draft  
**Assumption:** Applies if the Build or substantial-custom-build option is selected.

## 1. MVP Goal

Build the smallest safe, usable platform capable of validating the Sanad provider-to-provider tele-expertise operating model.

The MVP is not the smallest amount of code. It is the smallest product that can responsibly support the pilot.

## 2. MVP Capabilities

### Identity and verification
- invite/register;
- professional profile;
- verification workflow;
- login;
- MFA for privileged roles.

### Role and contextual access
- local doctor;
- consultant;
- coordinator;
- specialty lead;
- governance lead;
- administrator.

### Case workflow
- draft;
- structured template;
- consent confirmation;
- submit;
- assignment;
- review;
- request information;
- final advice;
- outcome;
- closure.

### Attachments
- secure upload;
- protected retrieval;
- file validation;
- weak-network retry.

### Routing
- manual/coordinator-assisted;
- consultant eligibility;
- reassignment.

### Governance
- incident report;
- second opinion;
- basic audit;
- complaints tracking at minimum workable level.

### Operational
- notifications;
- basic dashboards;
- audit trail;
- monitoring.

### Connectivity
- resilient mobile UX;
- safe offline draft capability if validated;
- retry/idempotency.

## 3. Explicit MVP Exclusions

Unless discovery changes the requirement:

- patient portal;
- direct patient consultation;
- emergency service;
- native video platform;
- advanced AI decision support;
- automated diagnosis;
- billing;
- complex microservices;
- full national interoperability;
- full offline historical record;
- sophisticated automated routing.

## 4. Delivery Slices

### Slice 0: Foundation
- repository/application skeleton;
- environments;
- CI/CD;
- authentication baseline;
- observability;
- security baseline.

### Slice 1: Professional Identity
- accounts;
- profiles;
- verification;
- roles/policies.

### Slice 2: Case Submission
- templates;
- drafts;
- consent confirmation;
- attachments;
- submission.

### Slice 3: Routing and Review
- coordinator queue;
- assignment;
- consultant case access;
- request for information.

### Slice 4: Advice and Outcome
- final advice;
- addendum;
- outcome;
- closure.

### Slice 5: Governance
- audit;
- incident;
- second opinion;
- complaint basics.

### Slice 6: Connectivity and Hardening
- offline draft;
- retries;
- low-bandwidth optimisation;
- security testing;
- performance.

### Slice 7: Pilot Readiness
- training;
- runbooks;
- dashboards;
- backup restore;
- incident exercise;
- acceptance testing.

## 5. Exit Criteria Before Pilot

- clinical workflow signed off;
- legal/regulatory blockers resolved sufficiently;
- privacy/data-flow review complete;
- permissions matrix approved;
- security assessment complete;
- backup restore successful;
- critical tests passing;
- pilot users trained;
- support and incident contacts defined;
- fallback communication procedure approved.

## 6. Post-MVP Evolution

### Pilot+
- availability-aware routing;
- richer SLA escalation;
- stronger offline;
- enhanced analytics;
- improved governance dashboards.

### Expansion
- multiple specialties;
- configurable templates;
- additional states/facilities;
- institutional integration;
- identity federation.

### Mature platform
- advanced interoperability;
- policy engine;
- SIEM integration;
- scalable analytics;
- stronger multi-region resilience where required.

## 7. Guardrail

Do not add features because they sound mature.

Add them because a validated clinical, operational, regulatory, security, or scale need exists.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
