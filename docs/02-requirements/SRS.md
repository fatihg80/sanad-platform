# Sanad Software Requirements Specification

**Version:** 0.1  
**Status:** Draft  
**Scope:** MVP supporting the initial pilot

## 1. Purpose

This SRS translates the product concept into testable software requirements. It does not replace clinical, legal, regulatory, or information-governance specifications.

## 2. Proposed MVP Architecture

Engineering recommendation:

- Modular monolith for the MVP
- Clear domain boundaries
- API-capable design
- PostgreSQL as the primary relational database
- Queue and cache layer
- Object storage for permitted files and images
- Mobile-first web application
- Progressive Web App capabilities where safe
- Full audit trail for material actions

Microservices are not recommended for the initial pilot because current scale does not justify the operational complexity.

## 3. Proposed Domains

- Identity and Access
- Professional Verification
- Facilities
- Clinical Cases
- Routing
- Consultant Availability
- Clinical Advice
- Outcomes
- Governance
- Incidents and Complaints
- Notifications
- Audit
- Reporting

## 4. Roles

Initial logical roles:

- Local Doctor
- Consultant
- Duty Coordinator
- Specialty Lead
- Clinical Governance Lead
- Research / Evaluation User
- Platform Administrator

Final permissions require governance review.

## 5. Case Lifecycle

Proposed state model:

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

Possible exception states:

- Withdrawn
- Rejected / Insufficient Information
- Reassigned
- Escalated
- Second Opinion Requested
- Incident Under Review

Exact transitions remain subject to clinical workflow validation.

## 6. Identity and Access Requirements

- **IAM-001** The system shall require authentication for protected functions.
- **IAM-002** Access shall be determined by role and authorised context.
- **IAM-003** Professional accounts shall have a verification state.
- **IAM-004** Unverified users shall not submit or answer live clinical cases.
- **IAM-005** Administrative privilege changes shall be audited.
- **IAM-006** Session and credential controls shall follow the approved security baseline.
- **IAM-007** Multi-factor authentication should be required for privileged roles and evaluated for all clinical users.

## 7. Case Requirements

- **CASE-001** A local doctor shall be able to create a draft case.
- **CASE-002** A case shall use the active template for its specialty.
- **CASE-003** Required clinical fields shall be validated before submission.
- **CASE-004** The system shall record that consent requirements were acknowledged before submission.
- **CASE-005** The system shall discourage or prevent unnecessary direct patient identifiers.
- **CASE-006** Permitted attachments shall be validated by type and size.
- **CASE-007** Case changes after submission shall be controlled and auditable.
- **CASE-008** The system shall retain case lifecycle timestamps.
- **CASE-009** Users shall only see cases for which they have authorised access.

## 8. Routing Requirements

- **ROUTE-001** Submitted cases shall enter a routing workflow.
- **ROUTE-002** Authorised coordinators shall be able to assign a consultant.
- **ROUTE-003** Assignment shall consider specialty eligibility.
- **ROUTE-004** Assignment and reassignment shall be audited.
- **ROUTE-005** The design shall permit later introduction of availability-aware or rules-based routing.
- **ROUTE-006** Priority cases shall be identifiable throughout the workflow.

## 9. Advice Requirements

- **ADV-001** An assigned consultant shall be able to review the available case information.
- **ADV-002** The consultant shall be able to provide written advice.
- **ADV-003** Advice submission shall record author and timestamp.
- **ADV-004** The system shall distinguish draft advice from final submitted advice.
- **ADV-005** Material correction of final advice shall preserve history.
- **ADV-006** The workflow shall support authorised requests for additional information.

## 10. Outcome Requirements

- **OUT-001** The local doctor shall be able to record management or outcome information.
- **OUT-002** Outcome capture shall support pilot evaluation requirements.
- **OUT-003** Closure rules shall identify required minimum information.
- **OUT-004** Closed cases shall remain available according to approved retention and access rules.

## 11. Governance Requirements

- **GOV-001** Authorised clinical leads shall be able to select cases for audit.
- **GOV-002** The system shall support structured audit findings.
- **GOV-003** The service shall support incident and near-miss reporting.
- **GOV-004** Incident records shall have restricted access.
- **GOV-005** The service shall support complaint tracking.
- **GOV-006** The workflow shall support second-opinion requests.
- **GOV-007** Governance actions shall be audited.

## 12. Audit Requirements

The audit trail should record, where applicable:

- actor;
- action;
- timestamp;
- affected entity;
- prior and new state for material changes;
- assignment changes;
- access-control changes;
- advice submission and correction;
- case closure;
- governance events.

Audit logs must not become an uncontrolled duplicate store of sensitive clinical content.

## 13. Offline and Connectivity Requirements

- **OFF-001** The system should allow safe drafting during intermittent connectivity.
- **OFF-002** The user shall be informed when content is not yet synchronised.
- **OFF-003** Synchronisation shall avoid silent data loss.
- **OFF-004** Conflict behaviour shall be explicitly defined.
- **OFF-005** Sensitive local storage shall be minimised.
- **OFF-006** Attachment offline behaviour requires separate security approval.
- **OFF-007** Failed uploads should be resumable where practical.

A full offline clinical record is not assumed for the MVP.

## 14. File and Image Handling

- Validate file type
- Enforce size limits
- Strip unnecessary metadata where appropriate
- Avoid exposing direct object-storage URLs
- Authorise every retrieval
- Support compression or optimisation where clinically acceptable
- Preserve diagnostic usefulness when processing clinical images

Image-processing rules must be clinically validated before use on diagnostic material.

## 15. Notifications

Potential events:

- new assignment;
- request for additional information;
- advice submitted;
- response target approaching;
- reassignment;
- second opinion;
- governance action.

Channels remain TBD.

No notification should expose unnecessary sensitive clinical content.

## 16. Reporting

Initial reporting should support:

- case volumes;
- case category;
- facilities;
- specialties;
- response times;
- target compliance;
- completion rates;
- outcomes where captured;
- incidents and complaints at an appropriate governance level;
- consultant participation;
- pilot evaluation metrics.

## 17. Security Requirements

At minimum:

- TLS in transit
- encryption at rest
- least privilege
- role-based access
- secure secrets handling
- strong authentication controls
- protected object storage
- audit logging
- rate limiting
- secure session handling
- dependency monitoring
- backup and recovery
- vulnerability management
- incident response procedures

Detailed controls belong in the Security Architecture and Threat Model.

## 18. Privacy Requirements

- Data minimisation by design
- No unnecessary patient names
- Controlled free-text usage
- Consent recording
- Defined lawful processing basis, subject to legal review
- Retention schedule, TBD
- Data residency, TBD
- Cross-border transfer analysis, TBD
- Privacy impact assessment before live operation where required
- Metadata exposure assessment, including image EXIF and device/network metadata

## 19. Proposed MVP Technology Direction

Engineering proposal, not yet an approved architecture decision:

- Laravel for the application backend
- Vue 3 + TypeScript for the user interface
- PostgreSQL
- Redis for queues and cache
- S3-compatible object storage
- PWA capabilities for constrained connectivity
- Containerised deployment
- CI/CD
- centralised logs and error monitoring

A formal Build vs Buy vs Partner assessment must occur before implementation commitment.

## 20. MVP Acceptance Themes

The MVP must demonstrate that:

- verified users can securely access the service;
- a local doctor can submit a usable structured case;
- the case can be routed;
- a consultant can provide documented advice;
- the local doctor can report an outcome;
- the service can close and audit cases;
- priority and routine workflows are distinguishable;
- basic operations remain usable under weak connectivity;
- material actions are traceable;
- the workflow can support pilot evaluation.

## 21. Required Follow-on Specifications

- Clinical Workflow Specification
- Clinical Governance Specification
- Data Classification and Privacy Requirements
- Security Architecture
- Threat Model
- C4 Architecture
- Build vs Buy vs Partner ADR / assessment
- Backup and Disaster Recovery Plan
- Pilot Operations Runbook

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
