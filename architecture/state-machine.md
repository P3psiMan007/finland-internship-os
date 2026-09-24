# Current State Machine

```text
DISCOVERED
   |
   v
RESEARCH_MORE <----------------+
   |                            |
   | enough evidence            | missing/stale evidence
   v                            |
QUALIFIED ----------------------+
   |
   +--> READY_TO_SEND --> SENT_INITIAL --> FOLLOWUP_1 --> FOLLOWUP_2
   |                          |
   |                          +--> HUMAN_REPLY --> STOP_COLD_AUTOMATION
   |
   +--> ACTION_REQUIRED --> APPLICATION_READY? --> APPLIED
   |
   +--> MANUAL_REVIEW

Human reply branches:
HUMAN_POSITIVE
HUMAN_NEUTRAL
HUMAN_NEGATIVE
REFERRAL
APPLICATION_REQUEST
INTERVIEW_REQUEST
DOCUMENT_REQUEST
AVAILABILITY_QUESTION
COMPENSATION_QUESTION
OOO
BOUNCE_HARD / BOUNCE_SOFT
OPT_OUT
```

## Known weakness
`APPLICATION_READY` is conceptual today, not a fully implemented worker-owned state. ATS opportunities often stop at `ACTION_REQUIRED`, shifting tailoring work to Manav manually.
