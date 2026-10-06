# Response Time and Escalation Policy Model

**Version:** 0.1  
**Status:** Draft for operations and clinical approval

## 1. Source Targets

Founding concept:

- Routine: 24 to 48 hours
- Priority: 4 to 6 hours during service hours

Sanad is not an emergency service.

## 2. Required Policy Decisions

Before implementation define:

- service timezone;
- service hours;
- working days;
- public-holiday behaviour;
- when response clock starts;
- whether clock pauses awaiting additional information;
- assignment acceptance timeout;
- escalation thresholds;
- outage handling.

## 3. Proposed Clock Events

### Start
At successful case submission.

Alternative to review:
At validation/routing acceptance.

A single rule must be chosen.

### Stop
At submission of final specialist advice.

### Pause
Possible when:
- local doctor must provide required additional information.

Pause behaviour is TBD and must be transparent in metrics.

## 4. Escalation Stages

Example model:

### Stage 1
Case awaiting assignment beyond operational threshold.

Action:
Coordinator alert.

### Stage 2
Assigned consultant has not accepted within threshold.

Action:
Coordinator reassigns or contacts backup.

### Stage 3
Response target approaching.

Action:
Escalation to coordinator/specialty lead.

### Stage 4
Response target breached.

Action:
Operational review, reassignment where useful, breach recorded for evaluation.

## 5. Priority Safety

Priority must never be labelled or presented as emergency coverage.

User-facing text should instruct clinicians to use appropriate local emergency pathways for immediately life-threatening situations.

## 6. Metrics

Track:

- submission-to-assignment;
- assignment-to-acceptance;
- acceptance-to-advice;
- total response time;
- paused time, if applicable;
- target breach;
- reason for breach.

## 7. Outages

Policy must distinguish:

- Sanad infrastructure outage;
- user connectivity outage;
- consultant unavailability;
- fallback-channel use.

## 8. Governance

Repeated target breaches may indicate:

- insufficient consultant capacity;
- poor routing;
- unrealistic SLA;
- operational failure.

Response-time reporting is therefore a service-design metric, not only a performance leaderboard.

---

### Project & Documentation Attribution

**Project Founder and Founding Prospectus source:** **Dr. Elaf Sabri Khalil**  
[Email](mailto:elafsabri515@gmail.com) · [LinkedIn](https://www.linkedin.com/in/elaf-sabri-khalil-68097024a)

**Consulting contributor — repository structure, documentation architecture, methodology expression, and analysis:** **Alfatih Abdalla**  
[Email](mailto:Fabdalla782@gmail.com) · [LinkedIn](https://www.linkedin.com/in/alfatihabdalla) · [GitHub](https://github.com/fatihg80)

Alfatih Abdalla contributed to Sanad in a consulting capacity after being engaged by Dr. Elaf Sabri Khalil. His contribution in this repository is limited to structuring the repository, documentation layers, analysis, and related consulting work based on Dr. Elaf’s founding materials. This attribution does **not** represent Alfatih Abdalla as the founder or owner of Sanad.

Source materials and third-party contributions retain their respective authorship and rights.
