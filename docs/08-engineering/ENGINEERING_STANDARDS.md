# Sanad Engineering Standards

**Version:** 0.1  
**Status:** Draft

## 1. Goal

Establish development practices that keep Sanad safe, maintainable, reviewable, and sustainable beyond the pilot.

## 2. Core Principles

- Prefer clarity over cleverness.
- Keep business rules inside explicit domain/application boundaries.
- Treat security and clinical safety as design requirements.
- Keep infrastructure replaceable where practical.
- Avoid premature microservices.
- Avoid framework-specific shortcuts that hide critical business logic.
- Document important decisions with ADRs.
- Automate repeatable quality checks.

## 3. Repository Rules

- Main branch should remain deployable.
- Work through short-lived feature branches.
- Pull requests should be small enough to review.
- No secrets in repository history.
- Documentation changes should accompany architecture/product changes.
- Database migrations must be version controlled.
- Generated artifacts should not replace source documentation.

## 4. Coding Rules

- Explicit naming.
- Single-responsibility application services.
- Domain rules tested independently where practical.
- Authorisation enforced server-side.
- No direct controller-to-database shortcuts for critical clinical workflows.
- Avoid broad service classes that become hidden monoliths.
- Prefer typed DTOs/value objects for clinically important inputs.
- Avoid magic strings for lifecycle states, roles, and event names.
- Use immutable or append-oriented patterns for final advice and audit history.

## 5. Module Boundaries

Modules should not write directly into another module's tables unless explicitly designed and reviewed.

Preferred communication:

- public application service;
- domain/application event;
- read-only query contract.

## 6. Error Handling

Errors must:

- be understandable to users;
- avoid exposing sensitive internals;
- carry a correlation ID where useful;
- distinguish validation, authorisation, conflict, dependency, and server failures.

## 7. Clinical Safety Coding Rule

Any logic that can affect:

- case priority;
- routing;
- advice visibility;
- patient safety;
- clinical image transformation;
- SLA escalation

requires explicit tests and review.

## 8. Internationalisation

Arabic and English are first-class requirements.

Rules:

- no hard-coded UI text;
- RTL tested explicitly;
- dates/times localised;
- medical terms reviewed for meaning, not merely machine translated;
- database content that is user-entered is not automatically translated.

## 9. Accessibility

The product should target practical accessibility for clinicians using:

- small screens;
- low-quality devices;
- poor lighting;
- variable network;
- Arabic/English interfaces.

Keyboard navigation, contrast, readable typography, focus states, and form clarity should be tested.

## 10. Database Changes

Every migration should:

- be reviewed;
- avoid destructive production changes without plan;
- consider rollback/recovery;
- preserve historical clinical meaning;
- be tested on representative synthetic data.

## 11. Dependencies

New dependencies require justification.

Avoid adding a package for trivial functionality.

High-risk packages involving:

- authentication;
- file handling;
- encryption;
- PDF/image processing;
- networking

require stronger review.

## 12. Documentation

Required living documents include:

- PRD;
- SRS;
- Clinical Workflow;
- Architecture;
- Threat Model;
- ADRs;
- API/integration contracts;
- operational runbooks.

Code and docs should not knowingly contradict one another.

## 13. Definition of Ready for Development

A feature is ready when:

- user/problem is understood;
- acceptance criteria exist;
- clinical/legal dependency identified;
- data classification understood;
- authorisation rule defined;
- error/edge cases considered;
- design dependencies resolved enough to build safely.

## 14. Definition of Done

A feature is done when:

- code implemented;
- tests pass;
- authorisation tested;
- security implications reviewed;
- accessibility/i18n checked where applicable;
- monitoring/logging considered;
- migrations tested;
- documentation updated;
- acceptance criteria met;
- no known critical defect remains.
