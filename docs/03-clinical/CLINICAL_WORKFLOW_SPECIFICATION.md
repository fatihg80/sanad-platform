# Clinical Workflow Specification

**Version:** 0.1  
**Status:** Draft for clinical validation  
**Scope:** Initial Sanad pilot  
**Audience:** Clinical, public-health, operations, product, and engineering teams

## 1. Purpose

This document defines the proposed clinical service workflow that the technology platform must support.

It separates:

- the service concept already established in the founding prospectus;
- workflow decisions proposed for the MVP;
- and issues that still require clinical, legal, or regulatory validation.

This is not a clinical guideline and does not define how any disease should be diagnosed or treated.

## 2. Service Boundary

Sanad is designed as a **provider-to-provider tele-expertise service**.

The remote consultant advises the treating doctor rather than directly managing the patient.

The initial pilot excludes:

- direct remote consultation with patients;
- emergency service;
- guaranteed 24/7 cover;
- direct prescribing by the remote consultant;
- patient charging.

## 3. Primary Actors

### Local Doctor
The clinician who is directly responsible for the patient and initiates the case.

### Consultant
A verified specialist who reviews the submitted case and provides advice.

### Duty Coordinator
Supports operational routing, reassignment, escalation, and service continuity.

### Specialty Lead
Defines specialty-specific case requirements and supports quality review.

### Clinical Governance Lead
Owns clinical governance processes, including audit, incidents, complaints, and quality review.

### Platform Administrator
Supports technical administration without automatically receiving unrestricted clinical access.

## 4. Core Workflow

### Step 1: Create Case Draft

The local doctor creates a new case using the active template for the relevant specialty.

The case may include:

- clinical history;
- examination findings;
- vital signs;
- relevant investigation results;
- permitted images or documents;
- a specific clinical question.

The system should minimise direct patient identifiers.

**Proposed system state:** `Draft`

### Step 2: Consent Confirmation

Before submission, the local doctor confirms that the required patient consent process has been completed.

The platform records the confirmation.

The platform does not determine whether the legal form of consent is sufficient. That requirement must be defined by the approved clinical/legal governance model.

### Step 3: Submission Validation

The system checks that required fields are complete.

Possible validation outcomes:

- Ready to Submit
- Missing Required Information
- Potential Identifier Warning
- Attachment Validation Failure

The doctor corrects the case before final submission.

### Step 4: Submit Case

When submitted:

- the case receives a permanent case identifier;
- the submission timestamp is recorded;
- the selected service category is recorded;
- the case becomes read-only except through controlled amendment mechanisms;
- the response-time clock begins according to the approved service rules.

**Proposed system state:** `Submitted`

### Step 5: Routing

The case is directed to an eligible consultant.

For the pilot, routing should initially favour operational simplicity and transparency.

Recommended MVP approach:

1. specialty eligibility check;
2. consultant availability check, if availability data exists;
3. manual assignment or coordinator-assisted assignment;
4. later automation only after routing rules are validated.

**Proposed state:** `Awaiting Assignment`

After assignment:

**Proposed state:** `Assigned`

### Step 6: Consultant Accepts or Declines

The assigned consultant should be able to:

- accept the case;
- decline for a defined reason;
- indicate temporary unavailability;
- request reassignment.

Suggested decline reasons:

- outside scope of expertise;
- insufficient time;
- conflict of interest;
- technical inability;
- other approved reason.

Declines and reassignments should be auditable.

### Step 7: Consultant Review

The consultant reviews all authorised case information.

**Proposed state:** `Under Review`

The consultant may:

- prepare advice;
- request additional information;
- recommend synchronous discussion;
- request a second opinion or escalation according to policy.

## 5. Request for Additional Information

If information is insufficient, the consultant may return a structured request to the local doctor.

The request should identify what is missing without requiring informal communication outside the platform where avoidable.

Possible state:

`Awaiting Additional Information`

When the doctor responds, the case returns to:

`Under Review`

The response target behaviour while waiting for information must be defined by the service policy.

**TBD:** Whether the response timer pauses during this state.

## 6. Specialist Advice

The consultant prepares documented written advice.

The advice should distinguish, where appropriate:

- interpretation of the submitted information;
- suggested considerations;
- recommended next steps;
- limitations caused by missing information or unavailable investigations;
- urgency concerns;
- whether further review is recommended.

The final content structure must be defined by the Clinical Governance Lead and Specialty Lead.

When the consultant submits final advice:

- author identity is recorded;
- submission time is recorded;
- advice becomes part of the clinical record;
- later changes require a controlled correction or addendum.

**Proposed state:** `Advice Provided`

## 7. Synchronous Discussion

A voice or video discussion may be scheduled when written asynchronous review is insufficient.

The platform does not need to provide native video during the MVP unless the Build vs Buy vs Partner assessment demonstrates a clear requirement.

At minimum, the platform should record:

- whether a discussion was requested;
- scheduled time where relevant;
- participants;
- whether it occurred;
- a documented summary or resulting advice.

Clinical decisions should not exist only in an unrecorded call.

## 8. Local Clinical Decision

After receiving advice, the local doctor decides how to manage the patient according to:

- direct examination;
- local clinical judgement;
- available resources;
- patient circumstances;
- the specialist advice.

The technology must not present consultant advice as an automatic order.

This distinction should also be reflected in user-interface wording.

## 9. Outcome Reporting

The local doctor later records the relevant outcome.

Pilot outcome fields may include:

- whether advice changed management;
- whether referral was recommended;
- whether referral was avoided;
- whether additional investigations were ordered;
- known short-term outcome, where appropriate;
- whether further specialist review is needed.

The exact outcome dataset requires evaluation and clinical review.

**Proposed state:** `Awaiting Outcome`

## 10. Case Closure

A case can be closed once the minimum closure requirements are met.

Closure should record:

- closing user;
- closure time;
- outcome status;
- unresolved issues, if any.

**Proposed state:** `Closed`

Closed cases should not be silently edited.

Corrections after closure should use an auditable addendum or reopening process.

## 11. Routine Case Workflow

Source response target:

**24 to 48 hours**

Proposed flow:

```text
Draft
  ↓
Submitted
  ↓
Awaiting Assignment
  ↓
Assigned
  ↓
Under Review
  ↓
Advice Provided
  ↓
Awaiting Outcome
  ↓
Closed
```

## 12. Priority Case Workflow

Source description:

Time-sensitive but not an emergency.

Source response target:

**4 to 6 hours during service hours**

Priority cases should:

- be visually distinguishable;
- receive routing priority;
- generate earlier operational alerts;
- never be represented as emergency coverage.

The system should display a clear warning that Sanad is not an emergency service.

## 13. Emergency Boundary

The founding concept explicitly excludes emergency care.

If a doctor indicates that a case is immediately life-threatening, the system should not imply that Sanad can provide a guaranteed timely response.

The exact emergency warning and local escalation wording must be clinically and legally approved.

The product should avoid designing an “emergency” category that contradicts the service boundary.

## 14. Reassignment

Reassignment may occur when:

- the consultant declines;
- the consultant does not accept within a defined period;
- the consultant becomes unavailable;
- the specialty lead or coordinator identifies mismatch;
- escalation is required.

Every reassignment should retain the history of prior assignments.

## 15. Second Opinion

A second opinion may be requested for:

- complex cases;
- disputed advice;
- governance review;
- high-risk situations defined by policy.

The second consultant should receive access only after the appropriate authorisation.

The system should distinguish the original opinion from the second opinion.

It should not overwrite one with the other.

## 16. Incident and Near-Miss Workflow

An incident may relate to:

- incorrect advice;
- delayed advice;
- missed assignment;
- privacy or confidentiality concern;
- technical failure affecting care;
- inappropriate user behaviour;
- other patient-safety concern.

Proposed workflow:

```text
Incident Reported
      ↓
Triage
      ↓
Governance Review
      ↓
Corrective Action / Investigation
      ↓
Resolution
      ↓
Learning / Follow-up
```

Incident access should be more restricted than ordinary case access.

An incident record may reference a case without exposing unnecessary clinical data to all administrative users.

## 17. Complaint Workflow

Complaints should be supported from participating clinicians and consultants.

Proposed states:

- Open
- Acknowledged
- Under Review
- Action Required
- Resolved
- Closed

Complaints and clinical incidents may overlap but should not automatically be treated as the same record.

## 18. Clinical Audit Workflow

Authorised governance users should be able to select cases for audit.

An audit may assess:

- completeness of case submission;
- appropriateness of consultant assignment;
- timeliness;
- quality and clarity of advice;
- documentation quality;
- outcome completion;
- compliance with service standards.

Audit should support structured findings and actions.

## 19. Virtual MDT Workflow

A Virtual MDT is a scheduled group review of selected complex cases.

Potential flow:

1. Case nominated
2. Governance/specialty approval
3. Participants invited
4. Case material prepared
5. MDT held
6. Discussion summary recorded
7. Result communicated to treating doctor
8. Follow-up recorded

The MDT record should identify participants and preserve the relationship to the original case.

## 20. Case-Based Teaching

Teaching content should use appropriately anonymised or approved case material.

A clinical case should not automatically become teaching material.

The workflow requires explicit governance rules for:

- de-identification;
- reuse permission;
- audience;
- storage;
- publication.

## 21. Backup Communication During Outages

The founding concept allows fallback channels such as approved secure messaging or voice calls during outages, followed by later documentation in the platform.

The backup process must define:

- which channels are approved;
- what information may be shared;
- how identity is verified;
- who may initiate fallback communication;
- how the interaction is later reconstructed in the platform;
- how timestamps and authorship are recorded.

This should be treated as a controlled business-continuity workflow, not an informal workaround.

## 22. Case Status Model

Proposed normal lifecycle:

```text
Draft
Submitted
Awaiting Assignment
Assigned
Under Review
Awaiting Additional Information
Advice Provided
Awaiting Outcome
Closed
```

Proposed exception/supporting statuses:

```text
Withdrawn
Reassigned
Escalated
Second Opinion Requested
Reopened
```

Incident and complaint states should remain separate from the clinical case state machine.

## 23. Response-Time Clock

The service must define precisely:

- when the clock starts;
- whether assignment delay counts;
- whether the clock pauses while awaiting additional information;
- service hours;
- weekends and public holidays;
- consultant acceptance timeout;
- escalation thresholds;
- how outages affect measurement.

These rules must be agreed before SLA reporting is implemented.

## 24. Clinical Access Principle

Clinical access should be based on a legitimate relationship to the case.

A user should not receive broad clinical visibility merely because they hold an administrative role.

Examples:

- a consultant sees cases assigned to them;
- a coordinator sees the minimum information required for routing;
- a specialty lead sees cases required for approved governance work;
- a system administrator does not automatically receive unrestricted clinical-content access.

The final access matrix requires dedicated approval.

## 25. Information Minimisation

Case templates should prefer structured data where it improves quality and reduces unnecessary free text.

The platform should discourage:

- patient names;
- unnecessary national identifiers;
- home addresses;
- unrelated personal history;
- location information that is not clinically required.

In conflict-affected settings, clinician and facility metadata may also require protection.

## 26. Clinical Workflow Decisions Still Required

Before implementation, the founding team must resolve:

1. Pilot specialty
2. Specialty-specific case template
3. Minimum information required for submission
4. Consent wording and evidence
5. Priority classification rules
6. Consultant acceptance rules
7. Service hours
8. SLA clock behaviour
9. Reassignment thresholds
10. Second-opinion triggers
11. Outcome dataset
12. Case closure rules
13. Reopening rules
14. Incident severity model
15. Emergency warning and escalation wording
16. Approved outage backup channels
17. Case access matrix
18. Audit sampling method
19. Retention rules
20. Whether synchronous communication is embedded or external

## 27. Engineering Consequence

The software architecture should not be finalised before the workflow above is validated.

The validated workflow directly determines:

- state machine design;
- permissions;
- notification rules;
- queue behaviour;
- audit model;
- data model;
- offline conflict behaviour;
- reporting;
- escalation logic.

This specification should therefore be reviewed before the C4 architecture and major ADRs are approved.

## Required Expert Review

**Level:** Blocking before clinical workflow approval.

**Experts required:**
- Clinical Governance Lead
- Pilot Specialty Lead
- Healthcare Legal Counsel for liability/consent boundaries
- Operations representative for service-hour and escalation practicality

**Questions to review:**
- clinical responsibility boundary;
- emergency exclusion wording;
- priority criteria;
- additional-information workflow;
- second-opinion triggers;
- closure/reopening rules;
- fallback communication safety.

**Evidence to retain:** written review/approval, date, reviewers, unresolved conditions.

See `docs/00-governance/EXPERT_REVIEW_REGISTER.md`.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
