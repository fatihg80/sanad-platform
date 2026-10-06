# Security Assurance Execution

**Version:** 0.1  
**Status:** Draft

## Purpose

Translate the Threat Model and Security Architecture into implementation evidence.

## Activities

### During Development

- secure coding;
- dependency scanning;
- secret scanning;
- static analysis;
- authorisation tests;
- file-upload tests;
- security review of new dependencies.

### Before Staging Acceptance

- configuration review;
- object-storage review;
- logging review;
- privilege review;
- backup encryption;
- vulnerability scan.

### Before Go-Live

- independent application/security review or penetration test where feasible;
- remediation of critical/high findings;
- incident-response tabletop;
- account-compromise scenario;
- lost-device/offline scenario;
- restore test.

## Required Expert Review

**Blocking before go-live:**

- Security Architect / AppSec specialist
- Privacy/DPO for data exposure implications
- Infrastructure/SRE for production controls
- Clinical Governance where security failure can create patient safety risk
