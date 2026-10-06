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

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
