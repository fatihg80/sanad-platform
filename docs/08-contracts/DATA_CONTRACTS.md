# Data Contracts

**Version:** 0.1  
**Status:** Draft

## 1. Purpose

Define the meaning, ownership, quality, and compatibility of data shared between domains or exported for evaluation.

## 2. Data Contract Elements

Each governed dataset should define:

- name;
- owner;
- purpose;
- fields;
- field meaning;
- type;
- units;
- null semantics;
- sensitivity;
- allowed values;
- version;
- retention;
- consumers.

## 3. Example: Pilot Evaluation Case Record

Candidate fields:

- case_id: opaque identifier;
- specialty_code;
- service_category;
- submitted_at_utc;
- assigned_at_utc;
- advice_submitted_at_utc;
- outcome_recorded: boolean;
- advice_changed_management: yes/no/unknown;
- referral_avoided: yes/no/unknown;
- incident_linked: boolean.

No patient name should be included.

## 4. Clinical Units

Numeric clinical fields must document units.

Never assume a value such as “5.4” is meaningful without unit/context.

## 5. Null Semantics

Differentiate:

- not collected;
- unknown;
- not applicable;
- missing due to error.

Do not collapse all into one ambiguous null if evaluation depends on the distinction.

## 6. Ownership

Data ownership/stewardship must be explicit.

Examples:

- Clinical Governance owns clinical meaning.
- Research/Evaluation owns approved evaluation definitions.
- Technology owns implementation, not clinical semantics.

## 7. Change Management

Changing data meaning is a breaking change even if the database type stays the same.

## 8. Research Export

Research/evaluation exports should use a versioned contract separate from production table structure.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
