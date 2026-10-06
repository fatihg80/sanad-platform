# Clinical Safety Hazard Log

**Version:** 0.1  
**Status:** Draft for clinical governance review

This is not a substitute for formal clinical-safety assessment. It is an initial engineering and governance hazard register.

| ID | Hazard | Potential Harm | Initial Risk | Candidate Controls |
|---|---|---|---|---|
| H-01 | Priority case routed slowly | Delayed care | High | priority flag, routing alerts, escalation |
| H-02 | User assumes Sanad is emergency service | Delay seeking emergency care | Critical | clear boundary messaging, no emergency category |
| H-03 | Wrong consultant assigned | Inappropriate advice/delay | High | specialty eligibility, coordinator review, reassignment |
| H-04 | Consultant sees incomplete case | Advice based on missing data | High | required fields, attachment completeness, info request |
| H-05 | Stale offline draft overwrites newer data | Incorrect clinical information | Critical | explicit conflict handling, idempotency, timestamps |
| H-06 | Duplicate case created after retry | Conflicting advice/work | Medium/High | idempotency key, duplicate warning |
| H-07 | Image compression degrades diagnostic quality | Misinterpretation | Critical | clinically validated transforms, preserve original where required |
| H-08 | Advice silently edited after submission | Unsafe/unauditable decision | Critical | immutable final advice, addendum model |
| H-09 | Notification not delivered | Delayed review | High | delivery status, dashboard queue, escalation |
| H-10 | Local doctor interprets advice as mandatory order | Inappropriate care | High | wording/UI reinforces local responsibility |
| H-11 | Timezone/SLA logic wrong | Missed escalation | High | UTC storage, defined service timezone, tests |
| H-12 | Wrong patient/case attachment | Incorrect advice | Critical | attachment confirmation, clear case context |
| H-13 | Second opinion overwrites first | Loss of clinical history | High | separate opinion records |
| H-14 | Outage drives unmanaged WhatsApp workflow | Missing documentation/privacy breach | High | approved fallback procedure, reconciliation |
| H-15 | User account shared | Loss of accountability | High | individual accounts, MFA, policy/training |
| H-16 | Sensitive clinician location exposed | Physical safety threat | Critical | data minimisation, metadata controls |

## Required Review

For each hazard before pilot:

- confirm severity;
- assess likelihood;
- assign owner;
- confirm controls;
- define test/verification evidence;
- identify residual risk;
- record acceptance authority.

## Safety Decision Rule

A feature that improves convenience but materially increases clinical risk should not be accepted merely to meet MVP schedule.

## Review Triggers

Update when:

- specialty changes;
- case template changes;
- routing changes;
- offline scope changes;
- image processing changes;
- notifications change;
- direct patient service is considered;
- serious incident occurs.

## Required Expert Review

**Level:** Blocking before pilot go-live.

**Experts:** Clinical Governance, Pilot Specialty Lead, Patient Safety/Quality expert where available, Technology/Security for technical hazards.

Each hazard must have an owner, control evidence, residual-risk rating, and accountable acceptance before go-live.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
