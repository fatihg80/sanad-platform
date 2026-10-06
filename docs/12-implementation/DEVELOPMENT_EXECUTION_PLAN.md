# Development Execution Plan

**Version:** 0.1  
**Status:** Draft until Build/Buy/Partner decision

## 1. Purpose

Describe how implementation work should be executed if Sanad builds or significantly customises software.

## 2. Development Sequence

1. repository/application foundation;
2. identity and professional verification;
3. contextual authorisation;
4. facility relationships;
5. clinical template engine;
6. case draft/submission;
7. secure attachments;
8. routing/reassignment;
9. consultant review/advice;
10. outcomes/closure;
11. governance workflows;
12. notifications;
13. reporting/evaluation;
14. low-connectivity hardening;
15. security/operational hardening.

## 3. Per-Feature Workflow

```text
Requirement
  ↓
Acceptance Criteria
  ↓
Design
  ↓
Expert Review if needed
  ↓
Implementation
  ↓
Automated Test
  ↓
Code Review
  ↓
Security/Privacy Check
  ↓
Staging
  ↓
Acceptance
```

## 4. Branch / PR Practice

Follow Engineering Standards and CI/CD Strategy.

## 5. Documentation Update

A feature is not complete if it changes:

- workflow;
- permissions;
- data;
- architecture;
- security;
- operations

without updating the relevant document.

## 6. Vendor Adaptation

If Buy/Partner wins:

replace “development” with:

- configuration;
- integration;
- workflow adaptation;
- extension/custom code;
- vendor testing.

The same requirement and acceptance discipline still applies.
