# Project Status

## Project

Sanad

## Current Stage

Pre-implementation documentation baseline substantially complete. Active phase: evidence collection, expert engagement, and decision closure.

## Source of Truth

The initial project basis is the September 2026 **Sanad Founding Team Prospectus v1.0**.

The repository deliberately distinguishes:

- source-derived statements;
- later product requirements;
- engineering proposals;
- clinical/legal dependencies;
- unresolved decisions.

## Baseline Completed

### Product and scope
- PRD
- scope guardrails
- MVP definition
- roadmap
- implementation backlog

### Requirements
- SRS
- functional requirements
- measurable NFR catalog
- access-control matrix
- requirements traceability matrix

### Clinical
- clinical workflow
- generic case-template specification
- professional verification workflow
- response-time/escalation policy model
- clinical safety hazard log
- pilot specialty selection framework

### Architecture
- C4 candidate architecture
- domain model
- data architecture
- API/integration principles
- architecture decision records

### Security and privacy
- data classification and privacy requirements
- threat model
- security architecture
- data-flow inventory
- audit-event catalog
- DPIA template
- retention template
- hosting/data-residency options

### Engineering & implementation
- engineering standards
- Engineering & Implementation Playbook
- test strategy
- CI/CD strategy
- environment strategy
- configuration management

### Operations
- observability and monitoring
- backup/disaster recovery
- security incident response
- notification policy
- operations runbook
- support model
- training/onboarding
- release management

### Evaluation
- pilot evaluation protocol
- minimum evaluation dataset
- UAT/acceptance plan

### Governance
- multidisciplinary documentation manual / Start Here
- stakeholder register and engagement matrix
- internal/external factors analysis
- expert engagement policy and expert review register
- risk register
- assumptions register
- dependency register
- issue register
- decision register
- RACI
- quality management plan
- stakeholder communication plan
- documentation guide
- change governance
- changelog
- go-live readiness checklist
- launch governance pack

### Contracts
- technical contract architecture
- API/event/data/service contract foundations
- legal agreement requirements for counsel

### Procurement / platform discovery
- Build vs Buy vs Partner assessment
- initial market discovery
- vendor discovery questionnaire
- hosting/data residency options

## Documentation Lifecycle Order

The numbered folders now reflect the intended dependency and working sequence:

```text
00 Governance
01 Product
02 Requirements
03 Clinical
04 Research & Evidence
05 Architecture
06 Security & Privacy
07 Decisions
08 Contracts
09 Delivery
10 Engineering & Implementation
11 Operations
```

The numbering is a navigation aid, not a claim that each layer stops when the next begins. Governance, evidence, security, delivery, and operations continue across multiple phases.

## Remaining Work That Requires Real-World Evidence

These items are intentionally not “completed” by writing more documents because they depend on external evidence or accountable decisions:

1. Select pilot specialty using real survey/facility/consultant evidence
2. Create specialty-specific case template
3. Select pilot facilities and partners
4. Complete vendor demonstrations and technical due diligence
5. Obtain cost/TCO proposals
6. Close ADR-001 Build vs Buy vs Partner
7. Obtain qualified legal/regulatory advice
8. Finalise consultant indemnity and professional eligibility rules
9. Finalise data-controller/processor roles
10. Finalise hosting/data-residency decision
11. Complete DPIA if required
12. Finalise retention periods
13. Obtain ethics/research determination
14. Execute consultant/facility/vendor/data agreements
15. Produce final deployment architecture after platform selection
16. Convert backlog to implementation GitHub issues after platform decision
17. Perform build/adaptation and pilot UAT
18. Complete final go-live governance review

## Expert Engagement Rule

Any decision outside the competence of the core project team is now explicitly marked for expert review.

The Project Manager should use `EXPERT_REVIEW_REGISTER.md` to engage the relevant clinical, legal, privacy, security, research, finance, compliance, insurance, UX, infrastructure, or informatics specialist before the corresponding gate is approved.

Absence of expert feedback is not approval.

## Project Origin, Consulting Role, and IP Governance

The repository now explicitly separates the **Sanad project origin** from the **consulting documentation contribution**.

- **Dr. Elaf Sabri Khalil** is identified from the founding materials as the **Founder of Sanad** and the source associated with the **Sanad Founding Team Prospectus**.
- **Alfatih Abdalla** contributed in a **consulting capacity** after being engaged by Dr. Elaf. His role is limited to structuring this repository, defining its documentation layers and methodology expression, and providing product/technical analysis based on Dr. Elaf's source materials.
- Alfatih Abdalla is not represented as the founder or owner of Sanad.

Added:

- `AUTHORS.md`;
- `NOTICE.md`;
- `CONTRIBUTING.md`;
- standard Project & Documentation Attribution across Markdown documentation;
- ER-28 for IP/contributor/licensing review;
- DEC-014 for the future repository licence, contributor IP terms, and any assignment to a Sanad legal entity.

Final legal ownership/licensing questions remain subject to explicit agreements and qualified IP/legal review.

## Evidence Collection Started

Completed in the current evidence phase:

- official-source platform evidence snapshot;
- evidence-based platform matrix;
- updated discovery position for Intelehealth, VSee Enterprise, CHT, OpenMRS, and Custom MVP;
- specialty literature desk review;
- field specialty evidence questionnaire;
- vendor demonstration script;
- expert engagement action plan;
- local doctor evidence form;
- facility evidence form;
- diaspora consultant evidence form;
- evidence intake register with traceable Evidence IDs;
- specialty decision evidence table;
- vendor evidence capture form;
- populated desk/source Evidence IDs E-001 through E-015;
- platform matrix linked to Evidence IDs;
- specialty decision table linked to literature Evidence IDs while field scoring remains pending.

The specialty desk review is preliminary and explicitly requires local Sudan evidence and clinical expert review before selection.

### Field Evidence Batch 01 opened

Operational collection is now open with reserved IDs:

- F-001 to F-010: Local Doctors
- F-100 to F-102: Candidate Facilities
- F-200 to F-205: Diaspora Consultants
- F-300+: Vendor/platform demonstrations

GitHub execution issues have been opened for each collection stream. No field responses or scores are recorded until real evidence is received and validated.

## Current High-Priority Sequence

1. Clinical needs and specialty evidence
2. Partner/facility discovery
3. Intelehealth deep-dive and vendor/platform comparisons
4. Legal/regulatory consultation
5. Hosting/data residency narrowing
6. Final Build/Buy/Partner decision
7. Final implementation architecture
8. Implementation backlog → GitHub issues/milestones
9. Build/adapt platform
10. Pilot readiness and go-live

## Key Open Decisions

- pilot specialty
- partner facilities
- final legal entity/operating jurisdiction
- platform ownership model
- Build vs Buy vs Partner
- hosting provider/region/data residency
- authentication/MFA implementation
- final offline scope
- routing model
- service hours/SLA clock
- clinical coding standards
- retention periods
- notification providers/channels
- fallback communication channel
- research governance
- production support-access model

## External Dependencies

Engineering cannot close these alone:

- clinical governance approval;
- specialty decisions;
- professional eligibility/regulatory confirmation;
- legal liability;
- privacy/legal basis;
- cross-border data transfer;
- sanctions/payment review;
- facility/partner agreements;
- ethics determination;
- funding/staffing.

## Readiness Position

The **pre-implementation documentation baseline is substantially complete**.

The next maturity step is not to create more speculative documents. It is to populate and approve the existing frameworks using real clinical, operational, legal, vendor, and partner evidence.

See `DOCUMENTATION_COMPLETENESS_CHECKLIST.md` for the current completeness assessment.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
