# Evidence Collection Plan

**Version:** 0.1  
**Status:** Active

## Purpose

Move Sanad from a documentation baseline to evidence-backed decisions without expanding the approved pilot scope.

## Workstream A: Pilot Specialty Evidence

Collect:

- local clinical need;
- likely case volume;
- emergency dependency;
- consultant supply;
- diagnostic information availability;
- local-doctor readiness;
- outcome measurability;
- partner support;
- connectivity burden.

Outputs:

- completed specialty scorecards;
- evidence summary;
- recommended primary and backup specialty.

**Required Expert Review:** Clinical Governance, relevant specialty experts, and Public Health/Evaluation.

## Workstream B: Partner / Facility Evidence

Collect:

- organisational legitimacy;
- clinical leadership;
- coordinator capacity;
- case volume;
- connectivity;
- device availability;
- data practices;
- safety/neutrality;
- evaluation readiness.

Outputs:

- facility scorecards;
- due-diligence summary;
- shortlist.

**Required Expert Review:** Clinical Governance, Operations, Compliance/Legal where relevant.

## Workstream C: Platform / Vendor Evidence

Priority order for discovery:

1. Intelehealth
2. Community Health Toolkit
3. Commercial comparator such as VSee
4. Custom Sanad MVP reference option

Collect:

- exact Sanad workflow fit;
- offline behaviour;
- Arabic/RTL;
- security;
- hosting/data residency;
- data export;
- auditability;
- implementation effort;
- support;
- TCO;
- exit path.

Outputs:

- evidence matrix;
- vendor scorecards;
- updated ADR-001.

**Required Expert Review:** Technology, Security, Privacy, Clinical, Procurement/Commercial.

## Workstream D: Legal and Regulatory Evidence

Use `LEGAL_AND_REGULATORY_QUESTION_REGISTER.md`.

Outputs:

- written advice;
- blocker classification;
- affected requirements/architecture;
- required agreements.

**Required Expert Review:** Qualified healthcare counsel, privacy counsel/DPO, sanctions/compliance, indemnity specialist.

## Workstream E: Hosting / Data Residency Evidence

Collect for candidate regions/providers:

- legal permissibility;
- DPA;
- subprocessors;
- support-access geography;
- backup geography;
- service availability for Sudan;
- encryption/key options;
- latency;
- cost;
- portability.

Outputs:

- hosting scorecard;
- final hosting ADR after platform decision.

**Required Expert Review:** Privacy, Legal, Security, Infrastructure/SRE.

## Field Collection Operating Sequence

### Step 1: Assign Evidence IDs

Before collection, reserve an ID range in `EVIDENCE_INTAKE_REGISTER.md`:

- F-001+ Local Doctors
- F-100+ Facilities
- F-200+ Consultants
- F-300+ Vendors
- F-400+ Legal/Regulatory Experts
- F-500+ Security/Privacy Experts
- F-600+ Research/Public Health Experts

### Step 2: Use the Correct Form

- Local doctor → `LOCAL_DOCTOR_EVIDENCE_FORM.md`
- Facility → `FACILITY_EVIDENCE_FORM.md`
- Consultant → `CONSULTANT_EVIDENCE_FORM.md`
- Vendor/platform → `../07-decisions/VENDOR_EVIDENCE_CAPTURE_FORM.md`
- Expert review → `../00-governance/EXPERT_REVIEW_REQUEST_TEMPLATE.md`

### Step 3: Do Not Collect Patient Data

Field discovery forms must not contain patient names, IDs, clinical images, or identifiable case narratives.

Use aggregate/approximate service information during discovery.

### Step 4: Record Provenance

For each response capture:

- respondent/source type;
- date;
- collector;
- evidence ID;
- whether information is direct or estimated;
- supporting document if available;
- evidence quality.

### Step 5: Validate Before Scoring

Evidence should be checked for:

- completeness;
- internal consistency;
- whether it represents current conditions;
- whether multiple respondents independently support the claim;
- potential conflict of interest.

### Step 6: Update Decision Tables

Validated evidence should update:

- `SPECIALTY_DECISION_EVIDENCE_TABLE.md`;
- partner/facility scorecards;
- `PLATFORM_EVIDENCE_MATRIX.md`;
- Vendor Evaluation Matrix;
- relevant Risk/Assumption/Decision registers.

### Step 7: Expert Interpretation

Weighted scores are decision aids, not automatic decisions.

Clinical, public-health, technology, security, privacy, commercial, and legal reviewers must interpret the evidence according to their authority.

## Evidence Handling

Every evidence item should record:

- source;
- date;
- source type;
- owner;
- reliability;
- decision(s) informed;
- whether independent verification is required.

## Stop Rule

Do not keep researching indefinitely.

A workstream is ready for decision when:

- critical questions have evidence;
- major risks are understood;
- alternatives are comparable;
- remaining uncertainty is explicitly accepted.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
