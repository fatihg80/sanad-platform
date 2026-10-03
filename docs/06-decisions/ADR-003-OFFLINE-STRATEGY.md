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
