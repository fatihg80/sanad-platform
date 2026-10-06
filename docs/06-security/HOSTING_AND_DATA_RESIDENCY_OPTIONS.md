# Hosting and Data Residency Options

**Version:** 0.1  
**Status:** Options analysis, no provider selected

## 1. Purpose

Frame the hosting/data-residency decision before selecting a cloud vendor or committing to architecture.

## 2. Decision Drivers

The decision must account for:

- Sudanese legal requirements;
- organisation legal domicile;
- consultant locations;
- applicable data-protection law;
- partner/funder requirements;
- sanctions and service availability;
- latency/connectivity from Sudan;
- provider security maturity;
- backup regions;
- cost;
- operational support.

## 3. Option A: UK Hosting

Potential advantages:

- alignment if organisation is UK-established;
- mature cloud/data-protection environment;
- proximity to UK-based governance/funding partners;
- broad provider availability.

Potential concerns:

- international access/transfer analysis for Sudan and non-UK consultants;
- latency from Sudan;
- UK GDPR obligations;
- sanctions/provider-service considerations.

## 4. Option B: EU/EEA Hosting

Potential advantages:

- mature health-data/cloud ecosystem;
- strong privacy framework;
- broad region choice.

Potential concerns:

- GDPR transfer/access complexity;
- organisational legal alignment;
- latency;
- support/cost.

## 5. Option C: Middle East Region

Potential advantages:

- potentially lower latency from Sudan/Gulf;
- proximity to many diaspora consultants;
- possible regional partnership alignment.

Potential concerns:

- legal framework varies by country;
- funder/organisation expectations;
- cross-border transfer requirements;
- provider availability and contractual terms.

## 6. Option D: Sudan-Hosted / In-Country

Potential advantages:

- local residency;
- local sovereignty.

Potential concerns:

- infrastructure reliability;
- physical security;
- power/connectivity;
- operational support;
- conflict risk;
- backup/disaster recovery;
- vendor maturity.

This option should not be selected solely for geographic locality.

## 7. Option E: Hybrid

Examples:

- primary clinical data in one approved region;
- approved local edge/cache functions;
- separate research environment.

Hybrid architecture increases complexity and should only be used for a clear requirement.

## 8. Evaluation Criteria

Score each candidate region/provider for:

- legal permissibility;
- privacy/data-transfer fit;
- security certifications/controls;
- latency from pilot sites;
- availability;
- backup options;
- object storage;
- managed PostgreSQL;
- secrets management;
- monitoring;
- support;
- pricing;
- sanctions/service eligibility;
- exit/data portability.

## 9. Architecture Rule

Do not choose provider-specific services that create unnecessary lock-in before the legal/data-residency decision is settled.

Prefer portable fundamentals:

- PostgreSQL;
- S3-compatible object storage where feasible;
- containers;
- standard identity protocols;
- infrastructure as code.

## 10. Decision Evidence

Before final ADR, collect:

- legal opinion;
- provider DPA;
- subprocessor list;
- region list;
- encryption model;
- backup geography;
- support access geography;
- service availability for Sudan;
- sanctions eligibility;
- cost estimate;
- latency test.

## 11. No Current Decision

This document intentionally does not select:

- AWS;
- Azure;
- Google Cloud;
- regional provider;
- UK/EU/Middle East region.

Provider selection should follow the legal/privacy evidence, not precede it.

## Required Expert Review

**Level:** Blocking before final hosting/provider decision.

**Experts required:**
- Privacy Counsel / DPO
- Healthcare Legal Counsel
- Security Architect
- Cloud / Infrastructure Architect or SRE
- Sanctions/Compliance specialist where provider/service availability may be affected

**Evidence to retain:** legal position, DPA/subprocessors, support-access geography, backup geography, latency test, cost, security controls, and portability assessment.

---

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
