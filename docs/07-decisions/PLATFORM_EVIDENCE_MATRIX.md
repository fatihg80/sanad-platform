# Platform Evidence Matrix

**Version:** 0.1  
**Status:** Evidence collection, not final scoring  
**Date:** 2026-10-06

Legend:

- **C** Confirmed by official public evidence
- **P** Partial / indirect evidence
- **U** Unverified
- **N** No evidence found in current public review
- **D** Requires demonstration

| Requirement | Intelehealth | VSee Enterprise | CHT | Custom MVP |
|---|---:|---:|---:|---:|
| Provider-to-provider | C [E-002] | C [E-004/E-005] | P | Designable |
| Asynchronous specialist workflow | D | C [E-004/E-005] | D | Designable |
| Low-bandwidth orientation | C [E-003] | U/D | C [E-006] | Designable/test |
| Offline-first | P/D | U | C [E-006/E-008] | Proposed limited |
| Arabic / RTL | U | U | P/D | Designable |
| Structured case forms | C/P [E-002] | C [E-004] | C [E-006/E-007] | Designable |
| Routing | D | C/P [E-004] | D | Designable |
| Written advice | D | C [E-005] | D | Designable |
| Advice addenda/history | U | U | U | Designable |
| Outcomes | D | D | D | Designable |
| Second opinion | U | U | U | Designable |
| Clinical governance | P | D | D | Designable |
| Contextual record access | U | D | P [E-007] | Designable |
| Roles/permissions | C/P | C/P [E-004] | C [E-007] | Designable |
| MFA | U | C [E-004] | U/D | Designable |
| Auditability | D | D | D | Designable |
| Data export | D | D | C/P | Designable |
| API/integration | C/P [E-002] | C [E-004] | C/P | Designable |
| FHIR path | C [E-002/E-003] | D | Integration possible | Future |
| Hosting/data residency control | D | D | P/self-host | Designable |
| Open source | C [E-002] | No/commercial [E-004] | C | Yes if owned |
| Vendor lock-in risk | P | High/contract-dependent | Lower/self-host | Lowest product lock-in |
| Pilot implementation speed | D | D | D | Estimate required |
| 2-year TCO | U | U | U | Estimate required |

## Evidence Traceability

Evidence IDs refer to `docs/04-research/EVIDENCE_INTAKE_REGISTER.md`.

Cells without an Evidence ID remain unverified or demonstration-dependent.

## Interpretation

This matrix deliberately avoids numeric scores until the evidence behind critical rows is strong enough.

The next step is to replace U/D values with:

- demonstration evidence;
- architecture documents;
- security/privacy answers;
- commercial proposals;
- hands-on test results.

## Required Expert Review

Final numeric scoring requires:

- Technology
- Security
- Privacy
- Clinical Governance
- Commercial/Procurement

The Project Manager should not use this table as a procurement decision until those reviewers sign off.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
