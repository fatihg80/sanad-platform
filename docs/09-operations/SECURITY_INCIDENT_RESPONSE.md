# Security Incident Response Plan

**Version:** 0.1  
**Status:** Draft

## 1. Purpose

Define how Sanad responds to suspected security or privacy incidents.

## 2. Incident Examples

- compromised account;
- unauthorised case access;
- exposed object-storage data;
- leaked credentials;
- malicious upload;
- lost device containing offline drafts;
- vendor breach;
- excessive administrative access;
- research dataset disclosure.

## 3. Severity

Proposed levels:

### SEV-1 Critical
Potential patient/clinician safety impact, broad sensitive-data exposure, active compromise, or major service loss.

### SEV-2 High
Confirmed limited sensitive-data exposure or high-risk security failure.

### SEV-3 Medium
Contained event with limited impact.

### SEV-4 Low
Low-risk event or policy violation requiring tracking.

Final matrix requires governance approval.

## 4. Response Lifecycle

```text
Detect
  ↓
Triage
  ↓
Contain
  ↓
Preserve Evidence
  ↓
Eradicate
  ↓
Recover
  ↓
Notify as Required
  ↓
Review and Improve
```

## 5. Roles

At minimum:

- incident commander;
- technical/security lead;
- clinical governance representative;
- data protection/legal representative;
- operations representative;
- communications owner.

## 6. Immediate Actions

Depending on incident:

- revoke sessions;
- suspend account;
- rotate secrets;
- disable integration;
- restrict object access;
- preserve relevant logs;
- avoid destructive evidence cleanup.

## 7. Patient and Clinician Safety

Security response must assess whether disclosure could create:

- patient harm;
- clinician physical risk;
- facility risk;
- coercion or targeting risk.

## 8. Notification

Legal notification requirements are jurisdiction dependent and must be defined before pilot.

Maintain a contact matrix for:

- regulator/data protection authority;
- partner facilities;
- funders;
- affected users;
- vendors.

## 9. Post-Incident Review

Capture:

- root cause;
- timeline;
- scope;
- decisions;
- missed signals;
- corrective actions;
- tests added;
- document/architecture changes.

## 10. Tabletop Exercise

Run at least one pre-pilot exercise involving a realistic scenario such as:

> A consultant account is compromised and multiple clinical cases may have been accessed.
