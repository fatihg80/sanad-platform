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

### Documentation Attribution

**Documentation framework, repository structure, methodology expression, and original authored contributions:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

© 2026 Alfatih Abdalla. This attribution applies to Alfatih Abdalla’s original documentation contributions and organizational expression in this repository. Source materials and third-party contributions retain their respective authorship and rights.
