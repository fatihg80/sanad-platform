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

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
