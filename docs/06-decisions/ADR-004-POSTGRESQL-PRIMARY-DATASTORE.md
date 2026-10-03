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
