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

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
