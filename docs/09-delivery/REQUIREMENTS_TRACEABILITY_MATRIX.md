# Requirements Traceability Matrix

**Version:** 0.1  
**Status:** Draft

This matrix links product intent to system requirements, architecture, and verification.

| Product Need | SRS / Requirement | Architecture / Decision | Verification |
|---|---|---|---|
| Verified clinical users | FR-001/002, IAM requirements | Identity + Professional Verification modules | identity/verification feature tests |
| Role-restricted access | FR-003/004 | ADR-006 Contextual Authorisation | authorisation matrix tests |
| Structured case | FR-005/006 | Clinical Cases + template versioning | case validation tests |
| Clinical attachments | FR-007 | ADR-005 Object Storage | upload/security/integrity tests |
| Safe submission | FR-008 | Clinical Case aggregate | idempotency + validation tests |
| Case routing | FR-009 | Routing module | assignment/reassignment tests |
| Specialist advice | FR-010 | Clinical Advice module | advice submission/history tests |
| Follow-up discussion | FR-011 | integration boundary | workflow acceptance tests |
| Outcome capture | FR-012 | Outcomes module | outcome/closure tests |
| Case closure | FR-013/014 | state machine | transition tests |
| Clinical audit | FR-015 | Governance module | governance access/audit tests |
| Incidents | FR-016 | Incident aggregate | restricted-access tests |
| Complaints | FR-017 | Complaint aggregate | lifecycle tests |
| Second opinion | FR-018 | Governance/Advice | separate-opinion tests |
| Audit trail | FR-019 | audit architecture | append/history tests |
| Reporting | FR-020 | reporting views/read models | metric validation |
| Arabic/English | FR-021 | UI i18n architecture | RTL/LTR tests |
| Weak connectivity | NFR-001/003 | ADR-003 Offline Strategy | network simulation tests |
| Mobile first | NFR-002 | PWA/web UI | mobile usability tests |
| Security | NFR-005/006 | Security Architecture | ASVS-derived checklist + security tests |
| Auditability | NFR-007 | Audit module | audit coverage tests |
| Data minimisation | NFR-008/009 | privacy architecture | privacy review |
| Usability | NFR-010 | UX requirements | pilot usability testing |

## Traceability Rule

No critical pilot capability should reach production without:

1. requirement;
2. implementation owner;
3. architecture/design reference;
4. acceptance criteria;
5. verification evidence.

This matrix should evolve into issue/backlog links once implementation starts.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
