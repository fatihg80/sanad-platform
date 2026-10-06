# Minimum Evaluation Dataset

**Version:** 0.1  
**Status:** Draft

## 1. Purpose

Define the smallest dataset required to evaluate the pilot without collecting unnecessary clinical or personal information.

## 2. Design Principle

If a field is not needed for:

- safe case handling;
- service operations;
- agreed evaluation;
- governance

it should not be collected merely because it may be interesting later.

## 3. Case-Level Operational Fields

- case ID;
- facility ID;
- specialty;
- service category;
- submitted timestamp;
- assigned timestamp;
- consultant accepted timestamp;
- final advice timestamp;
- closed timestamp;
- reassignment count;
- additional-information requested: yes/no;
- second opinion: yes/no.

## 4. Minimal Patient Context for Evaluation

Only if clinically/evaluation-relevant:

- age or age band;
- sex where relevant;
- broad case type/category.

Avoid direct identity.

## 5. Clinical Value Fields

Candidate:

- advice changed management: yes/no/unknown;
- change type;
- referral recommended: yes/no;
- referral avoided: yes/no/unknown;
- additional investigation recommended: yes/no;
- follow-up requested: yes/no;
- known short-term outcome category where appropriate.

Final fields require specialty/research review.

## 6. Safety Fields

- incident linked: yes/no;
- incident category;
- severity;
- near miss: yes/no;
- complaint linked: yes/no;
- privacy/security event: yes/no.

Detailed incident content should remain in governance records, not the evaluation dataset.

## 7. Connectivity Fields

Useful candidate fields:

- upload failure experienced: yes/no;
- fallback channel used: yes/no;
- offline draft used: yes/no;
- sync conflict: yes/no.

Avoid collecting precise location/network identifiers unless needed.

## 8. User Experience

Survey-linked, not necessarily per case:

- satisfaction;
- usefulness;
- ease of use;
- documentation burden;
- connectivity burden;
- confidence in specialist support;
- willingness to continue.

## 9. Consultant Metrics

- active consultant count;
- cases assigned;
- cases accepted;
- cases declined;
- response time;
- participation over time.

Avoid using metrics as punitive performance scores during the pilot.

## 10. Financial Fields

- consultant fee;
- platform/technology cost allocation;
- coordination cost allocation;
- connectivity support;
- other direct pilot operating cost.

## 11. Data Minimisation Review

Every proposed field should be reviewed for:

- necessity;
- sensitivity;
- retention;
- reporting use;
- re-identification risk.

## 12. Versioning

The minimum dataset should be versioned.

Any field added during the pilot should document:

- why it was added;
- date;
- approval;
- effect on longitudinal comparison.

## Required Expert Review

**Level:** Required before evaluation schema is implemented.

**Experts:** Public Health/Health Services Research, Biostatistics/Evaluation, Privacy/DPO, Clinical Governance.

**Review:** necessity, outcome validity, missing-data semantics, re-identification risk, and analysis feasibility.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
