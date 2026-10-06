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

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
