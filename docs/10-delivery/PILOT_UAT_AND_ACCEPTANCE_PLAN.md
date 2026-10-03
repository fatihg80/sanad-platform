# Pilot UAT and Acceptance Plan

**Version:** 0.1  
**Status:** Draft

## 1. Goal

Verify that Sanad is safe and usable enough for a controlled pilot, not merely that software features compile.

## 2. Participants

Include representatives of:

- local doctors;
- consultants;
- coordinators;
- clinical governance;
- technology;
- operations.

## 3. Environment

Use staging/pre-production with synthetic cases.

No real patient data is required for acceptance testing.

## 4. Core Acceptance Scenarios

### A. Registration and Verification
- doctor registers;
- submits evidence;
- verification approved;
- unverified doctor cannot submit live case.

### B. Routine Case
- draft;
- attachment;
- submit;
- route;
- consultant advice;
- outcome;
- close.

### C. Priority Case
- submit priority;
- routing alert;
- consultant response;
- target timing recorded.

### D. Missing Information
- consultant requests information;
- doctor responds;
- review continues.

### E. Reassignment
- consultant declines;
- coordinator reassigns;
- history preserved.

### F. Second Opinion
- second opinion requested;
- second consultant reviews;
- opinions remain distinct.

### G. Incident
- user reports incident;
- governance access restricted;
- status tracked.

### H. Connectivity
- weak network;
- draft interruption;
- retry;
- no duplicate case.

### I. Access Control
- unrelated consultant denied;
- admin denied clinical content by default;
- governance role accesses approved case.

### J. Outage
- platform unavailable;
- fallback procedure exercised;
- reconciliation demonstrated.

## 5. Non-Functional Acceptance

- Arabic/RTL usable;
- mobile screen usable;
- upload behaviour understandable;
- security controls tested;
- backup restore tested;
- monitoring alerts demonstrated;
- critical response time under expected load acceptable.

## 6. Acceptance Severity

### Blocker
Patient safety, security, privacy, or inability to complete core workflow.

### Major
Serious operational problem with workaround.

### Minor
Low-risk usability or cosmetic issue.

Pilot launch requires zero open Blockers.

## 7. Sign-Off Areas

- clinical workflow;
- clinical governance;
- security/privacy;
- technology;
- operations;
- project leadership.

Formal legal/regulatory readiness remains a separate dependency.
