# Build vs Buy vs Partner, Market Discovery

**Version:** 0.1  
**Status:** Market discovery, not a procurement decision  
**Date:** 2026-10-04

## 1. Purpose

Evaluate currently visible platform options against Sanad's actual pilot requirements.

This document supplements ADR-001. It does not replace a formal vendor demonstration, security review, legal review, cost model, or contract assessment.

## 2. Sanad Critical Requirements

A serious candidate must be assessed for:

- provider-to-provider workflow;
- asynchronous structured cases;
- weak/unstable connectivity;
- mobile-first experience;
- safe offline behaviour;
- Arabic/RTL feasibility;
- clinical images/documents;
- routing;
- written specialist advice;
- outcomes;
- auditability;
- professional verification;
- governance workflows;
- role/context-based access;
- data export;
- hosting/data-residency control;
- low vendor lock-in;
- sustainability beyond the pilot.

## 3. Candidate 1: Intelehealth

### Current public evidence

Intelehealth describes its platform as:

- open source;
- designed for low-resource settings;
- suitable for low-bandwidth operation;
- provider-to-provider capable;
- customisable;
- based on an Android health-worker application and web interface;
- backed by OpenMRS;
- interoperable using HL7/FHIR-related capabilities.

In 2026, Intelehealth reported:

- improved low-bandwidth teleconsultation;
- a web-based health-worker portal;
- improved application stability;
- substantially reduced initial sync time;
- FHIR R4-compliant data capture.

### Sanad Fit

**Strong potential fit**

Reasons:

- closest visible match to provider-to-provider tele-expertise;
- designed for low-resource health systems;
- existing low-bandwidth experience;
- open-source/customisable model;
- existing teleconsult workflow;
- likely stronger starting point than a generic EMR.

### Questions requiring validation

- Is Arabic/RTL fully supported or realistically configurable?
- Can patient-direct assumptions be removed from the workflow?
- Can Sanad use doctor-to-doctor structured cases without CHW/task-shifting assumptions?
- What exactly is stored offline?
- Can clinical governance, incident, second-opinion, and outcome workflows be implemented?
- Can Sanad control hosting region and database/object storage?
- What data does Intelehealth or implementation partners access?
- What are support/customisation costs?
- What are the exact open-source license boundaries?
- What is the migration/exit path?

### Discovery position

**Highest-priority candidate for a live technical/product demonstration.**

## 4. Candidate 2: Community Health Toolkit (CHT)

### Current public evidence

The Community Health Toolkit is:

- open source;
- designed for health systems in low-infrastructure environments;
- explicitly offline-first;
- usable across smartphones, tablets, computers, and some SMS workflows;
- configurable for roles, permissions, workflows, messaging, tasks, and analytics.

Its offline architecture uses local device data with later synchronisation, historically through CouchDB/PouchDB patterns.

### Sanad Fit

**Strong infrastructure/workflow fit, weaker direct product fit**

Strengths:

- outstanding offline-first design;
- mature experience in unreliable connectivity;
- configurable permissions and health workflows;
- large deployment footprint.

Potential mismatch:

- primary design centre is community health/frontline health-worker workflows, not specialist tele-expertise;
- Sanad would likely require significant custom workflow design for consultant assignment, advice, governance, second opinion, and professional verification.

### Key risk

CHT's strength, synchronising accessible data to offline devices, must be carefully assessed against Sanad's conflict-environment privacy and device-loss risk.

### Discovery position

**Worth technical evaluation if offline capability becomes the dominant requirement, but not currently the first candidate for Sanad's complete pilot workflow.**

## 5. Candidate 3: VSee

### Current public evidence

VSee offers:

- commercial telehealth platform;
- video, chat, scheduling, waiting rooms;
- customisable enterprise workflows;
- APIs/SDKs;
- multi-provider support on higher plans;
- MFA/SSO options;
- HIPAA-oriented security controls;
- enterprise/federal deployment positioning.

### Sanad Fit

**Potential commercial fit, but significant discovery required**

Strengths:

- mature telehealth product;
- multi-provider workflows;
- APIs;
- strong video/communications capabilities;
- mature enterprise security posture.

Potential mismatch:

- public product model is strongly patient-provider/virtual-clinic oriented;
- offline-first support is not established in the public material reviewed;
- cost and licensing may be material;
- Sanad's provider-to-provider asynchronous structured-case workflow may require customisation;
- data residency and cross-border availability need validation.

### Discovery position

**Secondary commercial candidate. Worth a vendor conversation, but not enough evidence yet to prefer it over Intelehealth for Sanad.**

## 6. Candidate 4: OpenMRS

### Current public evidence

OpenMRS is a mature open-source EMR platform with:

- configurable clinical data model;
- REST API;
- FHIR module;
- large global-health ecosystem;
- current OpenMRS 3 reference application.

### Sanad Fit

**Good underlying clinical-record foundation, weak direct tele-expertise fit**

Strengths:

- strong health-data model;
- mature ecosystem;
- open source;
- extensible;
- interoperability path.

Limitations for Sanad:

- not itself a complete provider-to-provider tele-expertise product;
- routing, consultant advice workflow, low-connectivity mobile experience, governance, and offline behaviour would require substantial design;
- using OpenMRS alone may produce more adaptation work than a Sanad-specific MVP.

### Discovery position

**Useful as a component/foundation, especially because Intelehealth itself uses OpenMRS, but not the leading standalone answer for the pilot.**

## 7. Initial Comparative View

| Criterion | Intelehealth | CHT | VSee | OpenMRS |
|---|---|---|---|---|
| Provider-to-provider alignment | Strong | Custom work | Unclear/Custom | Custom work |
| Low bandwidth | Strong public evidence | Strong | Needs validation | Depends on implementation |
| Offline-first | Some evidence / validate exact scope | Very strong | Unknown from reviewed public material | Not primary strength |
| Structured health workflow | Strong | Strong/configurable | Strong clinic workflows | Strong data/workflow foundation |
| Teleconsultation | Strong | Custom | Strong | Custom |
| Open source | Yes | Yes | No/commercial | Yes |
| Customisation | Strong | Strong | Enterprise-dependent | Strong |
| Arabic/RTL | Validate | Likely configurable, validate | Validate | Custom |
| Clinical governance fit | Customise | Customise | Customise | Customise |
| Data residency control | Validate | Strong if self-hosted | Validate contractually | Strong if self-hosted |
| Sanad-specific build effort | Medium | Medium/High | Unknown | High |
| Pilot discovery priority | 1 | 2 | 3 | 4 as standalone |

This ranking is provisional and based only on currently reviewed public evidence.

## 8. Recommended Next Action

### Step 1: Intelehealth deep-dive

Request a demo specifically around a Sanad scenario:

1. doctor in Sudan creates structured specialist case;
2. case stored during weak connectivity;
3. sync after connection returns;
4. coordinator routes to consultant;
5. consultant provides asynchronous written advice;
6. doctor reports outcome;
7. governance user audits case;
8. data exported for evaluation.

Do not accept a generic telemedicine sales demo.

### Step 2: CHT technical spike

Test whether Sanad's exact case/consultant workflow can be modelled without fighting CHT's community-health assumptions.

### Step 3: VSee vendor qualification

Ask directly about:

- asynchronous provider-to-provider case workflow;
- offline support;
- hosting/data regions;
- Arabic/RTL;
- customisation cost;
- data export;
- API access;
- pricing for the pilot population.

### Step 4: Keep Custom MVP option alive

Do not abandon the custom MVP reference architecture until vendor demonstrations establish that one of the platforms meets the critical requirements without unacceptable compromise.

## 9. Decision Gate

A platform should not win because it has:

- the most features;
- the best demo;
- the most certifications;
- the lowest headline price.

It should win because it best supports:

1. the Sanad clinical operating model;
2. low-connectivity reality;
3. safety/privacy;
4. pilot speed;
5. evaluation;
6. sustainable ownership and exit.

## 10. Current Recommendation

**Prioritise Intelehealth for formal discovery, keep CHT as the strongest offline-first alternative/framework, qualify VSee as a commercial comparator, and retain the custom MVP as a credible fallback.**

No final Build/Buy/Partner decision should be made until:

- workflow demo completed;
- technical architecture reviewed;
- offline behaviour tested;
- security/privacy reviewed;
- Arabic/RTL tested;
- hosting/data residency confirmed;
- cost/TCO known;
- exit/data portability demonstrated.

## 11. Public Sources Reviewed

- Intelehealth technology and 2026 product updates
- Intelehealth open-source repository/material
- Community Health Toolkit technical documentation
- Medic 2026 strategy/architecture material
- VSee platform and pricing/security information
- OpenMRS current product and release information

Source URLs and evidence should be refreshed before procurement because product capabilities and pricing can change.
