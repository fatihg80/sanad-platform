# ADR-005: Private Object Storage for Clinical Files

**Status:** Proposed  
**Date:** 2026-10-04

## Context

Sanad must handle clinical images and documents. Storing large binary files directly in the relational database would complicate performance, scaling, and object lifecycle management.

## Decision

Use private S3-compatible object storage for permitted clinical files.

The application database stores metadata and references, not public URLs.

## Required Controls

- private bucket/container;
- encryption;
- opaque object keys;
- application authorisation before access;
- short-lived signed access where used;
- file validation;
- retention policy;
- metadata policy;
- no anonymous/public access.

## Consequences

Object storage becomes a critical protected datastore and must be included in backup, incident, retention, and vendor reviews.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
