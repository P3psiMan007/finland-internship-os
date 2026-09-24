# Current V3 Architecture

As of 2026-09-24, six internship automations are active.

| Worker | Schedule | Primary responsibility |
|---|---|---|
| Finland Internship Scan | Daily 08:00 | Broad opportunity scan/report |
| Finland Internship Lead Finder V3 | Weekdays hourly 08:00–16:00 | Discovery, qualification and CRM ingestion |
| Finland Internship Sender V2 | Weekdays hourly 09:15–16:15 | Manual-application queue + cold outreach |
| Internship Sender Boost | Weekdays 10:45, 12:45, 14:45 | Supplemental sending capacity |
| Finland Internship Inbox Guardian | Weekdays every 2h, 08:30–20:30 | Reply/bounce/OOO monitoring and safe routine replies |
| Finland Internship Funnel Learner | Weekdays 19:00 | Funnel analytics and experimentation |

## Current acquisition lanes

### Hidden opportunity
Company has a fresh signal of possible workload, plus a suitable functional owner and legitimate contact path.

### Open application
Company explicitly accepts open applications. Official route wins over cold email.

### Live role
Advertised internship/trainee/student position. If ATS/form is required, route is `ACTION_REQUIRED`.

## Current routing
- `READY_TO_SEND`: verified direct email outreach is allowed.
- `ACTION_REQUIRED`: official ATS/form/application route required.
- `RESEARCH_MORE`: evidence incomplete.
- `MANUAL_REVIEW`: potentially strong but needs judgment or missing facts.

## Current backpressure
Lead Finder stops broad company addition when about 30 genuinely usable READY_TO_SEND records exist and spends runs cleaning/reverifying the queue.
