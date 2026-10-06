# Platform Evidence Snapshot

**Version:** 0.1  
**Status:** Evidence collection in progress  
**Evidence date:** 2026-10-06

## Purpose

Record current source-backed evidence about shortlisted platform options before any Build / Buy / Partner decision is made.

This file distinguishes:

- **Confirmed by official public source**
- **Not yet verified**
- **Requires vendor demonstration**
- **Requires expert review**

## 1. Intelehealth

### Confirmed

Official Intelehealth material currently describes:

- a provider-to-provider telemedicine model connecting frontline health workers with remote doctors;
- an open-source telemedicine platform;
- suitability for low-resource settings;
- operation in low-bandwidth environments;
- customisation for partner projects;
- a web-based health-worker portal added in 2026;
- improved low-bandwidth WebRTC teleconsultation;
- FHIR R4-compliant data capture;
- improved application stability and initial sync performance.

### Official sources

- https://intelehealth.org/technology/
- https://intelehealth.org/all-the-upgrades-for-our-intelehealth-app/
- https://intelehealth.org/wp-content/uploads/2025/10/Annual-Report-2024-25.pdf

### Not Yet Verified for Sanad

- exact asynchronous doctor-to-doctor structured-case workflow;
- offline data model and local encryption;
- Arabic/RTL quality;
- professional verification model;
- case routing/reassignment;
- final advice/addendum semantics;
- incidents and clinical audit;
- hosting/data residency choices;
- administrator clinical-access model;
- total implementation/support cost;
- source-code/customisation ownership and exit terms.

### Current Position

**Priority discovery candidate.**

A Sanad-specific demonstration is required.

## 2. Community Health Toolkit

### Confirmed

Official CHT documentation states:

- applications are designed Offline-First;
- workflows can continue with intermittent or no internet;
- relevant data is cached locally using PouchDB and replicated with CouchDB;
- applications can support most languages;
- roles and permissions are configurable;
- workflows can use forms, tasks, schedules, messaging, and analytics;
- users can include community health workers, nurses, facility staff, managers, researchers, patients, and caregivers;
- offline users receive data they are authorised to access on their device, with advanced controls available over sync scope.

### Official sources

- https://docs.communityhealthtoolkit.org/technical-overview/concepts/offline-first/
- https://docs.communityhealthtoolkit.org/technical-overview/architecture/overview/
- https://docs.communityhealthtoolkit.org/building/users/
- https://docs.communityhealthtoolkit.org/building/

### Sanad Relevance

Strength:

- strongest confirmed offline-first evidence among current candidates.

Risk:

- locally synchronised clinical data creates device-loss, seizure, shared-device, and privacy concerns for Sanad.

### Not Yet Verified

- consultant tele-expertise workflow fit;
- Arabic/RTL quality in a Sanad prototype;
- consultant assignment/reassignment model;
- advice immutability/addenda;
- second opinion;
- governance workflows;
- professional verification;
- diagnostic-file behaviour;
- effort required to adapt the CHW/community-health design model.

### Required Expert Review

**Security + Privacy/DPO + Clinical + UX** must review the offline data model before CHT can be preferred for Sanad.

## 3. VSee

### Confirmed

Current VSee public material states that Enterprise supports:

- custom workflows;
- SSO and MFA;
- custom intake with routing logic;
- custom assessment forms;
- multi-provider operation;
- APIs and SDKs;
- asynchronous eConsult;
- commercial enterprise telehealth customisation.

A VSee feature comparison explicitly describes eConsult / asynchronous visit as supporting provider-to-provider or patient-to-provider secure consults.

Current published pricing shows:

- Free: $0/provider/month;
- Plus: $29/provider/month;
- Premium: $49/provider/month plus setup fee;
- Enterprise: quote required and typically annual.

These public prices do not establish Sanad Enterprise TCO.

### Official sources

- https://vsee.com/pricing
- https://vsee.com/dev/
- https://lp.vsee.com/hubfs/Sales-Enablement%20Materials/2023%20VSee%20Pricing%20%26%20Features%20Comparison%20Sheet.pdf

### Current Position

**Serious commercial discovery candidate**, not merely a generic comparator.

### Not Yet Verified

- offline-first capability;
- low-bandwidth operation under Sudan conditions;
- Arabic/RTL;
- data residency/hosting options suitable for Sanad;
- cross-border support access;
- clinical governance workflow fit;
- ability to minimise patient-facing assumptions;
- exact Enterprise cost and customisation cost;
- data portability and exit.

## 4. OpenMRS

### Confirmed

OpenMRS remains an actively maintained open-source clinical platform, with OpenMRS 3 releases continuing in 2026.

It is an important clinical-data and interoperability foundation, and is relevant because Intelehealth uses OpenMRS as part of its architecture.

### Official sources

- https://openmrs.org/openmrs-3-7-1-is-out/
- https://o3-docs.openmrs.org/en-US/docs/changelog/

### Current Position

**Foundation/component candidate, not currently the leading standalone Sanad tele-expertise product.**

It would require substantial workflow work for:

- tele-expertise routing;
- consultant advice;
- low-connectivity/mobile workflow;
- governance;
- offline sync.

## 5. Evidence-Based Discovery Order

The previous discovery order is refined to:

1. **Intelehealth**: strongest direct low-resource/provider-to-provider alignment.
2. **VSee Enterprise**: now confirmed to support asynchronous provider-to-provider eConsult and custom enterprise workflows.
3. **CHT**: strongest offline-first platform, but significant privacy/device and workflow-fit questions.
4. **Custom Sanad MVP**: retained as a reference/fallback and may become preferred if adaptation compromises critical requirements.
5. **OpenMRS standalone**: component/reference foundation rather than primary pilot candidate.

This is **not a final ranking**.

## 6. Evidence Still Required

No candidate can be selected without evidence for:

- Sanad workflow demonstration;
- Arabic/RTL;
- offline/weak-network test;
- security architecture;
- contextual record-level access;
- audit trail;
- hosting regions;
- data residency;
- subprocessors/support access;
- data export;
- exit/migration;
- implementation effort;
- 2-year TCO;
- legal and privacy fit.

## Required Expert Review

**Level:** Blocking before final ADR-001.

Experts:

- Technology Lead / Architect
- Security Specialist
- Privacy/DPO
- Clinical Governance
- Procurement / Commercial specialist
- Legal Counsel for data/vendor terms

The Project Manager should arrange vendor demonstrations and expert review using `VENDOR_DISCOVERY_QUESTIONNAIRE.md`.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
