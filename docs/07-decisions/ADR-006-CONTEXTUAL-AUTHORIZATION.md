# ADR-006: Contextual Authorisation on Top of RBAC

**Status:** Proposed  
**Date:** 2026-10-04

## Context

Role alone is insufficient for clinical privacy.

Two consultants have the same role, but one must not automatically see the other's assigned cases.

## Decision

Use RBAC for coarse permission eligibility and contextual policy checks for record-level access.

Authorisation may evaluate:

- role;
- verification state;
- assignment;
- facility relationship;
- specialty;
- governance authority;
- record sensitivity.

## Consequences

- every protected action requires server-side policy enforcement;
- UI visibility is not security enforcement;
- authorisation tests become a critical test suite;
- administrator access must be explicitly designed.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
