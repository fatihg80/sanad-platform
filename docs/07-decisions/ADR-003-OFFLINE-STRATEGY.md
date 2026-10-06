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

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
