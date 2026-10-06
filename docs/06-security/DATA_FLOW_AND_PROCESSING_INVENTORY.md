# Data Flow and Processing Inventory

**Version:** 0.1  
**Status:** Draft

## 1. Purpose

Identify where sensitive data originates, moves, is stored, and is accessed.

## 2. Core Flow

```text
Local Doctor
  ↓
Case Draft / Submission
  ↓
Sanad Application
  ↓
PostgreSQL + Private Object Storage
  ↓
Assigned Consultant
  ↓
Advice
  ↓
Local Doctor
  ↓
Outcome
  ↓
Governance / Approved Evaluation
```

## 3. Processing Activities

| Activity | Data | Actor/System | Purpose | Sensitivity |
|---|---|---|---|---|
| User registration | contact/account data | Sanad | identity | Confidential |
| Verification | professional evidence | Governance/Operations | eligibility | Confidential Professional |
| Case submission | clinical data | Doctor/Sanad | tele-expertise | Sensitive Clinical |
| File upload | images/results | Doctor/Sanad | specialist review | Sensitive Clinical |
| Routing | case metadata | Coordinator | assignment | Sensitive/Operational |
| Advice | clinical opinion | Consultant | specialist support | Sensitive Clinical |
| Outcome | follow-up data | Local Doctor | care/evaluation | Sensitive Clinical |
| Incident | safety/governance | Governance | safety | Highly Sensitive |
| Evaluation export | minimum dataset | Research | pilot evaluation | Controlled |

## 4. External Data Flows

Potential:

- notification provider;
- hosting provider;
- monitoring provider;
- identity provider;
- vendor telemedicine platform;
- research environment.

Each external flow requires approval before production.

## 5. Prohibited Default Flows

Do not send full clinical data to:

- analytics SDK;
- error monitoring;
- email/SMS;
- generic support tools;
- product marketing tools.

## 6. Access Geography

For each production provider record:

- storage region;
- backup region;
- support-access geography;
- subprocessor geography.

## 7. Update Trigger

Update whenever a new integration, vendor, data use, or research flow is introduced.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
