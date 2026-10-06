# Sanad Vendor Demonstration Script

**Version:** 0.1  
**Status:** Active vendor-discovery artifact

## Purpose

Prevent generic telemedicine demonstrations from being mistaken for evidence that a platform fits Sanad.

Vendors should demonstrate the same synthetic Sanad scenario.

## Scenario

A verified doctor at a participating Sudanese facility has a non-emergency case requiring specialist advice.

Connectivity is weak and intermittent.

The doctor needs asynchronous provider-to-provider review.

## Demonstration Steps

### 1. Professional Identity
Demonstrate:

- doctor role;
- consultant role;
- verification state;
- suspended/unverified behaviour;
- MFA if available.

### 2. Case Creation
Doctor creates:

- structured case;
- clinical question;
- relevant history/exam;
- synthetic result;
- image/document attachment.

Show:

- Arabic/RTL if supported;
- data-minimisation controls;
- template configurability.

### 3. Weak / Lost Connectivity
Demonstrate:

- what happens if connection drops;
- local data stored;
- sync status;
- retry;
- duplicate prevention;
- conflict handling.

Vendor must explain exactly what clinical data is stored on device.

### 4. Submission
Show:

- validation;
- permanent case ID;
- timestamps;
- priority/routine category.

### 5. Routing
Show:

- coordinator queue;
- consultant eligibility;
- assignment;
- accept/decline;
- reassignment;
- assignment history.

### 6. Additional Information
Consultant requests missing information.

Doctor responds.

Show audit/history.

### 7. Specialist Advice
Consultant submits final written advice.

Then demonstrate:

- correction/addendum;
- inability to silently overwrite final advice;
- author/time history.

### 8. Outcome
Local doctor records:

- whether advice changed management;
- referral information;
- follow-up outcome.

### 9. Second Opinion
Show whether a second opinion can remain distinct from the first.

### 10. Governance
Demonstrate:

- clinical audit;
- incident/near miss;
- complaint or equivalent;
- restricted governance access.

### 11. Access Control
Attempt:

- unrelated consultant opening the case;
- technical admin accessing clinical content;
- coordinator viewing only routing-relevant information.

Show actual behaviour.

### 12. Audit Trail
Show events for:

- case submission;
- assignment/reassignment;
- advice;
- amendment;
- role change;
- export.

### 13. Data Export
Export the approved synthetic evaluation dataset.

Show:

- format;
- API/export mechanism;
- data ownership;
- bulk export restrictions.

### 14. Hosting and Privacy
Vendor explains:

- primary region;
- backup region;
- support-access locations;
- subprocessors;
- data deletion;
- encryption;
- DPA;
- breach process.

### 15. Exit
Demonstrate or document:

- full data export;
- attachments export;
- audit export;
- migration format;
- deletion certification;
- exit costs.

## Evidence Capture

For every step record:

- Supported / Partial / Unsupported
- Native / Configuration / Custom Development
- Evidence
- Limitation
- Cost implication
- Expert review needed

## Required Expert Review

Vendor demo should include Technology, Clinical, Security, Privacy, and Commercial reviewers.

No generic sales demo should close a Sanad requirement.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
