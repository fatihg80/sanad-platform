# Event Contracts

**Version:** 0.1  
**Status:** Draft

## 1. Purpose

Define domain/application events used to decouple workflow side effects such as notifications, metrics, and audit processing.

## 2. Event Envelope

Every event should include:

- event_id;
- event_type;
- event_version;
- occurred_at;
- aggregate_type;
- aggregate_id;
- actor_id where appropriate;
- correlation_id;
- minimal payload.

## 3. Candidate Events

### CaseSubmitted v1
Payload candidates:
- case_id;
- specialty;
- service_category;
- submitting_facility_id;
- submitted_at.

Do not include full clinical narrative.

### CaseAssigned v1
- case_id;
- consultant_id;
- assigned_at;
- assigned_by.

### AdditionalInformationRequested v1
- case_id;
- request_id;
- requested_at;
- requested_by.

### FinalAdviceSubmitted v1
- case_id;
- advice_id;
- consultant_id;
- submitted_at.

Do not place full advice content on a general event bus unless a validated use case requires it.

### CaseClosed v1
- case_id;
- closed_at;
- closed_by.

### IncidentReported v1
- incident_id;
- severity;
- reported_at.

Do not expose incident narrative broadly.

## 4. Versioning

A consumer must not depend on undocumented fields.

Breaking payload changes require a new event version.

## 5. Delivery Semantics

Assume at-least-once delivery unless infrastructure proves otherwise.

Consumers must therefore be idempotent.

## 6. Privacy

Events should carry references and minimum metadata, not duplicate the clinical record.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
