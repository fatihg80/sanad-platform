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

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
