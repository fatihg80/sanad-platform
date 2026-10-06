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
