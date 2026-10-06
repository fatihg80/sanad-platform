# Decision and Change Governance

**Version:** 0.1  
**Status:** Draft

## 1. Purpose

Prevent product, clinical, legal, and technical decisions from becoming implicit or contradictory.

## 2. Decision Types

### Clinical
Examples:

- case template;
- priority criteria;
- closure criteria;
- emergency wording.

Owner: Clinical Governance / Specialty Lead.

### Product
Examples:

- scope;
- user workflow;
- pilot success metrics.

Owner: Product/Founding team with relevant stakeholders.

### Architecture
Examples:

- datastore;
- offline strategy;
- hosting;
- identity provider.

Owner: Technology Lead, with security/privacy input.

### Security/Privacy
Examples:

- MFA;
- retention;
- logging;
- vendor data access.

Owner: Security/privacy authority with legal input.

### Legal/Regulatory
Examples:

- lawful basis;
- liability;
- sanctions;
- cross-border transfer.

Owner: qualified legal/compliance advisers.

## 3. ADR Rule

Use an ADR when a technical decision:

- has material long-term consequences;
- has credible alternatives;
- affects security, privacy, scale, or operations;
- would be expensive to reverse.

## 4. Change Impact

A material change should be assessed against:

- PRD;
- SRS;
- clinical workflow;
- safety hazard log;
- privacy;
- threat model;
- architecture;
- testing;
- operations.

## 5. Versioning

Documents should carry:

- version;
- status;
- date where useful.

Statuses:

- Draft
- Proposed
- Approved
- Superseded
- Retired

## 6. Approval

Not every document requires the same approver.

Examples:

- clinical workflow requires clinical approval;
- architecture requires technology/security approval;
- legal positions require legal validation;
- pilot go-live requires cross-functional approval.

## 7. No Silent Assumptions

If a point is unknown, mark it TBD.

Do not convert an engineering preference into a clinical or legal requirement without authority.

## 8. Change Log

Material approved changes should be recorded in the relevant document and, where cross-cutting, in a project changelog.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
