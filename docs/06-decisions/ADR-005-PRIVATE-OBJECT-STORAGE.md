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
