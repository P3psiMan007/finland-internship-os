# System Overview

## Objective
Maximize the probability that Manav secures an English-speaking internship in Finland.

The system uses two acquisition lanes in parallel:

1. **Formal demand**: advertised internships, traineeships, student roles, open applications and study-compatible part-time work.
2. **Hidden demand**: Finnish companies where recent change signals imply useful intern-level business work even though no internship is advertised.

## High-level architecture

```text
               +---------------------------+
               | Finland Internship Scan   |
               +-------------+-------------+
                             |
               +-------------v-------------+
               | Lead Finder V3            |
               | discover + qualify        |
               +-------------+-------------+
                             |
                  Finland Internship CRM
                             |
              +--------------+---------------+
              |              |               |
       READY_TO_SEND   ACTION_REQUIRED   RESEARCH_MORE
              |              |               |
       Sender V2 +       Manav / future      |
       Sender Boost      Pack Builder        |
              |              |               |
              +-------> Gmail / ATS <--------+
                             |
                    Inbox Guardian
                             |
                      Funnel Learner
                             |
                   ranking/experiments
```

## Discovery logic
Advertised sources include company careers pages, Work in Finland, Job Market Finland, Kuntarekry and other current role sources.

Hidden-company triggers include funding, international expansion, new products, new markets, hiring bursts, partnerships, leadership changes, new offices, customer growth and commercial team expansion.

Each hidden trigger is translated into bounded BBA-relevant work such as market research, competitor research, prospect mapping, CRM organization, structured follow-up, campaign reporting, business-development research, ecommerce/commercial coordination or project coordination.

## Current operating philosophy
Accuracy and real employer progress are more important than lead or email volume. No-op is valid when no prospect clears the quality bar.
