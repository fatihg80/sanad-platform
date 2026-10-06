# Implementation Backlog

**Version:** 0.1  
**Status:** Draft  
**Purpose:** Convert approved documentation into buildable work when the implementation path is selected.

## Epic 0: Project Foundation

- Initialise application architecture
- Configure environments
- Configure CI/CD
- Configure secrets management
- Configure logging/monitoring
- Define coding standards in repository
- Add baseline security headers
- Establish synthetic test data

## Epic 1: Identity and Access

- User registration/invitation
- Login/logout
- MFA
- account states
- role management
- contextual authorisation policies
- session revocation
- account recovery
- audit identity events

## Epic 2: Professional Verification

- professional profile
- registration records
- evidence upload
- verification review queue
- request more information
- approve/reject
- expiry/reverification
- suspension/reinstatement
- verification audit history

## Epic 3: Facilities

- facility registry
- facility activation/suspension
- doctor-facility relationship
- safety-aware location fields
- partner metadata

## Epic 4: Clinical Templates

- template model
- template versioning
- structured fields
- specialty extension
- publish/retire
- validation rules
- Arabic/English labels

## Epic 5: Case Drafting and Submission

- create draft
- edit draft
- consent confirmation
- structured case fields
- privacy warnings
- attachment upload
- submission validation
- permanent case reference
- idempotent submission
- audit events

## Epic 6: Low-Connectivity Support

- local draft model
- sync status UI
- retry queue
- conflict handling
- duplicate prevention
- local-data expiry
- network-state feedback

## Epic 7: Routing

- submitted queue
- consultant eligibility
- coordinator assignment
- consultant accept/decline
- reassignment
- routing history
- priority indicator
- escalation hooks

## Epic 8: Consultant Review

- assigned-case view
- request additional information
- doctor response
- advice draft
- final advice
- advice addendum
- synchronous-discussion record
- advice audit history

## Epic 9: Outcome and Closure

- outcome form
- evaluation fields
- closure validation
- close case
- reopen under permission
- closure audit

## Epic 10: Governance

- second opinion
- clinical audit
- incident reporting
- incident restricted access
- complaint workflow
- corrective action
- governance dashboard

## Epic 11: Notifications

- in-app notifications
- provider abstraction
- assignment notification
- additional-information notification
- advice notification
- SLA alerts
- delivery status
- retry/failure dashboard
- Arabic/English templates

## Epic 12: Audit and Security

- audit-event store
- privileged-event capture
- export audit
- break-glass architecture if approved
- rate limits
- file validation
- security telemetry
- access review tooling

## Epic 13: Reporting and Evaluation

- case volume
- response-time metrics
- target compliance
- outcome metrics
- consultant activity
- facility metrics
- safe governance metrics
- approved research export pipeline

## Epic 14: Operations

- health checks
- monitoring dashboards
- alerting
- backup automation
- restore testing
- incident runbooks
- status communication process

## Epic 15: Pilot Readiness

- UAT
- Arabic/RTL QA
- mobile/weak-network QA
- security review
- penetration test where feasible
- backup restore exercise
- incident tabletop
- onboarding materials
- pilot support rota
- go-live checklist

## Prioritisation Rule

Prioritise by:

1. patient/clinician safety;
2. pilot-critical workflow;
3. security/privacy;
4. operational reliability;
5. evaluation needs;
6. convenience features.

## Backlog Rule

No backlog item should be accepted as implementation-ready unless it links to:

- requirement;
- acceptance criteria;
- role/authorisation expectation;
- data classification;
- relevant architecture decision.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
