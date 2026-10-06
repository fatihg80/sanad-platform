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

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
