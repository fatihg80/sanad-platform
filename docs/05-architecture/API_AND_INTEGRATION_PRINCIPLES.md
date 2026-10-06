# API and Integration Principles

**Version:** 0.1  
**Status:** Draft

## 1. Purpose

Define how Sanad should expose and consume interfaces without over-engineering the pilot.

## 2. MVP Principle

The initial application may be a modular monolith, but module boundaries and external interfaces should be explicit enough to support future integrations.

Do not create microservices merely to claim API-first architecture.

## 3. API Rules

External APIs should:

- use HTTPS;
- require authentication;
- enforce server-side authorisation;
- validate request schemas;
- avoid sensitive data in URLs;
- use stable identifiers;
- use pagination;
- define error formats;
- support idempotency for retry-sensitive writes;
- rate limit;
- version deliberately.

## 4. Internal Module Interfaces

Modules should interact through:

- application services;
- domain events;
- explicit interfaces.

Avoid arbitrary cross-module database writes.

## 5. Idempotency

Idempotency is important for weak-network conditions.

Operations that may be retried must avoid accidental duplication, especially:

- case submission;
- advice submission;
- outcome submission;
- file finalisation.

## 6. Correlation IDs

Requests and asynchronous jobs should carry a correlation ID for troubleshooting.

Correlation IDs must not contain sensitive business meaning.

## 7. Webhooks

If webhooks are introduced:

- sign payloads;
- retry safely;
- record delivery state;
- minimise payload;
- rotate signing secrets;
- verify destination ownership.

## 8. Third-Party Integrations

Every integration requires documentation of:

- purpose;
- data shared;
- lawful/approved basis;
- authentication;
- failure mode;
- retry behaviour;
- monitoring;
- retention;
- vendor exit.

## 9. Notification Interfaces

Notification services should receive only the minimum information needed.

Clinical content should not be placed in email/SMS/push payloads unless explicitly approved.

## 10. Future Healthcare Interoperability

FHIR or other healthcare standards may become relevant for:

- hospital integration;
- patient identifiers;
- observations;
- diagnostic reports;
- practitioner/facility data.

Do not implement FHIR before a real interoperability use case exists.

## 11. API Documentation

Approved external APIs should have:

- machine-readable specification where practical;
- authentication documentation;
- examples using synthetic data;
- version and deprecation policy;
- security considerations.

## 12. Deprecation

Breaking external API changes require:

- versioning;
- notice;
- migration guidance;
- defined retirement date.

## 13. Integration Failure Principle

External service failure must not silently corrupt clinical workflow.

The system must distinguish:

- request failed;
- delivery unknown;
- confirmed delivered;
- retry scheduled.

## 14. Open Decisions

- whether MVP exposes any public/partner API;
- identity federation;
- notification providers;
- video/voice integration;
- research export interface;
- future FHIR profile requirements.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
