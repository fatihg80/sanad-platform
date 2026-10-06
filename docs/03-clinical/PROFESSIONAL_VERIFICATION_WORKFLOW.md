# Professional Verification Workflow

**Version:** 0.1  
**Status:** Draft for clinical and regulatory validation

## 1. Purpose

Define how doctors and consultants become authorised to participate in live Sanad clinical workflows.

## 2. Principle

Account registration and professional verification are separate.

Creating an account does not grant permission to submit or answer live cases.

## 3. Local Doctor Verification

Candidate evidence:

- identity;
- Sudan Medical Council registration;
- facility confirmation;
- current role/contact details.

Workflow:

```text
Invited / Registered
        ↓
Profile Completed
        ↓
Evidence Submitted
        ↓
Verification Review
   ↙             ↘
More Info      Verified
                   ↓
              Active Clinical User
```

## 4. Consultant Verification

Candidate evidence from founding source:

- specialist qualification;
- current Sudan Medical Council registration;
- current registration where practising;
- references;
- interview/review;
- relevant indemnity/employment confirmation where required.

## 5. Verification States

- Pending Profile
- Pending Evidence
- Under Review
- More Information Required
- Verified
- Rejected
- Suspended
- Expired / Reverification Required
- Revoked

## 6. Verification Record

Record:

- professional;
- evidence type;
- source/issuer;
- registration number where approved to store;
- expiry date;
- reviewer;
- decision;
- decision time;
- notes;
- revalidation date.

Sensitive evidence should have stricter access than ordinary profile information.

## 7. Reverification

Trigger when:

- professional registration expires;
- user changes country of practice;
- facility relationship changes;
- governance concern occurs;
- periodic review becomes due.

## 8. Suspension

A verified account may be suspended because of:

- expired registration;
- governance concern;
- security concern;
- partner/facility request;
- regulator issue.

Suspension must immediately restrict clinical actions while preserving records.

## 9. Separation of Duties

Where feasible, the person administering the platform should not be the sole approver of professional clinical eligibility.

## 10. Audit

Audit:

- evidence submission;
- reviewer;
- verification decision;
- status changes;
- suspension;
- reinstatement.

## 11. Regulatory Dependency

The exact acceptable verification evidence must be agreed with relevant professional/regulatory stakeholders.

Engineering cannot determine professional eligibility independently.

## Required Expert Review

**Level:** Blocking before live professional activation.

**Experts:** Clinical Governance, relevant professional regulator/adviser, Healthcare Legal Counsel, and Indemnity/Insurance specialist.

**Review:** acceptable evidence, registration status, cross-border eligibility, expiry/reverification, suspension, and indemnity conditions.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
