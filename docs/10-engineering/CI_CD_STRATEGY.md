# Sanad CI/CD Strategy

**Version:** 0.1  
**Status:** Draft

## 1. Objectives

- reproducible builds;
- traceability from commit to deployment;
- automated quality gates;
- controlled production release;
- simple rollback/recovery.

## 2. Branching

Recommended:

- `main` as protected deployable branch;
- short-lived feature branches;
- pull request review;
- no long-lived develop branch unless team workflow later requires it.

## 3. Pull Request Checks

Required candidates:

- formatting/linting;
- unit tests;
- feature/integration tests;
- static analysis;
- dependency vulnerability scan;
- secret scan;
- frontend build;
- database migration validation.

## 4. Deployment Environments

- Development
- CI/Test
- Staging
- Production

Optional dedicated security/research environments may be introduced later.

## 5. Staging

Staging should resemble production architecture while using synthetic data.

It should support:

- clinical workflow acceptance;
- migration rehearsal;
- permissions testing;
- security review;
- performance checks.

## 6. Production Deployment

A deployment must identify:

- commit SHA;
- build artefact;
- migration version;
- deployer/automation identity;
- deployment timestamp.

## 7. Database Migrations

High-risk migrations require:

- staging rehearsal;
- backup/recovery plan;
- compatibility consideration during rolling deployment.

## 8. Rollback

Code rollback should be straightforward.

Database rollback may not always be safe, therefore changes should prefer forward-compatible remediation.

## 9. Secrets

CI/CD secrets must be:

- stored in platform secret management;
- least privileged;
- environment specific;
- rotated when exposure is suspected.

## 10. Production Approval

During the pilot, production releases should use an explicit approval gate for:

- schema changes affecting clinical data;
- authentication/authorisation changes;
- clinical workflow state changes;
- file-processing changes.

## 11. Supply Chain

- pin trusted CI actions where practical;
- review third-party actions;
- minimise pipeline privileges;
- avoid exposing production secrets to pull-request code.

## 12. Release Notes

Material releases should document:

- user-visible changes;
- clinical workflow changes;
- security fixes;
- migrations;
- known limitations.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
