# API Contracts

**Version:** 0.1  
**Status:** Draft

## 1. Purpose

Define stable expectations for external or decoupled interfaces.

## 2. Contract Elements

Each API operation should define:

- endpoint / operation name;
- purpose;
- authentication;
- authorisation;
- request schema;
- response schema;
- error schema;
- idempotency behaviour;
- rate limits;
- version;
- audit requirements.

## 3. Example: Submit Clinical Case

Conceptual contract only:

```text
Operation: SubmitCase
Actor: Verified Local Doctor
Input:
- client_submission_id
- case_template_version
- specialty
- service_category
- structured_case_data
- consent_confirmation
- attachment_references

Output:
- case_id
- case_reference
- submitted_at
- status

Errors:
- validation_failed
- unauthorised
- verification_required
- duplicate_submission
- attachment_not_ready
```

## 4. Example: Submit Final Advice

```text
Operation: SubmitFinalAdvice
Actor: Assigned Consultant
Input:
- case_id
- advice_content
- limitations
- follow_up_recommendation
- client_submission_id

Output:
- advice_id
- submitted_at
- case_status

Errors:
- unauthorised
- case_not_assigned
- invalid_case_state
- duplicate_submission
```

## 5. API Compatibility

Backward-compatible changes may include:

- optional fields;
- new enum values only where consumers tolerate them;
- additive response metadata.

Potential breaking changes:

- deleting fields;
- changing field meaning;
- changing requiredness;
- changing identifier semantics;
- changing authorisation assumptions.

## 6. Security

No API should rely on the frontend to enforce permissions.

Sensitive data should not appear in:

- URLs;
- query strings;
- error traces;
- logs.

## 7. Documentation

When implementation begins, formal contracts should be expressed using an appropriate machine-readable specification such as OpenAPI for HTTP APIs.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
