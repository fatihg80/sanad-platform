# Audit Event Catalog

**Version:** 0.1  
**Status:** Draft

## 1. Purpose

Define material events that should be recorded for accountability without duplicating sensitive clinical content.

## 2. Identity and Access

- UserRegistered
- UserActivated
- LoginSucceeded
- LoginFailed
- MFAEnabled
- MFAChanged
- SessionRevoked
- AccountSuspended
- AccountReinstated
- RoleGranted
- RoleRevoked

## 3. Professional Verification

- VerificationSubmitted
- VerificationEvidenceAdded
- VerificationMoreInfoRequested
- ProfessionalVerified
- VerificationRejected
- VerificationExpired
- VerificationRevoked

## 4. Clinical Case

- CaseDraftCreated
- CaseSubmitted
- CaseAmended
- CaseWithdrawn
- CaseReopened
- CaseClosed

## 5. Attachments

- AttachmentUploaded
- AttachmentRejected
- AttachmentAccessed
- AttachmentDeletedByPolicy

Do not log attachment content.

## 6. Routing

- CaseAssigned
- AssignmentAccepted
- AssignmentDeclined
- CaseReassigned
- CaseEscalated

## 7. Advice

- AdditionalInformationRequested
- AdditionalInformationProvided
- AdviceDrafted, optional and carefully scoped
- FinalAdviceSubmitted
- AdviceAddendumAdded

## 8. Outcomes

- OutcomeRecorded
- OutcomeUpdatedUnderControlledProcess

## 9. Governance

- SecondOpinionRequested
- SecondOpinionSubmitted
- AuditOpened
- AuditCompleted
- IncidentReported
- IncidentStatusChanged
- ComplaintOpened
- ComplaintStatusChanged
- CorrectiveActionRecorded

## 10. Data and Privacy

- ClinicalExportRequested
- ClinicalExportApproved
- ClinicalExportGenerated
- ClinicalExportDownloaded
- BreakGlassAccessUsed
- RetentionOverrideApplied

## 11. Administration

- SystemSettingChanged
- TemplatePublished
- TemplateRetired
- FacilityActivated
- FacilitySuspended

## 12. Event Fields

Candidate common fields:

- event_id;
- event_type;
- occurred_at;
- actor_id;
- actor_role/context;
- entity_type;
- entity_id;
- result;
- correlation_id;
- approved minimal metadata.

## 13. Integrity Principle

Audit history must be append-oriented.

Corrections should create new audit events, not rewrite prior history.

## 14. Privacy Principle

Audit events must not contain:

- full case narrative;
- full specialist advice;
- passwords/tokens;
- unnecessary patient identifiers.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
