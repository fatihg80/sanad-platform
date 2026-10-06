# ADR-002: Start with a Modular Monolith

**Status:** Proposed  
**Date:** 2026-10-04

## Context

Sanad is in discovery and pilot planning. Clinical workflow and operating rules are still evolving, while the initial scale is modest.

## Decision

If Sanad builds a custom MVP, start with a **modular monolith**, not microservices.

Modules will have explicit boundaries and ownership, but the application can initially be deployed as one primary application.

## Reasons

- simpler deployment and operations;
- easier transactional consistency;
- faster product iteration;
- smaller engineering team requirement;
- easier debugging;
- current load does not justify distributed complexity;
- module boundaries preserve an extraction path later.

## Consequences

Positive:

- faster MVP delivery;
- lower infrastructure overhead;
- easier local development and testing.

Negative:

- discipline is required to prevent module coupling;
- one application deployment affects all modules;
- future extraction may require deliberate refactoring.

## Revisit When

- independent teams own separate domains;
- one module scales radically differently;
- regulatory isolation requires separation;
- deployments interfere with critical availability;
- integration load justifies dedicated services.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
