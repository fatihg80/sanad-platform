# Sanad Data Architecture

**Version:** 0.1  
**Status:** Draft

## 1. Goals

The data architecture must support:

- clinical safety;
- privacy;
- auditability;
- low-connectivity workflows;
- evaluation;
- future interoperability;
- controlled growth.

## 2. Primary Stores

### PostgreSQL
Authoritative store for structured application data.

### Object Storage
Authoritative store for permitted images and documents.

### Redis
Ephemeral queue/cache coordination only, not a source of clinical truth.

### Audit Data
Initially stored in append-oriented PostgreSQL structures, with the option to stream to a dedicated security/audit system later.

## 3. Data Separation

Logical schemas or strong module ownership should separate:

- identity;
- professional verification;
- clinical;
- governance;
- audit;
- reporting.

Physical separation is not required for the MVP unless risk or regulation requires it.

## 4. Clinical Data

Clinical structured fields should favour:

- explicit types;
- coded options where clinically appropriate;
- units;
- clear null/unknown semantics;
- template-version references.

Avoid dumping the entire case into an unstructured JSON blob merely for development speed.

JSON/JSONB can be used where variability is genuinely required, but core workflow fields should remain queryable and constrained.

## 5. Timestamps

All persistent timestamps should be stored in UTC.

The UI should display times in the user's relevant timezone.

Service rules must explicitly define which timezone governs response targets.

## 6. Soft Delete

Do not use generic soft-delete behaviour as the answer to every retention problem.

Different records need different semantics:

- account deactivation;
- clinical record closure;
- legal retention;
- privacy deletion;
- archive;
- correction.

Deletion behaviour must be domain-specific.

## 7. Data Retention

Retention must be policy-driven.

Each category needs:

- retention period;
- retention reason;
- archival rule;
- deletion mechanism;
- backup treatment.

## 8. Object Metadata

Database record for an object should include:

- opaque object ID;
- owning domain/entity;
- MIME type;
- size;
- integrity hash where useful;
- upload status;
- scanning status;
- storage key;
- retention class;
- created by;
- created time.

Do not expose raw provider keys as business identifiers.

## 9. Audit Data

Audit events should contain the minimum content needed to establish accountability.

Suggested fields:

- event ID;
- actor ID;
- actor type;
- action;
- entity type;
- entity ID;
- timestamp;
- request/session correlation ID;
- result;
- metadata approved for logging.

Avoid storing full clinical content in audit logs.

## 10. Reporting Views

Operational reporting should use dedicated database views or read models.

This reduces pressure to grant analysts raw-table access.

## 11. Research Extraction

Approved research extraction should:

1. define an approved field list;
2. filter permitted records;
3. transform/de-identify where required;
4. generate a versioned dataset;
5. record who generated it and why;
6. restrict access;
7. record expiry/retention.

## 12. Backup Data

Backups are copies of sensitive data and must follow:

- encryption;
- access control;
- retention;
- restoration testing;
- deletion/expiry policy.

## 13. Data Migration

Every schema change must be:

- version controlled;
- reviewed;
- forward safe;
- tested on representative non-production data;
- accompanied by rollback or recovery planning for high-risk changes.

## 14. Interoperability Readiness

Do not adopt a healthcare standard superficially.

Internal modelling should preserve semantic clarity so that future mapping to standards such as FHIR is possible where required.

Interoperability should be introduced based on real partner and policy needs.

## 15. Data Quality

Critical fields require validation for:

- presence;
- type;
- units;
- acceptable ranges where clinically approved;
- consistency;
- vocabulary version.

Clinical validation rules must be approved by clinical owners.

## 16. Data Ownership

The system must document ownership/stewardship for:

- clinical case data;
- professional verification data;
- governance data;
- research extracts;
- audit logs.

Technical administrators are custodians, not automatically business owners of data.

## 17. Open Data Decisions

- retention periods;
- hosting region;
- backup region;
- encryption key ownership;
- research pseudonymisation model;
- clinical coding systems;
- partitioning/archive strategy;
- audit-log immutability mechanism;
- production support access.
