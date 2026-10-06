# Testing and Verification Execution

**Version:** 0.1  
**Status:** Draft

## Test Layers

1. Unit
2. Integration
3. Feature/API
4. Authorisation
5. Contract
6. Browser/E2E
7. Offline/network
8. Security
9. Performance
10. UAT
11. Clinical safety verification
12. Operational recovery tests

## Critical Verification Areas

- unrelated consultant cannot access case;
- unverified clinician cannot participate;
- final advice cannot be silently overwritten;
- retry does not duplicate case/advice;
- offline sync does not corrupt case;
- attachments remain private;
- audit events exist;
- priority workflow triggers expected escalation;
- notification failure is visible;
- backup restore works.

## Evidence

Each release candidate should retain:

- test results;
- security results;
- UAT results;
- defects;
- accepted residual risks.

## Required Expert Review

Clinical test cases involving safety rules require Clinical Governance/ specialty expert approval.

Security verification requires security specialist review.

Accessibility/mobile validation should include representative local users or UX/accessibility expertise.
