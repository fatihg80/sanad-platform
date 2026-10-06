# Vendor Discovery Questionnaire

**Version:** 0.1  
**Status:** Draft  
**Purpose:** Ensure every platform/vendor is evaluated using the same Sanad scenario.

## 1. Product Fit

1. Can the platform support provider-to-provider asynchronous consultation?
2. Can one local doctor submit a case to one or more remote specialist consultants?
3. Can direct-to-patient features be disabled if not required?
4. Can specialty-specific structured templates be configured?
5. Can final advice be locked with addenda rather than silent editing?
6. Can outcomes be captured later by the local treating doctor?
7. Can second opinions remain distinct records?
8. Can incident/audit workflows be configured?

## 2. Low Connectivity

1. Which exact workflows work offline?
2. What data is stored on device?
3. How is local data encrypted?
4. How are conflicts handled?
5. How are duplicate submissions prevented?
6. Are uploads resumable?
7. What happens after weeks without connectivity?
8. Can offline data be remotely invalidated/expired?

## 3. Mobile and Language

1. Minimum Android version?
2. Web/PWA/native?
3. Arabic support?
4. RTL support?
5. Can clinical labels be translated without code changes?
6. Can the interface work acceptably on low-cost devices?

## 4. Identity and Professional Verification

1. MFA?
2. SSO/OIDC?
3. Configurable professional verification?
4. Registration expiry/reverification?
5. Suspensions?
6. Role + record-level/contextual access?

## 5. Clinical Files

1. Supported image/document types?
2. Size limits?
3. Compression?
4. Does processing alter diagnostic images?
5. EXIF/metadata handling?
6. Private storage?
7. Malware scanning?
8. Resumable upload?

## 6. Security

Provide:

- security architecture;
- encryption details;
- penetration-test approach;
- vulnerability-management process;
- incident-response process;
- admin-access model;
- audit-log behaviour;
- backup/recovery model;
- security certifications where relevant.

## 7. Privacy and Hosting

1. Available hosting regions?
2. Self-hosting supported?
3. Who can access production data?
4. Subprocessors?
5. Cross-border support access?
6. Data export?
7. Data deletion?
8. Backup geography?
9. DPA available?
10. Exit/migration procedure?

## 8. Auditability

Demonstrate:

- login event;
- case access;
- assignment;
- advice submission;
- advice amendment;
- export;
- role change;
- admin access.

## 9. Reporting and Evaluation

1. Custom reports?
2. Raw data export?
3. API?
4. Pseudonymised research dataset?
5. Response-time metrics?
6. User activity metrics?
7. Can analytics be disabled/restricted?

## 10. Integration

1. REST API?
2. FHIR?
3. Webhooks?
4. Notification APIs?
5. Identity federation?
6. Data import/export standards?

## 11. Operations

1. Uptime history/SLA?
2. Support hours?
3. Severity model?
4. Upgrade process?
5. Breaking changes?
6. Release cadence?
7. Implementation partner requirements?

## 12. Commercial

1. Setup cost?
2. Licence cost?
3. Per-user/per-case cost?
4. Customisation cost?
5. Support cost?
6. Hosting cost?
7. Minimum contract?
8. Exit fee?
9. Data-export fee?
10. Estimated 2-year TCO for Sanad pilot + expansion?

## 13. Demonstration Requirement

Vendor must demonstrate, using synthetic data:

```text
Doctor creates case offline/weak connection
→ sync
→ coordinator routes
→ consultant reviews
→ additional information requested
→ doctor responds
→ consultant finalises advice
→ doctor records outcome
→ governance audit
→ evaluation export
```

A generic patient video-visit demo is insufficient.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
