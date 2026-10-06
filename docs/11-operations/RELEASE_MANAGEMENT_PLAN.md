# Release Management Plan

**Version:** 0.1  
**Status:** Draft

## 1. Release Types

### Routine Release
Normal planned changes.

### High-Risk Release
Changes affecting:
- authentication;
- authorisation;
- clinical state machine;
- advice;
- image processing;
- data migrations.

### Emergency Release
Urgent fix for critical safety/security/availability issue.

## 2. Release Readiness

Before production:

- automated tests pass;
- UAT where relevant;
- security checks pass;
- migration reviewed;
- rollback/recovery considered;
- release notes prepared;
- monitoring ready.

## 3. Change Window

Production change windows should reflect service hours and consultant operations.

## 4. Rollback

Rollback plan should define:

- code rollback;
- feature disablement;
- migration handling;
- data reconciliation.

## 5. Post-Release Validation

Check:

- login;
- case submission;
- routing;
- advice;
- notifications;
- queue;
- storage;
- monitoring.

## 6. Emergency Release

Emergency change must document:

- reason;
- approver;
- risk;
- change;
- outcome;
- follow-up actions.
