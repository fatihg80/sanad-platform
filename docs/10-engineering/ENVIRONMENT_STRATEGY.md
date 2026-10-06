# Environment Strategy

**Version:** 0.1  
**Status:** Draft

## 1. Environments

### Local Development
Synthetic data only.

### CI/Test
Automated tests and ephemeral test databases.

### Staging / Pre-production
Production-like configuration with synthetic data.

### Production
Live pilot data and strictly controlled access.

## 2. Separation

Each environment should have separate:

- database;
- object storage;
- secrets;
- credentials;
- external-provider configuration.

## 3. Production Data

Production patient/clinical data must not be copied into development or routine staging.

## 4. Access

Production access:

- least privilege;
- individual accounts;
- MFA;
- audited;
- time-limited where possible.

## 5. Configuration

Environment-specific settings must not require source-code modification.

## 6. Test Providers

Use sandbox/test accounts for:

- email/SMS;
- storage;
- identity;
- monitoring

where available.

## 7. Promotion

Deploy the same tested build artifact through environments where practical.

## 8. Emergency Changes

Emergency production changes require retrospective review and documentation.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
