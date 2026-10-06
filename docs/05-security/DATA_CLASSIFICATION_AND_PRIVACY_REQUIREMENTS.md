# Data Classification and Privacy Requirements

**Version:** 0.1  
**Status:** Draft for legal, clinical, security, and product review  
**Scope:** Initial Sanad pilot

## 1. Purpose

This document defines an initial data-classification model and privacy requirements for Sanad.

It is a product and security design input, not legal advice.

Final lawful bases, retention requirements, international-transfer rules, and jurisdiction-specific obligations must be validated by qualified legal and data-protection advisers before live operation.

## 2. Privacy Design Principle

Sanad should not ask:

> What information could be useful?

It should ask:

> What is the minimum information required to deliver safe tele-expertise and evaluate the pilot?

The platform should minimise both patient data and information that could expose clinicians, facilities, or participants in conflict-affected areas.

## 3. Proposed Data Classes

### Class A: Public

Information intentionally suitable for public release.

Examples:

- public project description;
- published research outputs;
- public policy briefs;
- public contact information approved for publication.

**Handling:** No special confidentiality control beyond normal integrity protection.

### Class B: Internal

Operational information not intended for public distribution but not normally patient-identifiable.

Examples:

- internal project plans;
- generic training material;
- non-sensitive operating procedures;
- aggregated service metrics where disclosure risk is low.

**Handling:** Authenticated access; organisational sharing rules apply.

### Class C: Confidential Professional

Information relating to clinicians, consultants, staff, or partners.

Examples:

- professional registration details;
- verification documents;
- personal contact information;
- consultant availability;
- contracts;
- payment details;
- internal performance or governance information.

**Handling:** Role-restricted access, encryption, audited administrative actions, retention limits.

### Class D: Sensitive Clinical

Clinical information submitted for a case that could relate to an individual patient even when direct identifiers are removed.

Examples:

- history;
- examination findings;
- vital signs;
- laboratory results;
- ECGs;
- X-rays;
- clinical photographs;
- consultant advice;
- follow-up outcomes.

**Handling:** Strongest routine clinical controls, contextual access, encryption, auditability, strict retention and export rules.

### Class E: Highly Sensitive Safety / Governance

Information whose disclosure could create exceptional clinical, legal, professional, or physical safety risk.

Examples:

- incident investigations;
- complaints involving individuals;
- suspected misconduct;
- security incidents;
- clinician location or identity data in high-risk environments;
- sanctions-related records;
- sensitive legal advice;
- breach investigations.

**Handling:** Need-to-know access, additional role restrictions, stronger monitoring, controlled export, dedicated retention rules.

## 4. Direct Patient Identifiers

The product should not normally require:

- patient name;
- national identity number;
- home address;
- personal telephone number;
- personal email;
- exact home location.

If a specialty later demonstrates that an identifier is clinically necessary, that requirement must be explicitly reviewed and approved rather than added by convenience.

## 5. Indirect Identification Risk

Removing a patient name does not automatically make a case anonymous.

A patient may still be identifiable from combinations such as:

- rare condition;
- exact age;
- exact facility;
- exact admission date;
- photograph;
- distinctive injury;
- geographic information;
- uncommon occupation;
- free-text narrative.

Sanad should therefore treat clinical cases as sensitive clinical information even when direct identifiers are absent.

## 6. Clinician and Facility Safety

In conflict-affected settings, data about clinicians and facilities may itself create physical risk.

Potentially sensitive information includes:

- clinician full identity;
- exact work location;
- shift schedules;
- contact information;
- IP address;
- device information;
- geolocation;
- facility details;
- timestamps that reveal activity patterns.

The product should avoid collecting or exposing such information unless required.

## 7. Image and File Metadata

Uploaded files may contain hidden metadata.

Potential examples:

- EXIF location;
- device model;
- author name;
- creation timestamp;
- document properties;
- embedded thumbnails.

The platform should assess metadata stripping before storage or sharing.

However, automated processing must not damage clinically meaningful image content.

Any transformation of diagnostic material requires clinical validation.

## 8. Free Text

Free-text fields are a major privacy risk because users may enter unnecessary identifiers.

Controls should include a combination of:

- clear field guidance;
- warnings;
- structured fields where useful;
- staff training;
- potential detection of obvious identifiers;
- governance review.

Automated identifier detection should be treated as assistance, not as a guarantee of de-identification.

## 9. Access Model

Access to clinical data should require a legitimate service relationship.

Examples:

- local doctor: cases they submitted or are authorised to manage;
- consultant: cases assigned to them;
- coordinator: minimum case information required for routing;
- specialty lead: approved cases required for governance;
- governance lead: cases required for authorised safety and quality work;
- research user: approved dataset, preferably de-identified or pseudonymised;
- platform administrator: technical privilege should not automatically imply unrestricted clinical visibility.

The final permissions matrix requires formal approval.

## 10. Purpose Limitation

Information collected for clinical tele-expertise should not automatically be reused for:

- research;
- publication;
- teaching;
- product demonstrations;
- fundraising;
- model training;
- external analytics.

Each secondary purpose requires an appropriate governance and legal basis.

## 11. Research and Evaluation

Pilot evaluation is part of the founding concept.

The project should define:

- which evaluation fields are collected;
- whether data is identifiable, pseudonymised, or aggregated;
- who can access research datasets;
- ethics requirements;
- consent implications;
- publication safeguards;
- retention period.

Research access should not be implemented as unrestricted access to production clinical records.

## 12. Teaching and MDT Reuse

A clinical case should not automatically become reusable teaching content.

The governance process should determine:

- whether reuse is permitted;
- whether additional consent is required;
- de-identification requirements;
- permitted audience;
- retention;
- whether images can be reused.

## 13. Offline Storage

Offline capability is a core product requirement, but sensitive local storage creates risk.

For the MVP:

- offline storage should be minimised;
- text drafts should contain the minimum necessary information;
- full offline clinical archives should be avoided;
- attachment caching requires explicit approval;
- local data should have a defined expiry mechanism;
- synchronised data should be removed locally where appropriate;
- lost-device risk must be considered.

A dedicated ADR should determine the exact offline architecture.

## 14. Logging and Observability

Logs must not become a shadow clinical database.

Application logs should avoid:

- full case text;
- consultant advice content;
- patient identifiers;
- authentication secrets;
- file contents.

Logs may include controlled technical references such as:

- internal case ID;
- event type;
- timestamp;
- error code;
- service component.

Access to logs should be restricted and retention defined.

## 15. Analytics

Product analytics should minimise user and clinical data.

The team should be cautious with third-party analytics SDKs because they may transmit:

- device data;
- IP addresses;
- usage behaviour;
- page names;
- identifiers.

No third-party analytics service should be introduced into clinical workflows without privacy and security review.

## 16. Data Residency and Cross-Border Processing

Hosting and processing jurisdictions are currently TBD.

Before selection, the team must identify:

- where production data is stored;
- where backups are stored;
- where support personnel can access data;
- where subprocessors operate;
- whether consultant access constitutes a regulated international transfer;
- contractual and legal safeguards required.

This decision should be recorded before production deployment.

## 17. Retention

Retention periods are currently TBD.

The retention schedule should separately address:

- clinical cases;
- audit trails;
- professional verification documents;
- incidents;
- complaints;
- financial records;
- research datasets;
- logs;
- backups.

"Keep everything forever" is not an acceptable default.

## 18. Deletion and Correction

The platform must distinguish between:

- correction of inaccurate data;
- controlled amendment of clinical records;
- account closure;
- removal under applicable privacy rights;
- retention required for clinical, legal, or governance reasons.

Clinical records should not be silently overwritten.

## 19. Export and Download

Export creates additional leakage risk.

The system should define:

- which roles may export;
- permitted formats;
- whether exports are watermarked or logged;
- whether bulk export is allowed;
- whether clinical images may be downloaded;
- expiry of generated export links.

Bulk export should not be enabled by default.

## 20. Backups

Backups should:

- be encrypted;
- have restricted access;
- follow retention rules;
- be included in incident-response planning;
- be tested for restoration;
- not silently extend data retention beyond approved policy.

## 21. Security Incident Link

A privacy breach may also be a security incident and a clinical safety issue.

The future incident-response plan should define coordination between:

- technology;
- clinical governance;
- data protection;
- legal/compliance;
- communications;
- partner organisations.

## 22. Decisions Required Before Pilot

1. Hosting jurisdiction
2. Data residency
3. Lawful processing basis
4. Data controller / processor roles
5. Retention periods
6. Cross-border transfer model
7. Offline storage model
8. Attachment metadata policy
9. Research dataset design
10. Teaching reuse rules
11. Export permissions
12. Backup retention
13. Administrator clinical-access boundaries
14. Approved analytics and monitoring services
15. Breach-notification responsibilities

## 23. Architecture Consequences

The privacy model directly affects:

- database design;
- object storage;
- tenancy and access rules;
- logging;
- audit architecture;
- offline storage;
- analytics;
- backups;
- hosting region;
- support processes;
- research pipelines.

These decisions must therefore be resolved alongside, not after, architecture design.

## Required Expert Review

**Level:** Required before data model freeze; blocking before production.

**Experts:** Privacy/DPO, Healthcare Legal Counsel, Security Architect, Clinical Governance.

**Review:** sensitivity classes, indirect identification, clinician safety, secondary use, exports, offline storage, international processing, and data-subject obligations.
