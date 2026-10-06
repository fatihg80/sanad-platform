# Sanad Threat Model

**Version:** 0.1  
**Status:** Draft, living security artifact  
**Scope:** Pilot and custom-platform reference architecture

## 1. Purpose

This document identifies security, privacy, clinical-safety, and physical-safety threats that could affect Sanad.

Threat modelling is treated as a continuous activity. It must be revisited when the clinical workflow, hosting model, identity model, offline behaviour, third-party integrations, or regulatory assumptions change.

## 2. Threat-Modelling Method

Sanad uses four recurring questions:

1. What are we building?
2. What can go wrong?
3. What will we do about it?
4. Did we do a good enough job?

Threat identification uses STRIDE as a practical taxonomy, supplemented by privacy, clinical-safety, conflict-environment, and operational threats.

## 3. Assets Requiring Protection

### Clinical assets
- structured case content;
- clinical images and documents;
- specialist advice;
- outcomes;
- second opinions;
- MDT records.

### Identity assets
- doctor and consultant identities;
- professional registration evidence;
- contact details;
- account credentials;
- MFA recovery data.

### Governance assets
- incidents;
- complaints;
- clinical audits;
- misconduct concerns;
- corrective actions.

### Operational assets
- routing information;
- consultant availability;
- facility information;
- service schedules;
- notification metadata.

### Security assets
- credentials;
- secrets;
- encryption keys;
- audit logs;
- backup data;
- infrastructure configuration.

### Safety-sensitive metadata
- clinician location;
- facility location;
- device metadata;
- IP address;
- EXIF metadata;
- timestamps that reveal activity patterns.

## 4. Adversaries and Failure Sources

Potential threat actors or sources include:

- external cybercriminals;
- credential thieves;
- malicious insiders;
- compromised clinician devices;
- hostile or coercive actors in conflict areas;
- unauthorised facility staff;
- over-privileged administrators;
- compromised third-party vendors;
- accidental user disclosure;
- software defects;
- misconfiguration;
- unreliable networks;
- lost or stolen devices.

The project must not assume all threats are financially motivated.

## 5. Trust Boundaries

Important trust boundaries include:

- clinician device ↔ internet;
- browser/PWA ↔ Sanad application;
- application ↔ database;
- application ↔ object storage;
- application ↔ notification provider;
- application ↔ monitoring provider;
- application ↔ identity provider, if external;
- production system ↔ research/evaluation environment;
- online platform ↔ fallback communication channel;
- one user role ↔ another user's clinical context.

## 6. STRIDE Threats

### 6.1 Spoofing

Threats:

- stolen clinician credentials;
- fake professional account;
- attacker impersonates consultant;
- session theft;
- phone-number or email takeover;
- forged professional registration evidence.

Controls:

- professional verification workflow;
- MFA;
- secure session management;
- credential-breach protection where feasible;
- re-verification for sensitive account changes;
- audit of identity changes;
- privileged-role approval.

### 6.2 Tampering

Threats:

- submitted case modified after review;
- advice altered after submission;
- attachment replaced;
- audit log altered;
- outcome changed to manipulate evaluation;
- routing history overwritten.

Controls:

- immutable or append-oriented histories for material events;
- controlled addenda rather than silent overwrite;
- content integrity checks;
- author and timestamp recording;
- database permissions;
- privileged-action audit;
- backup integrity controls.

### 6.3 Repudiation

Threats:

- user denies submitting advice;
- coordinator denies reassignment;
- administrator denies access-control change;
- fallback call cannot be reconstructed.

Controls:

- authenticated actions;
- server timestamps;
- append-oriented audit trail;
- assignment history;
- explicit advice submission;
- fallback communication reconstruction procedure.

### 6.4 Information Disclosure

Threats:

- user accesses unrelated cases;
- public object-storage URL;
- notification exposes clinical details;
- logs contain case text;
- analytics provider receives sensitive metadata;
- EXIF reveals location;
- research export is identifiable;
- administrator sees all cases by default;
- screen or device loss exposes offline drafts.

Controls:

- contextual authorisation;
- private object storage;
- signed short-lived object access;
- data minimisation;
- notification-content policy;
- metadata stripping where safe;
- log redaction;
- export governance;
- offline data minimisation;
- device/session controls.

### 6.5 Denial of Service

Threats:

- volumetric attack;
- abusive requests;
- upload flooding;
- queue exhaustion;
- database resource exhaustion;
- dependency outage;
- intentional disruption during a conflict event.

Controls:

- rate limiting;
- upload quotas;
- WAF/reverse-proxy protections;
- queue isolation;
- resource monitoring;
- graceful degradation;
- operational fallback channels;
- tested recovery procedures.

### 6.6 Elevation of Privilege

Threats:

- local doctor gains admin access;
- consultant accesses governance functions;
- technical administrator gains clinical visibility;
- compromised service account gains broad access.

Controls:

- least privilege;
- explicit role boundaries;
- contextual authorisation;
- separate privileged roles;
- MFA for privileged access;
- deny-by-default policies;
- privileged-action monitoring;
- periodic access review.

## 7. Clinical Safety Threats

Security failures can become patient-safety failures.

Examples:

- delayed case due to failed notification;
- wrong consultant assignment;
- duplicate submission;
- stale offline draft overwrites newer information;
- consultant reviews incomplete attachment set;
- image compression removes diagnostic detail;
- incorrect timezone causes SLA or scheduling error;
- advice displayed as authoritative order rather than consultation;
- emergency case incorrectly treated as normal Sanad workflow.

Controls must therefore include both cybersecurity and clinical-workflow validation.

## 8. Offline and Synchronisation Threats

Threats:

- sensitive drafts remain on lost device;
- duplicate cases created after reconnect;
- conflicting edits silently overwrite server state;
- stale clinical information submitted;
- attachments partially upload;
- local cache survives logout;
- device shared between staff members.

Required controls:

- visible synchronisation state;
- idempotent submission;
- explicit conflict handling;
- local-data expiry;
- minimise offline fields;
- avoid full offline archive in MVP;
- secure local storage where supported;
- clear logout/cache behaviour;
- attachment integrity verification.

## 9. Image and Attachment Threats

Threats:

- malware embedded in documents;
- active content in uploaded formats;
- EXIF location;
- oversized files exhaust storage;
- wrong file attached to case;
- diagnostic image altered by compression;
- predictable storage URL.

Controls:

- file allowlist;
- size limits;
- malware scanning where practical;
- metadata policy;
- private object storage;
- random object identifiers;
- clinically validated processing;
- integrity/hash checks;
- attachment confirmation in UI.

## 10. Notification Threats

Threats:

- SMS/email/push reveals condition or patient detail;
- notification sent to old contact method;
- phishing through fake Sanad alerts;
- third-party provider retains metadata.

Controls:

- minimal notification text;
- contact verification;
- notification preference management;
- provider privacy review;
- no sensitive payload in push notification;
- anti-phishing communication guidance.

## 11. Research and Evaluation Threats

Threats:

- research user accesses production directly;
- exported dataset can be re-identified;
- rare cases reveal identity;
- dataset reused beyond approved purpose;
- publication reveals facility or clinician location.

Controls:

- separate approved extraction process;
- pseudonymisation/de-identification;
- minimum dataset;
- purpose-specific access;
- export logging;
- ethics/governance review;
- disclosure-risk review before publication.

## 12. Conflict-Environment Threats

Sanad must account for risks that conventional telemedicine systems may underweight.

Threats:

- clinician location inferred from metadata;
- facility participation list used for targeting or coercion;
- user pressured to reveal credentials;
- captured device reveals professional network;
- political affiliation inferred from facility or region;
- public contributor list creates risk.

Controls:

- no unnecessary public participant directory;
- minimise precise location;
- minimise retained device/network metadata;
- separate public project information from operational participant information;
- rapid account/session revocation;
- incident playbook for coercion or device seizure;
- neutrality-by-design in labels and reporting.

## 13. Third-Party Threats

Potential third parties:

- hosting provider;
- object-storage provider;
- email/SMS/push provider;
- monitoring/error provider;
- identity provider;
- telemedicine platform partner;
- analytics provider.

Before approval, assess:

- data processed;
- hosting locations;
- subprocessors;
- breach history/process;
- retention;
- deletion;
- encryption;
- admin access;
- contractual rights;
- exit and portability.

## 14. High-Risk Threat Register

| ID | Threat | Likelihood | Impact | Priority |
|---|---|---:|---:|---|
| T-01 | Compromised clinician account exposes cases | Medium | Critical | Critical |
| T-02 | Excessive role permissions expose unrelated cases | Medium | Critical | Critical |
| T-03 | Device/offline cache exposes sensitive case data | Medium | High | High |
| T-04 | Metadata reveals clinician/facility location | Medium | Critical | Critical |
| T-05 | Wrong or stale case data caused by sync conflict | Medium | Critical | Critical |
| T-06 | Clinical image damaged by processing | Low/Medium | Critical | High |
| T-07 | Notification failure delays priority response | Medium | High | High |
| T-08 | Admin or vendor accesses clinical data unnecessarily | Medium | High | High |
| T-09 | Research export permits re-identification | Medium | High | High |
| T-10 | Platform outage causes reliance on unsafe informal channel | High | High | High |
| T-11 | Audit trail can be altered or bypassed | Low/Medium | High | High |
| T-12 | Cross-border vendor/data arrangement violates obligations | Medium | High | High |

Likelihood values are preliminary and require review once deployment details are known.

## 15. Security Validation Activities

Before pilot:

- architecture review;
- threat-model review;
- authorisation tests;
- abuse-case tests;
- secure-code review;
- dependency scanning;
- static analysis;
- dynamic application testing;
- object-storage configuration review;
- backup restore test;
- incident-response tabletop exercise;
- offline-device loss test;
- privacy/data-flow review;
- clinical workflow failure-mode review;
- external penetration test before live clinical use where feasible.

## 16. Review Triggers

Update this threat model when:

- pilot specialty changes;
- offline capability expands;
- native mobile app is introduced;
- new third-party provider is added;
- hosting region changes;
- direct patient services are considered;
- payment is introduced;
- API integration is added;
- research data flow changes;
- a significant incident occurs.

## 17. Open Threat Decisions

- device trust requirements;
- MFA mechanism;
- offline encryption approach;
- session duration;
- attachment malware-scanning service;
- metadata stripping rules;
- administrator break-glass access;
- audit immutability strategy;
- secrets-management platform;
- WAF/DDoS provider;
- research export environment;
- security monitoring provider.

## Required Expert Review

**Level:** Required before architecture freeze; blocking before go-live.

**Experts required:**
- Security Architect / Application Security Specialist
- Privacy/DPO representative
- Clinical Governance representative for safety consequences
- Infrastructure/SRE representative once hosting is selected

**Evidence to retain:** review findings, accepted residual risks, remediation actions, and review date.

An independent implementation-level security assessment remains required before live clinical use.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
