# Evidence Intake Register

**Version:** 1.1  
**Status:** Active  
**Last updated:** 2026-10-06

## Purpose

Provide one controlled index of evidence collected during the decision-closure phase.

Evidence is separated into:

- **Source / desk evidence**: prospectus, literature, official vendor/platform material;
- **Field evidence**: doctors, facilities, consultants, partners;
- **Expert evidence**: legal, clinical, security, privacy, research, commercial review.

A critical decision must not be closed using desk evidence alone where the decision depends on Sudan-specific field reality or professional judgement.

## Collected Source / Desk Evidence

| Evidence ID | Date | Source Type | Source | Topic | Specialty / Platform | Quality | Decisions Informed | Status |
|---|---|---|---|---|---|---|---|---|
| E-001 | 2026-09 | Founding source | Sanad Founding Team Prospectus v1.0 | Project model, candidate specialties, pilot assumptions | Sanad | High for founding intent | Scope, pilot design | Validated source |
| E-002 | 2026-10-06 | Official vendor | Intelehealth Technology | Provider-to-provider, open source, customisable, OpenMRS/FHIR | Intelehealth | High | ADR-001/platform shortlist | Validated |
| E-003 | 2026-10-06 | Official vendor | Intelehealth 2026 product upgrades | Low-bandwidth improvements, web portal, sync improvement, FHIR R4 | Intelehealth | High | ADR-001/connectivity | Validated |
| E-004 | 2026-10-06 | Official vendor | VSee pricing/features | Enterprise custom workflows, routing, SSO/MFA, async eConsult | VSee Enterprise | High | ADR-001/platform shortlist | Validated |
| E-005 | 2026-10-06 | Official vendor help | VSee eConsult documentation | Asynchronous eConsult can be submitted by patient or another provider | VSee Enterprise | High | Provider-to-provider/async fit | Validated |
| E-006 | 2026-10-06 | Official technical docs | CHT Offline-First documentation | Offline-first operation in intermittent/low connectivity | CHT | High | Offline architecture/vendor assessment | Validated |
| E-007 | 2026-10-06 | Official technical docs | CHT Users/Permissions | Configurable roles/permissions; offline users sync authorised data | CHT | High | Access/privacy/vendor assessment | Validated |
| E-008 | 2026-10-06 | Official technical docs | CHT data architecture | PouchDB on device + CouchDB replication | CHT | High | Device-loss/privacy/offline assessment | Validated |
| E-009 | 2026-10-06 | Official project source | OpenMRS 3.7.1 release, Aug 2026 | Active OpenMRS 3 maintenance/ecosystem | OpenMRS | High | Component/platform context | Validated |
| E-010 | 2026-10-06 | Peer-reviewed literature | Teledermatology systematic review/meta-analysis references in desk review | Async/store-and-forward diagnostic fit | Dermatology | Medium/High | Specialty shortlist | Validated desk evidence |
| E-011 | 2026-10-06 | Peer-reviewed literature | Tele-ultrasound/resource-limited review referenced in desk review | Remote image interpretation potential | Radiology | Medium | Specialty shortlist | Validated desk evidence |
| E-012 | 2026-10-06 | Peer-reviewed literature | Paediatric telemedicine in rural/remote LMIC review | Remote paediatric consultation potential | Paediatrics | Medium | Specialty shortlist | Validated desk evidence |
| E-013 | 2026-10-06 | Peer-reviewed literature | OB/GYN telehealth and maternal-health reviews | Telehealth potential with emergency-boundary complexity | OB/GYN | Medium | Specialty shortlist | Validated desk evidence |
| E-014 | 2026-10-06 | Peer-reviewed literature | Surgical telemedicine reviews | Consultation/follow-up potential; physical-exam limitations | General Surgery | Medium | Specialty shortlist | Validated desk evidence |
| E-015 | 2026-10-06 | Peer-reviewed literature | Provider-to-provider eConsult / asynchronous consultation reviews | Broad async specialist-support evidence | Internal Medicine / general eConsult | Medium/High | Specialty/model fit | Validated desk evidence |

## Planned Field Evidence

| Evidence ID | Source Type | Required Input | Decision(s) | Status |
|---|---|---|---|---|
| F-001+ | Local Doctors | Need, case mix, informal workflows, connectivity, outcome feasibility | Pilot specialty, UX, offline | Planned |
| F-100+ | Facilities | Case volumes, diagnostic resources, connectivity, coordinator readiness | Facility + specialty | Planned |
| F-200+ | Diaspora Consultants | Capacity, async suitability, exclusions, response windows | Specialty + rota | Planned |
| F-300+ | Vendor demonstrations | Sanad workflow, security, privacy, hosting, TCO, exit | ADR-001 | Planned |
| F-400+ | Legal / regulatory experts | Liability, professional eligibility, consent, data transfer | Legal blockers | Planned |
| F-500+ | Security/privacy experts | Threats, vendor/data model, offline risks | Platform/hosting/go-live | Planned |
| F-600+ | Research/public health experts | Outcome validity, bias, ethics, dataset | Pilot evaluation | Planned |

## Source Links for Platform Evidence

- E-002: https://intelehealth.org/technology/
- E-003: https://intelehealth.org/all-the-upgrades-for-our-intelehealth-app/
- E-004: https://vsee.com/pricing
- E-005: https://help.vsee.com/kb/articles/how-to-send-an-e-consult-patient
- E-006: https://docs.communityhealthtoolkit.org/technical-overview/concepts/offline-first/
- E-007: https://docs.communityhealthtoolkit.org/building/users/
- E-008: https://docs.communityhealthtoolkit.org/technical-overview/data/
- E-009: https://openmrs.org/openmrs-3-7-1-is-out/

Specialty literature URLs are retained in `PILOT_SPECIALTY_DESK_EVIDENCE_REVIEW.md`.

## Evidence Quality

### High
Documented, direct, current, and verifiable.

### Medium
Relevant and credible but indirect, context-limited, or not Sudan-specific.

### Low
Anecdotal, old, weakly applicable, or not independently verifiable.

Low-quality evidence may identify a question but should not close a critical decision alone.

## Evidence Status

- Planned
- Collected
- Validated
- Superseded
- Rejected

## Traceability Rule

Every final score in a specialty, facility, or vendor decision table must reference one or more Evidence IDs.

Desk evidence may support **screening**.

Field + expert evidence is required for **approval** where the decision depends on real operating conditions.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
