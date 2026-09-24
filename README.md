# Finland Internship OS

Architecture and optimization workspace for Manav's autonomous Finland internship acquisition system.

## North star

Get an English-speaking practical-training internship in Finland as quickly as reasonably possible.

Outcome priority:
1. Internship secured
2. Interview
3. Application/CV request
4. Referral or positive employer interest
5. Genuine human reply

Paid is preferred, but unpaid internships are acceptable.

## Current live system

The live operational source of truth is the Google Sheet **Finland Internship CRM — Clean v1** plus ChatGPT scheduled automations and Gmail. This repository is an architecture, prompt, and optimization workspace. It intentionally contains no OAuth tokens, passwords, API keys, Gmail credentials, or raw private mailbox exports.

Current pipeline:

```text
Discovery
  -> Qualification
  -> CRM
  -> READY_TO_SEND / ACTION_REQUIRED / RESEARCH_MORE
  -> Outreach or ATS application
  -> Inbox handling
  -> Interview / offer
  -> Funnel learning
  -> Better future targeting
```

## Start here for Fable / Astra

Read in this order:
1. `SYSTEM.md`
2. `MANAV_PROFILE.md`
3. `architecture/current-v3.md`
4. `architecture/state-machine.md`
5. `architecture/crm-schema.md`
6. `architecture/known-problems.md`
7. every file in `automations/`
8. `prompts/fable-audit.md`

Then write the redesign only under `proposals/v4/` until the audit is complete.

## Important constraints

- Finland workplace/presence required.
- English must be confirmed or plausibly supported by evidence.
- Finnish is limited.
- Current availability is approximately 10–15 hours/week while studies continue.
- Paid is preferred, not required.
- Never invent experience, graduation dates, salary expectations, work-permit facts, or university approval.
- Never guess personal email addresses.
- Official ATS/application routes must not be bypassed.
- Outreach must sound human and concise. No em dashes.

## Repository status

`current-v3` documents the live system as of 2026-09-24. `proposals/v4/` is intentionally isolated for a redesign.
