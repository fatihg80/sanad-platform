# Project Documentation Changelog

## 2026-10-04

### Repository foundation
- Established documentation-first repository structure.
- Added non-technical project README for clinical/public-health audiences.
- Added project status and glossary.

### Product and requirements
- Added PRD.
- Added SRS.
- Added access-control matrix.
- Added measurable non-functional requirements catalog.
- Added requirements traceability matrix.

### Clinical
- Added clinical workflow specification.
- Added initial clinical safety hazard log.

### Architecture
- Added draft C4 architecture.
- Added domain model.
- Added data architecture.
- Added API and integration principles.

### Security and privacy
- Added data classification and privacy requirements.
- Added threat model.
- Added security architecture.

### Architecture decisions
- Added Build vs Buy vs Partner assessment.
- Proposed Modular Monolith.
- Proposed limited offline strategy for MVP.
- Proposed PostgreSQL.
- Proposed private object storage.
- Proposed contextual authorisation on top of RBAC.

### Engineering and operations
- Added engineering standards.
- Added test strategy.
- Added CI/CD strategy.
- Added observability and monitoring plan.
- Added backup and disaster recovery plan.
- Added security incident response plan.

### Delivery
- Added MVP scope and delivery plan.
- Added product and technical roadmap.

### Governance
- Added decision and change governance.
- Preserved founding prospectus source notes separately from later engineering interpretation.


### Clinical and operational specification expansion
- Added specialty-agnostic clinical case template specification.
- Added professional verification workflow.
- Added response-time and escalation policy model.
- Added notification and escalation policy.
- Added audit event catalog.
- Added data-retention schedule template.
- Added pilot operations runbook.
- Added pilot UAT and acceptance plan.
- Added pilot support model.
- Added pilot training and onboarding plan.
- Added implementation backlog.


### Pilot selection and external discovery
- Added pilot specialty selection framework.
- Added partner and facility selection criteria.
- Added pilot evaluation protocol.
- Added minimum evaluation dataset.
- Added legal and regulatory question register.
- Added hosting and data-residency options analysis.
- Performed initial market discovery for Build vs Buy vs Partner.
- Added vendor discovery questionnaire and Sanad-specific demonstration scenario.
- Current discovery priority: Intelehealth first, CHT as strong offline-first alternative, VSee as commercial comparator, custom MVP retained as fallback.


### Governance, contracts, and baseline completion
- Added Scope Guardrails.
- Added Documentation Guide.
- Added Quality Management Plan.
- Added Stakeholder Communication Plan.
- Added RACI Matrix.
- Added active Risk, Assumptions, Dependency, Issue, and Decision registers.
- Added Master Register Index.
- Added Documentation Completeness Checklist.
- Added technical Contracts layer covering API, Event, Data, and Service contracts.
- Added Legal Agreement Requirements for qualified counsel.
- Added Environment Strategy and Configuration Management.
- Added Release Management Plan.
- Added Data Flow and Processing Inventory.
- Added DPIA template.
- Added pilot specialty and partner/facility scorecard templates.
- Added Go-Live Readiness Checklist and Launch Governance Pack.
- Marked the pre-implementation documentation baseline as substantially complete; remaining gaps require external evidence, approvals, vendor responses, or clinical/legal decisions.


### Expert engagement and evidence phase
- Established Expert Engagement Policy and central Expert Review Register.
- Added mandatory expert-review markers to clinical, legal, privacy, security, evaluation, access-control, retention, DPIA, and platform-decision documents.
- Added Project Manager Expert Action Plan and Expert Review Request Template.
- Updated README to explain the documentation-first method, expert involvement, and expected outcomes.
- Started evidence collection phase.
- Added official-source Platform Evidence Snapshot and Platform Evidence Matrix.
- Added Vendor Demonstration Script and evaluation matrix.
- Updated VSee evidence: Enterprise publicly supports asynchronous eConsult including provider-to-provider use.
- Added evidence-backed Pilot Specialty Desk Review and Specialty Evidence Questionnaire.
- Current desk evidence does not constitute specialty selection; local evidence and clinical expert review remain blocking.


### Multidisciplinary navigation, stakeholders, and implementation layer
- Added `docs/START_HERE.md` as the multidisciplinary documentation manual.
- Added role-specific reading paths for project management, clinical, legal, privacy, security, engineering, public health/research, and operations.
- Added Stakeholder Register and Stakeholder Engagement Matrix.
- Added Internal and External Factors Analysis using an internal-capability and PESTLE-style external context.
- Added explicit `12-implementation/` layer to connect approved requirements to development, testing, security assurance, deployment, and production handover.
- Clarified that `08-engineering` defines engineering standards, `09-operations` defines live-service operations, `10-delivery` defines stage/governance delivery, and `12-implementation` orchestrates execution order.
- Updated root README and documentation index so new contributors are directed to START_HERE first.


### Documentation simplification
- Removed the separate `12-implementation/` layer to avoid duplication and navigation complexity.
- Consolidated implementation lifecycle, development execution, test execution, security assurance, deployment, and production handover into `08-engineering/IMPLEMENTATION_PLAYBOOK.md`.
- Clarified the folder boundaries:
  - `08-engineering`: how the software is built, tested, secured, configured, deployed, and handed over.
  - `09-operations`: how the live service is operated.
  - `10-delivery`: how project stages, backlog, readiness, acceptance, and launch governance are managed.
- Added a clickable Documentation Map to the root README.
- Updated START_HERE and the documentation index to remove references to the retired implementation layer.


### Lifecycle reorder and field evidence instruments
- Reordered numbered documentation folders by actual dependency/workflow rather than creation date.
- New order: Governance → Product → Requirements → Clinical → Research/Evidence → Architecture → Security/Privacy → Decisions → Contracts → Delivery → Engineering/Implementation → Operations.
- Moved all affected files and updated root README, START_HERE, and document index.
- Added Local Doctor Evidence Form.
- Added Facility Evidence Form.
- Added Diaspora Consultant Evidence Form.
- Added central Evidence Intake Register with traceable Evidence IDs.
- Added Specialty Decision Evidence Table.
- Added Vendor Evidence Capture Form.
- Evidence scores must now reference collected Evidence IDs rather than unsupported judgement.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
