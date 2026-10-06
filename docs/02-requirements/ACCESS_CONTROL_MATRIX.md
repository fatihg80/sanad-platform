# Access Control Matrix

**Version:** 0.1  
**Status:** Draft for clinical/security approval

Legend:

- **O** Own/related records only
- **A** Assigned records only
- **G** Approved governance scope
- **M** Minimum operational metadata
- **Y** Permitted
- **N** Not permitted by default

| Capability | Local Doctor | Consultant | Coordinator | Specialty Lead | Governance Lead | Research User | Platform Admin |
|---|---:|---:|---:|---:|---:|---:|---:|
| Create case draft | O | N | N | N | N | N | N |
| Submit case | O | N | N | N | N | N | N |
| View case clinical content | O | A | M/G | G | G | Approved dataset only | N by default |
| Upload case attachment | O | A when requested | N | G | G | N | N |
| Assign/reassign consultant | N | N | Y | Y | Y | N | N |
| Provide specialist advice | N | A | N | G if clinically assigned | G if clinically assigned | N | N |
| Request additional info | N | A | N | G if assigned | G if assigned | N | N |
| Record outcome | O | N | N | N | G if authorised | N | N |
| Close case | O / policy | N | policy | policy | Y | N | N |
| Request second opinion | O/policy | A/policy | Y | Y | Y | N | N |
| Review clinical audit | N | N | N | G | G | N | N |
| Report incident | Y | Y | Y | Y | Y | N | technical only |
| View incident details | own/report context | related if authorised | limited | G | G | N | N by default |
| Manage complaint | related | related | limited | G | G | N | N |
| Export clinical data | N | N | N | restricted | restricted | approved dataset | N by default |
| Manage user roles | N | N | N | N | limited governance roles | N | Y |
| Change verification status | N | N | N | limited | Y | N | technical workflow only |
| System configuration | N | N | N | N | N | N | Y |
| View audit security logs | N | N | N | clinical audit only | clinical/governance | N | technical/security scope |

## Principles

1. Role is only the first filter.
2. Case relationship and assignment determine record access.
3. Platform administrator does not automatically gain clinical-content access.
4. Research access uses approved datasets, not unrestricted production browsing.
5. Incident and complaint data have stricter access than ordinary case data.
6. Final permissions require clinical, privacy, security, and legal approval.

## Open Decisions

- coordinator minimum-data view;
- specialty-lead scope;
- who may close/reopen a case;
- who may initiate second opinion;
- break-glass access;
- export approval workflow;
- verification approver model.

## Required Expert Review

**Level:** Required before authorisation implementation freeze; blocking before go-live.

**Experts:** Clinical Governance, Security Architect, Privacy/DPO, Operations.

**Review:** minimum necessary access, coordinator visibility, governance access, administrator separation, exports, and break-glass access.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
