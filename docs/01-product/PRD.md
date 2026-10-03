# Sanad Product Requirements Document

**Version:** 0.2  
**Status:** Draft  
**Stage:** Pilot planning  
**Product type:** Provider-to-provider tele-expertise service

## 1. Product Summary

Sanad is intended to connect verified doctors working inside Sudan with verified Sudanese specialist consultants based abroad.

Local doctors submit structured clinical cases and request specialist advice. Consultants review the submitted information and provide documented guidance. The local treating doctor remains responsible for patient care and clinical decisions.

The initial phase does not include direct doctor-to-patient telemedicine.

## 2. Problem

Sudan's health system has lost significant specialist capacity because of conflict, displacement, and disruption of services.

At the same time, many Sudanese specialists now practise abroad and are willing to support colleagues inside Sudan. Informal remote support already occurs through messaging and phone calls, but it is often unstructured, unpaid, undocumented, difficult to audit, and difficult to evaluate.

Sanad aims to create a structured, accountable, measurable, and potentially sustainable alternative.

## 3. Product Vision

Create a secure, simple, clinically governed tele-expertise network that enables doctors inside Sudan to access specialist knowledge from Sudanese consultants abroad.

## 4. Objectives

- Improve structured access to specialist advice
- Reduce professional isolation among local doctors
- Provide an organised route for diaspora specialists to contribute
- Create an auditable record of advice
- Measure clinical and operational outcomes
- Generate evidence for future policy and regulatory development
- Validate the operating model through a controlled pilot

## 5. Primary Users

### Local doctor
Submits cases, receives specialist advice, makes local clinical decisions, and records outcomes.

### Consultant
Reviews assigned cases and provides documented specialist advice.

### Duty coordinator
Supports service operations, routing, and escalation.

### Specialty lead
Owns specialty-specific templates, quality review, consultant support, and audit.

### Clinical governance lead
Owns clinical standards, incident review, verification, and quality processes.

### Platform administrator
Manages access, configuration, support, and system administration.

### Research and evaluation team
Uses appropriately governed data for evaluation and approved research.

## 6. Pilot Scope

Current source concept:

- one specialty;
- one Sudanese state;
- 3 to 5 facilities;
- 20 to 40 doctors inside Sudan;
- 10 to 20 consultants abroad;
- approximately 300 to 500 cases;
- six months of live service after preparation.

The exact specialty, state, facilities, and final platform remain TBD.

## 7. In Scope

- Professional user verification
- Role-based access
- Structured case submission
- Specialty-specific case templates
- Supporting images and results
- Routine and priority case categories
- Case routing
- Written specialist advice
- Scheduled synchronous discussion where required
- Outcome reporting
- Case closure
- Clinical audit
- Incident reporting
- Complaints handling
- Second opinion workflow
- Arabic and English
- Service reporting and evaluation data

## 8. Out of Scope for the Initial Pilot

- Direct patient consultations
- Remote consultant prescribing directly to patients
- Patient charging
- Emergency service
- Guaranteed 24/7 coverage

## 9. Core Case Journey

1. Local doctor creates a structured case.
2. Required consent is recorded.
3. The case is submitted.
4. The case is routed to a suitable consultant.
5. The consultant reviews the case.
6. Written advice is documented.
7. A scheduled call may follow if needed.
8. The local doctor decides on management.
9. The local doctor records the outcome.
10. The case is closed.
11. Selected cases may be reviewed through clinical governance processes.

## 10. Service Categories

### Routine
Target response: 24 to 48 hours.

### Priority
Time-sensitive but not an emergency.  
Target response: 4 to 6 hours during service hours.

### Virtual MDT
Scheduled multidisciplinary review of complex cases.

### Case-based teaching
Teaching using appropriately anonymised clinical cases.

## 11. Functional Requirements

- **FR-001** The system shall support controlled professional user registration.
- **FR-002** The system shall support verification of local doctors and consultants.
- **FR-003** The system shall authenticate users before protected access.
- **FR-004** The system shall enforce role-based permissions.
- **FR-005** Local doctors shall be able to create structured case drafts.
- **FR-006** Case templates shall support specialty-specific configuration.
- **FR-007** Users shall be able to attach permitted clinical images and results.
- **FR-008** The system shall support case submission after required validations.
- **FR-009** Cases shall be routed manually, automatically, or through a hybrid model, with final rules TBD.
- **FR-010** Consultants shall be able to provide documented written advice.
- **FR-011** Cases shall support scheduled synchronous follow-up where operationally required.
- **FR-012** Local doctors shall be able to record follow-up and outcomes.
- **FR-013** Cases shall support controlled closure.
- **FR-014** The system shall expose case lifecycle status.
- **FR-015** Authorised users shall be able to conduct clinical audit.
- **FR-016** The service shall support incident and near-miss reporting.
- **FR-017** The service shall support complaints.
- **FR-018** The service shall support authorised second opinions.
- **FR-019** Significant actions shall be recorded in an audit trail.
- **FR-020** The system shall provide operational and evaluation reporting.
- **FR-021** Core interfaces shall support Arabic and English.

## 12. Non-Functional Requirements

- **NFR-001 Low connectivity:** Core workflows must tolerate weak or intermittent connections.
- **NFR-002 Mobile-first:** Primary workflows must work effectively on low-cost Android devices.
- **NFR-003 Offline capability:** Selected workflows, especially case drafting, should function safely during disconnection.
- **NFR-004 Performance:** Network traffic and payload size should be minimised.
- **NFR-005 Security:** Sensitive data must be protected in transit and at rest.
- **NFR-006 Access control:** Users must only access information permitted by role and clinical context.
- **NFR-007 Auditability:** Material clinical and administrative actions must be traceable.
- **NFR-008 Data minimisation:** Only necessary data should be collected.
- **NFR-009 Confidentiality:** Information must be protected from unauthorised disclosure.
- **NFR-010 Usability:** Workflows should minimise clinician burden.

## 13. Data and Privacy

- Patient names should not normally be required.
- Unnecessary identifiers should not be collected.
- Consent must be recorded before relevant information is submitted.
- Access must be role-controlled.
- Data retention is TBD.
- Hosting location and data residency are TBD.
- Offline device storage requires a dedicated security decision.
- Applicable legal and cross-border requirements require qualified legal review.

## 14. Product Success Metrics

Pilot evaluation should include:

- cases submitted;
- participating facilities and clinicians;
- median response time;
- proportion answered within target;
- proportion where advice changed management;
- referrals avoided where measurable;
- outcomes where available;
- incidents, near misses, and complaints;
- user satisfaction;
- consultant retention;
- training activity;
- cost per case;
- proportion of costs covered by earned income.

## 15. Product Principles

- Patient safety
- Respect for local doctors
- Confidentiality
- Fairness
- Neutrality
- Evidence
- Accountability

## 16. Open Product Decisions

- Pilot specialty
- Pilot location and facilities
- Build vs Buy vs Partner
- Hosting and data residency
- Offline architecture
- Routing rules
- Identity assurance
- Notification channels
- Backup communication channel
- Data-retention policy
- Clinical coding approach
- Interoperability requirements
- Long-term ownership and operating model

## 17. Pilot Success Definition

Success is not merely processing a target number of cases.

The pilot should establish whether the model is clinically safe, operationally feasible, usable under real connectivity conditions, trusted by participants, measurable, financially understandable, and suitable for responsible expansion.
