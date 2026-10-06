# Notification and Escalation Policy

**Version:** 0.1  
**Status:** Draft

## 1. Objective

Deliver timely operational alerts while minimising sensitive information and notification fatigue.

## 2. Notification Principles

- minimum necessary content;
- no patient name;
- no diagnosis in notification preview by default;
- deep-link into authenticated application where possible;
- delivery status recorded where provider supports it;
- users can distinguish informational notifications from action-required alerts.

## 3. Candidate Events

- account verification update;
- case assigned;
- assignment declined/reassigned;
- additional information requested;
- additional information received;
- priority target approaching;
- final advice submitted;
- outcome requested;
- second opinion assigned;
- governance action requiring response;
- security/account event.

## 4. Channels

Possible channels:

- in-app;
- email;
- SMS;
- push;
- approved secure messaging.

Final channel selection requires privacy, cost, delivery, and local-connectivity assessment.

## 5. Sensitive Content Rule

Preferred:
> A priority case requires your review.

Avoid:
> 26-year-old patient with suspected condition X at Facility Y requires review.

## 6. Escalation

Notifications used for SLA escalation should have:

- event;
- recipient role;
- first threshold;
- repeat threshold;
- fallback recipient;
- stop condition.

## 7. Failure Handling

If a notification fails:

- record failure;
- retry according to policy;
- surface persistent failure in operations dashboard;
- do not assume notification equals receipt.

## 8. Quiet Hours

Consultant availability and service hours should control non-critical notifications.

Priority workflow rules may override ordinary quiet hours only if explicitly agreed.

## 9. Security Notifications

Account-security messages should include:

- login/security event context;
- action to secure account;
- no links that encourage unsafe credential entry where avoidable.

## 10. Open Decisions

- approved providers;
- supported channels by country;
- service-hours logic;
- escalation recipients;
- user notification preferences;
- message templates in Arabic/English.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
