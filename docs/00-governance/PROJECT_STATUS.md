# Project Status

## Project

Sanad

## Current Stage

Foundation, discovery, architecture, security design, and pilot planning.

## Source of Truth

The initial project basis is the September 2026 **Sanad Founding Team Prospectus v1.0**.

The repository deliberately distinguishes:

- source-derived statements;
- later product requirements;
- engineering proposals;
- clinical/legal dependencies;
- unresolved decisions.

## Completed Work

### Project and product
- Founding prospectus reviewed and preserved as source notes
- Project document classified as a founding prospectus / concept document, not an RFP and not a complete PRD
- Product Requirements Document drafted
- Software Requirements Specification drafted
- Risk, opportunity, stakeholder, and external-factor analysis completed
- Glossary and decision/change governance added

### Clinical
- Clinical Workflow Specification drafted
- Case lifecycle and escalation model drafted
- Initial Access Control Matrix drafted
- Initial Clinical Safety Hazard Log drafted

### Architecture
- Candidate C4 architecture drafted
- Domain model drafted
- Data architecture drafted
- API and integration principles drafted
- Modular Monolith proposed for custom MVP
- PostgreSQL proposed as primary relational datastore
- Private object storage proposed for clinical files
- Contextual authorisation proposed on top of RBAC
- Limited offline strategy proposed for MVP

### Security and privacy
- Data classification and privacy requirements drafted
- Threat model drafted
- Security architecture drafted
- Security incident-response plan drafted

### Engineering
- Engineering standards drafted
- Test strategy drafted
- CI/CD strategy drafted
- Measurable NFR catalog drafted
- Requirements traceability matrix established

### Operations
- Observability and monitoring plan drafted
- Backup and disaster-recovery plan drafted

### Delivery
- MVP scope and delivery slices drafted
- Product and technical roadmap drafted
- Build vs Buy vs Partner assessment drafted

## Current Workstream

The pre-implementation documentation foundation is now substantially established.

The project can move into evidence-backed platform/vendor discovery, specialty-specific clinical design, pilot partner discovery, and implementation planning without losing traceability.

## Next Planned Work

1. Define pilot specialty decision framework and specialty-specific template
2. Perform actual market/vendor research for Build vs Buy vs Partner
3. Define pilot partner/facility selection criteria
4. Define evaluation protocol and minimum dataset
5. Define legal/regulatory question register for counsel
6. Define hosting/data-residency options for legal/privacy review
7. Convert implementation backlog into GitHub issues after platform decision
8. Finalise technology stack ADRs after Build/Buy/Partner decision
9. Produce deployment architecture for the selected hosting/platform option
10. Prepare pilot go-live checklist and launch governance pack

## Key Decisions Still Open

- Pilot specialty
- Pilot state and facilities
- Final legal entity and operating jurisdiction
- Platform ownership model
- Build vs Buy vs Partner
- Hosting provider, region, and data residency
- Authentication provider and MFA method
- Final offline data-storage approach
- Consultant availability model
- Routing model
- Response-time clock and service hours
- Clinical coding standards
- Data retention periods
- Notification channels
- Approved backup communication channels
- Long-term interoperability approach
- Research dataset governance
- Production support-access model

## Major External Dependencies

The following cannot be resolved by engineering alone:

- clinical governance approval;
- specialty-specific workflow design;
- legal liability model;
- professional registration requirements;
- data-protection/legal basis;
- cross-border data transfer requirements;
- sanctions/payment review;
- partner/facility agreements;
- research ethics requirements;
- funding and operational staffing.

## Documentation Principle

No unresolved assumption should silently become a requirement.

Every material decision should be traceable to:

- source evidence;
- stakeholder approval;
- an ADR;
- or an explicit TBD.

## Readiness Position

The project is **not yet ready for production clinical implementation**.

It is ready for:

- structured clinical discovery;
- vendor/platform assessment;
- pilot operating-model design;
- detailed technical planning;
- backlog preparation.

Production implementation should begin only after the critical open decisions are narrowed sufficiently to avoid expensive rework or unsafe assumptions.
