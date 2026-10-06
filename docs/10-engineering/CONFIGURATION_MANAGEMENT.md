# Configuration Management

**Version:** 0.1  
**Status:** Draft

## 1. Purpose

Control application, infrastructure, clinical-template, and operational configuration changes.

## 2. Configuration Categories

- application;
- infrastructure;
- environment;
- feature flags;
- clinical templates;
- service hours;
- notification templates;
- routing rules;
- retention rules.

## 3. Source Control

Code and infrastructure configuration should be version controlled.

Sensitive secrets must not be stored in Git.

## 4. Clinical Configuration

Changes to:

- specialty template;
- priority rules;
- SLA rules;
- consent wording

require appropriate clinical/governance review.

## 5. Feature Flags

Feature flags may be used to:

- stage rollout;
- disable risky feature;
- pilot with limited users.

Flags must not become permanent undocumented branches of behaviour.

## 6. Configuration Audit

Material production configuration changes should be auditable.

## 7. Drift

Infrastructure/configuration drift between staging and production should be minimised and reviewed.
