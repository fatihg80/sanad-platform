# Sanad Domain Model

**Version:** 0.1  
**Status:** Draft  
**Purpose:** Define the core business concepts and boundaries that shape the software model.

## 1. Domain Principle

Sanad should model the real clinical and operational service, not the screens of the application.

The domain model therefore centres on:

- verified professionals;
- facilities;
- clinical cases;
- assignments;
- specialist advice;
- outcomes;
- governance;
- audit.

## 2. Proposed Bounded Modules

### Identity
User account, authentication identity, account status, contact channels.

### Professional Verification
Professional registration, verification evidence, verification state, reviewer, expiry/revalidation.

### Facilities
Participating healthcare facilities and approved relationships.

### Clinical Cases
Case creation, specialty template, structured clinical content, lifecycle, consent confirmation, attachments.

### Routing
Assignment, reassignment, routing reason, consultant eligibility, service priority.

### Consultant Availability
Availability windows, temporary unavailability, workload indicators.

### Clinical Advice
Advice draft, final advice, information request, addendum, synchronous-review record.

### Outcomes
Follow-up, management change, referral information, evaluation outcome fields.

### Clinical Governance
Audit, second opinion, clinical review, quality actions.

### Incidents
Patient-safety and service incidents, triage, investigation, corrective action.

### Complaints
Complaint intake, review, response, closure.

### Notifications
Delivery request, channel, delivery status, minimal payload.

### Audit
Material event trail.

### Reporting
Operational and approved evaluation views.

## 3. Core Entities

### User
Represents a platform identity.

Key concepts:

- status;
- preferred language;
- contact channels;
- authentication factors.

### ProfessionalProfile
Represents professional information distinct from the account.

Examples:

- profession;
- specialty;
- registration;
- country of practice;
- verification state.

### Facility
A participating healthcare organisation or clinical location.

Exact location information must be minimised when safety requires.

### ClinicalCase
Central aggregate for tele-expertise.

Candidate attributes:

- internal case ID;
- submitting doctor;
- facility;
- specialty;
- service category;
- template version;
- lifecycle state;
- created/submitted timestamps;
- consent confirmation;
- structured clinical fields.

### CaseAttachment
Reference to a protected uploaded object.

### Assignment
Links a case to a consultant for a specific assignment period.

Assignment history must be retained.

### InformationRequest
Structured request from consultant to submitting doctor for missing information.

### Advice
Specialist response.

Final advice must not be silently overwritten.

### AdviceAddendum
Controlled addition/correction after final advice.

### Outcome
Follow-up information recorded by the treating doctor.

### SecondOpinion
Separate specialist review linked to the original case.

### ClinicalAudit
Governance review of a case against defined criteria.

### Incident
Safety or service incident.

### Complaint
Complaint record, distinct from incident even where related.

### AuditEvent
Append-oriented event representing a material business action.

## 4. Aggregate Boundaries

Suggested aggregates:

```text
ClinicalCase
├── CaseContent
├── Attachments
├── InformationRequests
├── Assignment references
├── Advice references
└── Outcome reference

ProfessionalProfile
├── Registrations
├── VerificationEvidence
└── VerificationHistory

Incident
├── IncidentEvents
└── CorrectiveActions

Complaint
├── ComplaintEvents
└── Resolution
```

Do not force all related data into one database transaction if business consistency does not require it.

## 5. Case Identity

Use a non-meaningful internal identifier.

Do not encode:

- patient identity;
- facility code that reveals location;
- specialty;
- date of birth;
- political/geographic information

into externally visible IDs.

A separate human-friendly case reference may be generated if operationally useful.

## 6. Template Versioning

Case templates must be versioned.

A submitted case must retain the template version used at the time of submission.

Changing a template must not retroactively change the meaning of historical cases.

## 7. Advice Immutability Principle

Once final advice is submitted:

- preserve the original;
- corrections use addenda or controlled supersession;
- retain author and timestamps;
- never silently replace content.

## 8. Assignment History

A case may be assigned multiple times.

Every assignment record should retain:

- consultant;
- assigned by;
- assigned time;
- acceptance/decline;
- decline reason;
- reassignment reason;
- completion/release time.

## 9. Governance Separation

Incidents and complaints should not be embedded as ordinary fields on the case.

They are separate governed records that may reference:

- a case;
- a user;
- a facility;
- an operational event.

This supports stricter access control.

## 10. Research Boundary

Research/evaluation datasets are outputs of an approved extraction process.

They are not a separate unrestricted production role with direct access to every clinical table.

## 11. Domain Events

Potential domain events include:

- ProfessionalVerified
- CaseSubmitted
- CaseAssigned
- AssignmentDeclined
- AdditionalInformationRequested
- AdditionalInformationProvided
- AdviceSubmitted
- AdviceAddendumAdded
- OutcomeRecorded
- CaseClosed
- CaseReopened
- SecondOpinionRequested
- IncidentReported
- ComplaintOpened

Domain events may drive notifications, audit records, metrics, and asynchronous work.

## 12. Invariants

Examples of business rules that must always hold:

- only verified professionals can participate in live case workflow;
- a submitted case has a valid template version;
- a consultant cannot submit final advice for a case they are not authorised to review;
- a closed case cannot be silently edited;
- final advice history is preserved;
- every material assignment change is auditable;
- clinical access requires contextual authorisation.

## 13. Open Domain Decisions

- exact specialty taxonomy;
- professional-registration model by country;
- multi-facility doctor relationships;
- consultant availability representation;
- whether a case may have multiple concurrent consultants;
- second-opinion assignment rules;
- outcome vocabulary;
- clinical coding standards;
- MDT aggregate design;
- retention and archival states.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
