# ADR-003: Limit Offline Capability in the MVP

**Status:** Proposed  
**Date:** 2026-10-04

## Context

Weak and intermittent connectivity is a core Sanad constraint. Full offline clinical operation, however, materially increases privacy, security, synchronisation, and device-loss risk.

## Decision

For the initial custom MVP, target **offline-resilient drafting and synchronisation**, not a full offline clinical archive.

Prefer:

- local structured draft support;
- explicit sync status;
- idempotent submission;
- controlled retry;
- minimal local sensitive data.

Do not assume offline access to the full historical clinical record or unrestricted attachment caching.

## Consequences

Positive:

- reduces lost-device exposure;
- simpler conflict model;
- lower implementation risk;
- still supports intermittent connectivity.

Negative:

- some workflows still require connectivity;
- field users may request deeper offline behaviour.

## Revisit When

Field evidence shows that the pilot cannot function safely with limited offline capability.

Any expansion requires:

- secure local storage design;
- attachment policy;
- device-loss response;
- conflict resolution;
- local-data expiry.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
