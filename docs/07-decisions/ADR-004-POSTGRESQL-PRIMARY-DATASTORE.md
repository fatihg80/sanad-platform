# ADR-004: PostgreSQL as Primary Relational Datastore

**Status:** Proposed  
**Date:** 2026-10-04

## Context

Sanad requires reliable transactional storage, relational integrity, structured reporting, JSON flexibility where appropriate, and a mature operational ecosystem.

## Decision

For a custom MVP, use PostgreSQL as the primary relational datastore.

## Reasons

- mature transactional guarantees;
- constraints and relational modelling;
- strong indexing/query capabilities;
- JSONB for genuinely variable template data;
- broad hosting support;
- strong backup and replication ecosystem;
- suitable path from pilot to larger scale.

## Consequences

The team must still design:

- schema ownership;
- backups;
- encryption;
- migrations;
- reporting/read models;
- retention.

PostgreSQL is not a substitute for object storage, queueing, or analytics architecture.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
