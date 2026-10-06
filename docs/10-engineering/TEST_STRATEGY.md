# Sanad Test Strategy

**Version:** 0.1  
**Status:** Draft

## 1. Objective

Testing must prove not only that screens work, but that clinical workflow, permissions, auditability, and failure handling behave correctly.

## 2. Test Pyramid

### Unit Tests
Focus on:

- domain rules;
- state transitions;
- validation;
- priority rules;
- permission predicates;
- time calculations.

### Integration Tests
Focus on:

- database persistence;
- queues;
- object storage;
- authentication;
- notifications;
- file processing.

### Feature / API Tests
Focus on end-to-end application behaviour within the backend boundary.

### Browser / E2E Tests
Use for critical user journeys.

## 3. Critical Clinical Journeys

Automated tests should cover:

1. verified doctor creates draft;
2. doctor submits valid case;
3. unverified user cannot submit;
4. coordinator assigns eligible consultant;
5. unrelated consultant cannot access case;
6. consultant requests more information;
7. doctor responds;
8. consultant submits final advice;
9. final advice cannot be silently overwritten;
10. doctor records outcome;
11. case closes;
12. authorised governance user audits case;
13. second opinion remains distinct;
14. incident access is restricted.

## 4. Authorisation Tests

This is a critical suite.

Test every sensitive action against:

- allowed role/context;
- wrong role;
- correct role but wrong case;
- suspended user;
- unverified user;
- privileged role with insufficient context.

## 5. Offline Tests

Where PWA/offline drafting exists:

- disconnect during draft;
- reconnect and sync;
- repeated retry;
- duplicate submission prevention;
- conflict handling;
- logout before sync;
- expired local draft;
- partial attachment upload.

## 6. File Tests

- invalid extension;
- spoofed MIME type;
- oversized file;
- corrupted upload;
- duplicate retry;
- metadata policy;
- signed URL expiry;
- unauthorised retrieval.

## 7. Security Testing

Automated:

- dependency scan;
- secret scan;
- static analysis;
- security linting;
- unit/feature authorisation tests.

Pre-pilot:

- independent penetration test or equivalent security review where feasible;
- object-storage review;
- configuration review;
- recovery exercise.

## 8. Performance Testing

Pilot tests should model:

- weak latency;
- low bandwidth;
- intermittent failure;
- concurrent uploads;
- queue backlog;
- reporting load.

Performance targets must be defined from field constraints, not only broadband desktop benchmarks.

## 9. Accessibility and Localisation

Test:

- Arabic RTL;
- English LTR;
- mixed clinical content;
- keyboard navigation;
- mobile viewport;
- form error clarity;
- long translations;
- timezone/date formatting.

## 10. Clinical Safety Test Cases

Clinical owner review is required for tests involving:

- specialty templates;
- priority classification;
- image handling;
- outcome fields;
- emergency boundary messaging;
- SLA/escalation rules.

## 11. Test Data

Use synthetic data.

Do not copy production patient records into development or CI.

## 12. Regression Rule

Any production incident or serious defect should produce a regression test where technically appropriate.

## 13. Release Gate

No production release if:

- critical tests fail;
- authorisation suite fails;
- migration validation fails;
- secret scan fails;
- known critical security defect exists.
