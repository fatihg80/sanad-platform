# Sanad Implementation Lifecycle

**Version:** 0.1  
**Status:** Draft until platform decision

## Purpose

Provide the execution sequence that connects approved documentation to working software and pilot operations.

This folder does not replace:

- Engineering standards in `08-engineering`;
- Operational procedures in `09-operations`;
- Delivery governance in `10-delivery`.

It orchestrates them.

# 1. Entry Conditions

Implementation should begin only when enough of the following are closed:

- pilot scope;
- Build / Buy / Partner decision;
- key legal blockers;
- pilot specialty direction;
- architecture baseline;
- privacy/security baseline;
- implementation backlog.

# 2. Execution Stages

```text
Implementation Planning
        ↓
Development / Configuration
        ↓
Automated Testing
        ↓
Security Verification
        ↓
Integration Testing
        ↓
Staging
        ↓
UAT
        ↓
Clinical / Operational Acceptance
        ↓
Deployment Readiness
        ↓
Production Deployment
        ↓
Hypercare / Monitoring
        ↓
Pilot Operations
        ↓
Evaluation
```

# 3. Stage Gates

## Gate I1: Ready to Build

Requires:

- implementation path selected;
- architecture approved enough for build;
- priority backlog;
- environments defined;
- critical expert reviews scheduled/completed.

## Gate I2: Feature Complete for Pilot

Requires:

- pilot-critical backlog implemented;
- automated tests;
- no open critical defects;
- documentation updated.

## Gate I3: Security Ready

Requires:

- security controls implemented;
- authorisation tested;
- secrets/storage reviewed;
- vulnerability findings addressed;
- independent review scheduled/completed as required.

## Gate I4: UAT Ready

Requires:

- staging stable;
- synthetic pilot scenarios;
- training draft;
- operational workflows available.

## Gate I5: Production Ready

Requires:

- UAT acceptance;
- clinical sign-off;
- legal/privacy readiness;
- backup restore;
- monitoring;
- runbooks;
- deployment plan;
- rollback/recovery plan.

## Gate I6: Pilot Go-Live

Use:

- Go-Live Readiness Checklist;
- Launch Governance Pack.

# 4. Required Expert Review

Before implementation gates close, consult the Expert Review Register.

Implementation teams cannot close clinical, legal, privacy, research, or regulatory decisions by technical acceptance alone.
