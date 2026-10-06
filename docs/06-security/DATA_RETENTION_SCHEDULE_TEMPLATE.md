# Data Retention Schedule Template

**Version:** 0.1  
**Status:** Draft template, retention periods TBD

Final periods require legal, clinical, research, and regulatory approval.

| Data Category | Purpose | Sensitivity | Proposed Retention | Authority/Reason | End-of-Life Action | Owner |
|---|---|---|---|---|---|---|
| Clinical cases | Tele-expertise record | Sensitive Clinical | TBD | TBD | archive/delete per policy | Clinical Governance |
| Attachments | Clinical review | Sensitive Clinical | TBD | TBD | secure deletion | Clinical Governance |
| Specialist advice | Clinical record | Sensitive Clinical | TBD | TBD | archive/delete per policy | Clinical Governance |
| Outcomes | Care/evaluation | Sensitive Clinical | TBD | TBD | archive/delete per policy | Clinical Governance |
| Professional verification | Eligibility | Confidential Professional | TBD | TBD | delete/retain minimal proof | Operations/Governance |
| Incident records | Safety/governance | Highly Sensitive | TBD | TBD | secure archive/delete | Governance |
| Complaints | Governance | Highly Sensitive | TBD | TBD | secure archive/delete | Governance |
| Audit events | Accountability | Confidential | TBD | TBD | secure expiry/archive | Security/Governance |
| Security logs | Security | Confidential | TBD | TBD | expiry | Technology/Security |
| Research datasets | Approved research | Varies | Per protocol | Ethics/protocol | destroy/archive per approval | Research Lead |
| Backups | Recovery | Mirrors source | TBD | Recovery | expiry/rotation | Technology |
| Notification logs | Delivery evidence | Confidential metadata | TBD | Operations | delete | Operations |

## Retention Rules

- retention is category-specific;
- backups must not silently defeat deletion policy;
- legal hold must be explicit;
- research retention follows approved protocol;
- "keep forever" is not a default;
- deletion must be auditable where appropriate.

## Required Decisions

For each category define:

1. exact period;
2. legal/clinical basis;
3. archival need;
4. deletion mechanism;
5. backup handling;
6. responsible owner.

## Required Expert Review

**Level:** Blocking before final retention policy.

**Experts:** Healthcare Legal Counsel, Privacy/DPO, Clinical Governance, Research Governance for research datasets, Finance for statutory financial records.

No retention period should be invented by engineering.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
