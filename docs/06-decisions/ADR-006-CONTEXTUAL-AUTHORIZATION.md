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
