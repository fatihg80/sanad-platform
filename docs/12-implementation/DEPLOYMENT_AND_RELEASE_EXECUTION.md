# Deployment and Release Execution

**Version:** 0.1  
**Status:** Draft until hosting/platform decision

## Deployment Flow

```text
Approved Release Candidate
   ↓
Staging Validation
   ↓
Migration/Rehearsal
   ↓
Release Approval
   ↓
Production Deployment
   ↓
Smoke Tests
   ↓
Monitoring
   ↓
Hypercare
```

## Required Inputs

- release notes;
- deployment artifact;
- migration plan;
- rollback/recovery plan;
- monitoring;
- support coverage;
- communication plan.

## Production Smoke Tests

- authentication;
- MFA;
- case creation;
- assignment;
- consultant access;
- advice;
- file access;
- queue;
- notification;
- audit;
- monitoring.

Use synthetic/non-sensitive test records where possible.

## Failed Release

If release threatens:

- clinical workflow;
- confidentiality;
- integrity;
- availability

activate rollback or controlled recovery.

## Required Expert Review

Infrastructure/SRE and Security must review production deployment architecture before first go-live.

Clinical Governance must review releases that materially alter clinical workflow or safety behaviour.
