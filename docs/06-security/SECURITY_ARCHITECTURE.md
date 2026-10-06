# Sanad Security Architecture

**Version:** 0.1  
**Status:** Draft architecture baseline  
**Scope:** Pilot and custom-platform reference architecture

## 1. Security Objectives

Sanad security must protect:

- patient confidentiality;
- clinician confidentiality and physical safety;
- integrity of clinical advice and records;
- availability of the service within the limits of a non-emergency model;
- accountability for material actions;
- privacy across jurisdictions;
- safe recovery from outages and incidents.

## 2. Security Principles

1. **Least privilege**: users receive only the access needed.
2. **Deny by default**: access must be explicitly authorised.
3. **No implicit trust by network location**: authenticated identity and context determine access.
4. **Contextual authorisation**: role alone does not grant access to all records.
5. **Data minimisation**: do not collect unnecessary sensitive information.
6. **Separation of duties**: technical administration does not automatically equal clinical access.
7. **Defence in depth**: no single control is assumed sufficient.
8. **Auditability**: material actions are traceable.
9. **Secure defaults**: new features start private and restricted.
10. **Safety-aware security**: security decisions consider clinical and physical safety.

## 3. Security Zones

Proposed logical zones:

```text
Public Internet
      |
Edge / WAF / Reverse Proxy
      |
Application Zone
   |       |
Database  Queue/Cache
   |
Private Object Storage

Separate logical paths:
- Monitoring / Security telemetry
- Backup storage
- Approved research export
```

Production databases and object storage must not be publicly reachable.

## 4. Identity Architecture

### User identities

Every human user receives an individual account.

Shared clinical accounts should not be permitted.

### Identity states

Suggested states:

- Invited
- Registered
- Pending Verification
- Verified
- Suspended
- Revoked

Clinical actions require Verified state.

### MFA

MFA should be mandatory for:

- platform administrators;
- clinical governance leads;
- specialty leads;
- other privileged roles.

MFA for all clinical users should be the default target, subject to usability and connectivity evaluation.

### Recovery

Account recovery is a high-risk workflow and should require stronger verification than ordinary login.

## 5. Authorisation Architecture

RBAC is necessary but insufficient.

Access decision inputs may include:

- role;
- professional verification status;
- facility;
- specialty;
- current case assignment;
- case creator relationship;
- governance authority;
- sensitivity of record;
- case status.

Example:

A Consultant role does not grant access to every case. It grants eligibility to access cases assigned to that consultant.

## 6. Privileged Access

Privileged actions include:

- changing roles;
- suspending accounts;
- changing verification state;
- emergency access;
- data export;
- retention override;
- system configuration.

Controls:

- MFA;
- explicit permission;
- audit logging;
- minimal number of privileged users;
- periodic review;
- alerting for high-risk actions.

## 7. Break-Glass Access

If an operational need exists for emergency administrative access to otherwise restricted clinical information, it must be designed as an explicit break-glass mechanism.

It should require:

- approved role;
- reason;
- prominent warning;
- enhanced audit event;
- post-access review.

Do not create silent universal admin visibility.

## 8. Application Security

Controls should include:

- input validation;
- output encoding;
- CSRF protection where applicable;
- secure cookie configuration;
- session rotation;
- rate limiting;
- secure file handling;
- server-side authorisation for every protected action;
- no trust in client-side permission checks;
- mass-assignment protection;
- safe error handling;
- security headers.

## 9. API Security

If APIs are exposed:

- authenticated requests;
- scoped authorisation;
- rate limits;
- schema validation;
- versioning strategy;
- idempotency for sensitive retryable actions;
- no sensitive data in URLs;
- audit for material actions;
- strict CORS policy;
- short-lived credentials/tokens where appropriate.

## 10. Encryption

### In transit
TLS must be used for all production traffic.

### At rest
At minimum encrypt:

- production database storage;
- object storage;
- backups;
- managed secrets.

### Field-level encryption
Consider only where threat model and operational model justify it, for example highly sensitive professional or governance fields.

Encryption must not be added without a workable key-management and recovery model.

## 11. Secrets Management

Secrets must not be stored in:

- source control;
- client-side code;
- logs;
- documentation examples with real values.

Production secrets should be managed through an approved secrets mechanism provided by the hosting platform or dedicated service.

Secrets require:

- environment separation;
- rotation;
- access logging where supported;
- least privilege.

## 12. Object Storage Security

Clinical objects should be:

- private by default;
- referenced by opaque IDs;
- retrieved only after application authorisation;
- served through short-lived signed URLs or controlled streaming;
- encrypted;
- subject to retention rules.

Public bucket access must be prohibited.

## 13. Upload Security

Controls:

- allowlisted file types;
- file-size limits;
- validation based on actual content where practical;
- malware scanning for relevant document formats;
- metadata policy;
- random storage names;
- quarantine state before final availability if scanning is asynchronous.

## 14. Logging and Security Telemetry

Security-relevant events include:

- repeated failed login;
- MFA failure;
- privilege change;
- account suspension;
- unusual export;
- break-glass access;
- object-access denial;
- excessive case enumeration attempts;
- unexpected geographic/session behaviour where legally and operationally appropriate.

Logs must exclude full clinical content and secrets.

## 15. Audit Architecture

Clinical audit trail and technical/security logs are related but not identical.

### Clinical/application audit
Records business-significant actions.

### Security/technical logs
Record operational and security events.

Both require access controls and retention rules.

## 16. Environment Separation

Minimum environments:

- Development
- Test / CI
- Staging / Pre-production
- Production

Real patient data must not be used in development or ordinary test environments.

Production access must be restricted and auditable.

## 17. Dependency and Supply-Chain Security

Controls:

- lock dependency versions;
- automated vulnerability scanning;
- review high-risk package additions;
- minimise package count;
- protect CI/CD credentials;
- pin trusted CI actions where applicable;
- generate software inventory/SBOM if operationally feasible;
- defined patch process.

## 18. CI/CD Security Gates

Before production deployment:

- automated tests pass;
- lint/static analysis pass;
- dependency vulnerability threshold met;
- secret scan passes;
- database migration reviewed;
- security-sensitive changes receive review;
- artefact/build source is traceable to commit.

## 19. Database Security

- application uses least-privileged DB account;
- no shared root/superuser for runtime;
- encrypted connection where infrastructure requires;
- production DB not exposed publicly;
- backup access restricted;
- query and performance monitoring without sensitive payload leakage.

## 20. Network and Edge Controls

Depending on hosting:

- reverse proxy;
- WAF;
- DDoS protection;
- rate limiting;
- IP reputation controls where appropriate;
- no security dependence solely on IP allowlists.

Sanad's users are distributed and mobile, so network location is not a reliable identity boundary.

## 21. Device Considerations

Sanad may run on low-cost or shared Android devices.

Do not assume managed enterprise devices.

Controls should therefore emphasise:

- minimal local storage;
- short exposure window;
- clear logout;
- no sensitive notification previews where configurable;
- session revocation;
- device-loss procedure.

## 22. Third-Party Security Review

Before onboarding any provider, review:

- data processed;
- access model;
- authentication;
- encryption;
- breach response;
- subprocessor chain;
- data residency;
- logging;
- admin access;
- deletion;
- availability;
- exit strategy.

## 23. Security Standards Baseline

The engineering security checklist should be mapped to a recognised application-security verification baseline such as OWASP ASVS.

Zero-trust principles are used as an architectural mindset, particularly the principle that network location alone does not create trust.

This does not imply formal certification.

## 24. Security Acceptance Before Live Pilot

Required evidence should include:

- threat model reviewed;
- permissions matrix tested;
- professional verification workflow tested;
- MFA tested;
- audit trail verified;
- object storage confirmed private;
- backup restore tested;
- secrets scan clean;
- dependency scan reviewed;
- penetration test or independent security review completed where feasible;
- security incident procedure exercised;
- production access list approved.

## 25. Security Debt Rule

A pilot is allowed to have limited features.

It is not allowed to hide known critical security risks behind the word "MVP."

Any deferred security control must have:

- documented risk;
- owner;
- compensating control;
- target date;
- acceptance authority.

## Required Expert Review

**Level:** Required before implementation freeze; blocking before production approval.

**Experts required:**
- Security Architect
- Privacy/DPO
- Infrastructure/SRE
- Independent security assessor before go-live

**Questions to review:** identity assurance, MFA, contextual authorisation, privileged access, encryption/key management, object storage, logging, vendor access, incident response, backup security.
