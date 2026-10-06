# Non-Functional Requirements Catalog

**Version:** 0.1  
**Status:** Draft

The values below are initial engineering targets and must be validated against field conditions and operating model.

## Performance

### NFR-PERF-001
Core pages should become usable on constrained mobile connections without requiring large initial downloads.

### NFR-PERF-002
The application should minimise JavaScript bundle size and defer non-critical assets.

### NFR-PERF-003
Case submission must provide visible progress and recoverable retry for unreliable networks.

### NFR-PERF-004
Server-side API/application responses for ordinary non-upload actions should target p95 under 1 second under expected pilot load, excluding network latency.

## Availability

### NFR-AVL-001
Availability target must match a non-emergency service and be formally agreed before pilot.

### NFR-AVL-002
Planned maintenance must be communicated.

### NFR-AVL-003
Service status and approved fallback procedures must exist for outages.

## Reliability

### NFR-REL-001
Case submission retries must be idempotent.

### NFR-REL-002
Final advice submission must not produce duplicate final records on retry.

### NFR-REL-003
Background jobs must use retry and dead-letter/failure handling.

### NFR-REL-004
File upload completion must verify object integrity.

## Security

### NFR-SEC-001
All protected traffic uses TLS.

### NFR-SEC-002
Every protected server action enforces authorisation.

### NFR-SEC-003
Privileged roles use MFA.

### NFR-SEC-004
Production object storage is private.

### NFR-SEC-005
Material clinical/admin actions are auditable.

### NFR-SEC-006
Critical known vulnerabilities block production release unless formally risk accepted.

## Privacy

### NFR-PRV-001
Direct patient identifiers are not required by default.

### NFR-PRV-002
Monitoring/logging does not store full clinical narratives.

### NFR-PRV-003
Third-party integrations process only approved minimum data.

### NFR-PRV-004
Offline local data has defined expiry/removal behaviour.

## Usability

### NFR-UX-001
Core workflows must support mobile screens.

### NFR-UX-002
Arabic RTL and English LTR are supported.

### NFR-UX-003
Users can see case status and next required action.

### NFR-UX-004
Users can distinguish saved, unsynchronised, submitted, and failed states.

## Accessibility

### NFR-A11Y-001
Interactive controls are keyboard accessible where platform/browser supports it.

### NFR-A11Y-002
Form errors identify the field and corrective action.

### NFR-A11Y-003
Colour alone is not used to communicate critical status.

## Maintainability

### NFR-MNT-001
Core domain logic has automated tests.

### NFR-MNT-002
Architecture decisions are recorded through ADRs.

### NFR-MNT-003
Application modules have documented ownership/boundaries.

### NFR-MNT-004
Production deployments are traceable to source commits.

## Recoverability

### NFR-REC-001
Database backup restoration is tested before pilot.

### NFR-REC-002
RPO and RTO are documented before live service.

### NFR-REC-003
Fallback workflow can be reconciled after recovery.

## Scalability

### NFR-SCL-001
Pilot architecture should scale horizontally at the application/worker tier without redesigning core domain logic.

### NFR-SCL-002
Do not introduce distributed architecture until proven load or organisational requirements justify it.

## Observability

### NFR-OBS-001
Critical application failures produce actionable alerts.

### NFR-OBS-002
Every request/job involved in a workflow can be correlated without logging sensitive content.

### NFR-OBS-003
Queue delay and upload failures are visible to operations.

## Validation Note

Numerical targets should be baselined during field testing under representative Sudan connectivity conditions rather than inferred from high-bandwidth laboratory testing.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
