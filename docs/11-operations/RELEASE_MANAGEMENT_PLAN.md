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

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
