# Documentation Guide

**Version:** 0.1  
**Status:** Active

## 1. Purpose

Keep Sanad documentation usable, current, traceable, and understandable across clinical, public-health, operational, legal, and engineering audiences.

## 2. Required Metadata

Major documents should contain:

- title;
- version;
- status;
- purpose/scope.

## 3. Status Values

- Draft
- Proposed
- Approved
- Superseded
- Retired

## 4. Source Discipline

Distinguish:

- source-derived fact;
- project decision;
- engineering recommendation;
- assumption;
- legal/clinical dependency;
- open question.

## 5. Writing Style

Prefer:

- plain language;
- explicit definitions;
- short sections;
- stable terminology;
- tables for comparisons;
- diagrams where they add clarity.

Avoid:

- unexplained technical jargon;
- aspirational language presented as fact;
- legal conclusions without counsel;
- clinical claims without clinical ownership.

## 6. File Naming

Use uppercase descriptive Markdown filenames for major documents.

Examples:

- `CLINICAL_WORKFLOW_SPECIFICATION.md`
- `THREAT_MODEL.md`
- `ADR-003-OFFLINE-STRATEGY.md`

## 7. Change Rule

When a decision changes:

- update the owning document;
- update dependent documents;
- update changelog if material;
- supersede related ADR where required.

## 8. Git Principle

Markdown in Git is the primary editable source for project documentation.

Exported Word/PDF files are presentation/distribution artifacts, not the canonical editable source unless explicitly designated.

## 9. Review Ownership

- Clinical docs: clinical owner
- Legal docs: counsel/compliance owner
- Architecture/security: technology/security owner
- Evaluation: research/evaluation owner
- Operations: operations owner

## 10. Documentation Debt

Outdated documentation is a defect.

If implementation materially diverges from documentation, either the implementation or the document must be corrected.
