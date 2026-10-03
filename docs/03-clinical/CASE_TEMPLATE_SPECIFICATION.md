# Clinical Case Template Specification

**Version:** 0.1  
**Status:** Draft, specialty-agnostic

## 1. Purpose

Define the generic structure every Sanad clinical case template should follow before specialty-specific fields are added.

This document does not define specialty clinical content. Specialty leads must approve specialty-specific fields.

## 2. Template Design Principles

- collect only information necessary for specialist review;
- prefer structured fields where clinically useful;
- keep free text focused;
- avoid direct patient identifiers by default;
- make required fields clinically justified;
- support low-bandwidth entry;
- version every template;
- preserve the version used for each submitted case.

## 3. Core Sections

### Case Context
- specialty;
- service category: Routine or Priority;
- facility reference;
- submitting doctor;
- case reference.

### Patient Profile
Use minimum necessary demographic information.

Candidate fields:
- age or age band;
- sex where clinically relevant;
- pregnancy status where relevant.

Do not require:
- patient name;
- national ID;
- home address;
- personal phone number.

### Clinical Question
Required concise question to the consultant.

### Presenting Problem
- presenting complaint;
- duration;
- relevant symptoms;
- chronology.

### Relevant History
- medical history;
- surgical history;
- medications;
- allergies;
- relevant family/social history only where clinically required.

### Examination
Structured specialty-appropriate observations.

### Vital Signs
Where relevant:
- temperature;
- blood pressure;
- pulse;
- respiratory rate;
- oxygen saturation;
- other specialty measures.

Units must be explicit.

### Investigations
- laboratory results;
- imaging;
- ECG;
- pathology;
- other tests.

### Attachments
Permitted clinical images and documents.

### Local Assessment
Optional working diagnosis/differential where appropriate.

### Available Resources / Constraints
Information that materially affects management, such as unavailable investigation or referral capability.

### Consent Confirmation
Record that required consent process has been completed.

## 4. Priority Case Fields

If Priority is selected, require:

- reason for priority;
- clinically relevant timing information;
- confirmation that case is not being submitted as an emergency-service request.

## 5. Free-Text Controls

Every free-text field should include guidance not to enter unnecessary identifiers.

Potential identifier detection may warn users, but should not claim guaranteed anonymisation.

## 6. Required Field Rule

A field is required only if absence would make specialist review unsafe or operationally impossible.

Avoid making every field mandatory.

## 7. Units and Ranges

Where numeric values are collected:

- units must be defined;
- reasonable validation may be applied;
- clinically unusual values should not be silently rejected;
- warnings are preferable to hard rejection when rare valid values are possible.

## 8. Template Versioning

Each template version should record:

- template ID;
- specialty;
- version;
- effective date;
- status;
- approved by;
- change summary.

Submitted cases retain the original version.

## 9. Specialty Extension

Each pilot specialty should create an extension defining:

- required history;
- examination fields;
- investigation requirements;
- image types;
- red flags;
- priority criteria;
- outcome fields.

## 10. Validation Before Use

A specialty template requires:

- specialty lead review;
- clinical governance review;
- privacy review;
- usability testing with doctors inside Sudan;
- low-connectivity/mobile testing.

## 11. Open Decisions

- pilot specialty;
- age/date representation;
- clinical coding/vocabularies;
- whether local diagnosis is required;
- priority criteria;
- maximum attachment set;
- specialty-specific outcome dataset.
