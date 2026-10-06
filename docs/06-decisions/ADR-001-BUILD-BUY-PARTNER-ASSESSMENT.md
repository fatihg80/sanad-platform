# Build vs Buy vs Partner Assessment

**Document:** ADR-001 supporting assessment  
**Status:** Open, no final decision  
**Decision owner:** Founding team, with clinical, technology, legal, operations, and finance input

## 1. Decision Question

For the initial Sanad pilot, should the team:

1. **Build** a dedicated Sanad platform;
2. **Buy / Adapt** an existing telemedicine product;
3. **Partner** with an organisation that already operates suitable technology?

The founding prospectus currently leans toward adapting an existing secure platform for the pilot because building from scratch may be slower and more expensive.

That position should be tested, not assumed.

## 2. Decision Principle

The goal is not to choose the most technically interesting option.

The goal is to choose the option that can safely and credibly validate the Sanad service model with the lowest unacceptable risk.

## 3. Evaluation Criteria

Any candidate option should be scored against the same criteria.

### Clinical workflow
- Provider-to-provider rather than only doctor-to-patient
- Structured specialty-specific cases
- Asynchronous consultation
- Priority and routine cases
- Additional-information workflow
- Second opinion
- Outcome recording
- Audit
- Incident and complaint support

### Connectivity
- Weak-network performance
- Offline drafting
- Resumable uploads
- Low-bandwidth mobile experience
- Android compatibility

### Language and usability
- Arabic
- RTL
- English
- Mobile-first workflow
- Low training burden

### Security and privacy
- Encryption
- Contextual access controls
- Audit trail
- Private file storage
- Data minimisation
- Metadata controls
- Data export controls
- Hosting-region choice
- Backup controls
- Administrator-access boundaries

### Governance
- Professional verification
- Clinical audit
- Incident management
- Complaints
- Second opinion
- Governance reporting

### Data and evaluation
- Pilot metrics
- Export for approved evaluation
- Data ownership
- API access
- De-identification support
- Avoidance of vendor lock-in

### Operations
- Consultant availability
- Manual and rules-based routing
- Coordinator tools
- SLA tracking
- Notification control
- support model

### Legal and contractual
- Data controller / processor terms
- subprocessor transparency
- data residency
- international transfers
- sanctions implications
- exit rights
- data return and deletion
- indemnity boundaries

### Financial
- implementation cost
- licensing
- per-user or per-case cost
- hosting
- customisation
- integration
- support
- exit / migration cost
- expected 2-year total cost

### Strategic
- speed to pilot
- product control
- ability to evolve
- vendor dependency
- future national-scale options
- ability to preserve Sanad's identity and operating model

## 4. Option A: Build

### Advantages

- full control over workflow;
- can optimise specifically for Sanad;
- strong control over Arabic/RTL experience;
- data model aligned to evaluation;
- easier long-term differentiation;
- no forced product assumptions from another vendor;
- clearer ability to evolve into Sanad-owned intellectual property.

### Disadvantages

- engineering effort before pilot;
- security responsibility;
- operational responsibility;
- longer validation time if scope is not tightly controlled;
- risk of building features before the operating model is proven;
- requires sustained technology ownership.

### Build makes sense when

- no existing platform satisfies the critical requirements;
- customisation cost approaches custom-build cost;
- data/control requirements make vendor dependence unacceptable;
- the team has credible engineering and security capability;
- MVP scope can remain disciplined.

## 5. Option B: Buy / Adapt

### Advantages

- potentially faster deployment;
- existing clinical or telemedicine features;
- mature hosting and support may already exist;
- lower initial engineering burden;
- may have existing offline or low-resource capabilities.

### Disadvantages

- workflow mismatch;
- poor Arabic/RTL support;
- weak provider-to-provider model;
- limited control over offline behaviour;
- vendor access to sensitive data;
- licensing costs;
- customisation constraints;
- difficult data export;
- vendor lock-in;
- roadmap dependency.

### Buy / Adapt makes sense when

A product satisfies critical requirements with limited customisation and acceptable legal, security, and exit terms.

## 6. Option C: Partner

Partnering differs from ordinary software procurement.

A partner may contribute:

- platform;
- implementation;
- clinical-service experience;
- low-resource deployment expertise;
- training;
- research collaboration;
- operational support.

### Advantages

- access to expertise as well as software;
- potentially faster learning;
- reduced implementation risk;
- credible support for grant applications or institutional partnerships.

### Disadvantages

- governance and ownership can become unclear;
- Sanad may lose control over product direction;
- partner incentives may differ;
- data ownership and publication rights may become complicated;
- dependency may extend beyond software.

### Partner makes sense when

The relationship creates meaningful capability that Sanad cannot efficiently reproduce and the agreement preserves appropriate governance, data, branding, and exit rights.

## 7. MVP Reference Requirements

A candidate should not be accepted solely because it is called a telemedicine platform.

At minimum, the team should test whether it can support:

- verified professional users;
- doctor-to-doctor workflow;
- specialty case templates;
- weak connectivity;
- offline draft behaviour;
- clinical images;
- Arabic/English;
- priority/routine cases;
- routing;
- written specialist advice;
- outcome capture;
- audit logs;
- role/context access;
- clinical governance;
- data export;
- appropriate hosting and privacy terms.

## 8. Red Flags

Potential disqualifiers:

- no ability to control data location where required;
- vendor retains broad rights over clinical data;
- no reliable export or exit path;
- patient-direct workflow cannot be adapted;
- no meaningful audit trail;
- administrators automatically see all clinical data;
- no Arabic/RTL path;
- unusable on weak networks;
- offline mode stores uncontrolled sensitive data;
- licensing model becomes prohibitive at pilot scale;
- no transparency about subprocessors;
- unclear breach responsibilities;
- platform terms conflict with cross-border medical use.

## 9. Cost Comparison Model

The team should compare at least:

### Build
- product/design effort;
- engineering;
- security;
- hosting;
- maintenance;
- support;
- future development.

### Buy
- setup;
- licence;
- users/cases;
- customisation;
- support;
- integration;
- migration/exit.

### Partner
- platform cost;
- service fees;
- shared staffing;
- grant/funding implications;
- IP and data terms;
- long-term dependence.

A low first-year price can hide a high switching cost.

## 10. Evidence Required Before Decision

For each serious candidate:

1. product demonstration using Sanad's case workflow;
2. offline/weak-network test;
3. Arabic/RTL test;
4. security documentation;
5. data-flow diagram;
6. hosting regions;
7. subprocessor list;
8. data export demonstration;
9. audit-log demonstration;
10. contractual review;
11. support model;
12. implementation timeline;
13. full cost model;
14. reference customers where available.

## 11. Current Recommendation

**Do not choose yet.**

The correct next step is a short market and technical discovery against the documented requirements.

A reasonable provisional decision rule:

- If a platform satisfies the critical requirements with minor adaptation and acceptable legal/data terms, prefer **Buy/Partner for the pilot**.
- If available platforms require major workflow compromise, create unacceptable data/security constraints, or require expensive customisation, prefer a **tightly scoped custom MVP**.
- Regardless of option, preserve an explicit exit and data-portability path.

## 12. Decision Record Template

When evidence is available, ADR-001 should record:

- Decision
- Status
- Date
- Decision makers
- Options considered
- Evidence
- Trade-offs
- Consequences
- Exit strategy
- Review trigger

## Required Expert Review

**Level:** Blocking before implementation commitment.

**Experts required:**
- Technology Lead / Software Architect
- Security Specialist
- Privacy/DPO
- Clinical Governance representative
- Procurement / Commercial specialist
- Operations representative
- Legal Counsel for vendor/data terms

The final decision must be based on evidence from demonstrations, due diligence, TCO, exit/portability, legal/privacy review, and clinical workflow fit.
