# Service Contracts

**Version:** 0.1  
**Status:** Draft

## 1. Purpose

Define expectations between operational/technical services without confusing internal targets with patient-facing emergency guarantees.

## 2. Types

### Internal Operational Service Expectations

Examples:

- routing queue reviewed during service hours;
- notification failures visible to operations;
- backups completed and monitored;
- priority escalation triggered.

### External Vendor Service Commitments

Examples:

- hosting uptime;
- support response;
- incident notification;
- backup durability;
- data export;
- breach notification.

## 3. Important Boundary

Sanad is not an emergency service.

Therefore infrastructure SLAs must not be presented as a guarantee of emergency clinical response.

## 4. Contract Elements

Each service contract should define:

- service owner;
- consumer;
- availability expectation;
- response expectation;
- support hours;
- incident severity;
- escalation;
- maintenance;
- data responsibilities;
- termination/exit.

## 5. Example: Notification Service

Provider expectation:

- accepted message;
- delivery attempt;
- delivery status where supported;
- retry behaviour;
- failure visibility.

Sanad must not treat accepted-by-provider as proof the clinician read the message.
