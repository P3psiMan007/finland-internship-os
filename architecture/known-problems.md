# Known Problems to Audit

1. **Duplicate discovery**: Daily Scan and Lead Finder both search the market.
2. **High discovery frequency**: Lead Finder runs nine times each weekday despite READY queue backpressure at roughly 30.
3. **Sender duplication**: Sender V2 and Sender Boost overlap heavily.
4. **Stale cross-campaign logic**: Sender prompts still reference the retired motion/product-video campaign and combined mailbox capacity.
5. **Conflicting send policies**: Inbox Guardian mentions up to 100 new internship initials/24h while Sender workers use a much smaller combined cap.
6. **Stale pay assumptions**: Some workers still treat paid as mandatory even though unpaid is now acceptable.
7. **Learner objective drift**: Funnel Learner still ranks paid offer above internship secured and refers to an old pay gate.
8. **ATS bottleneck**: `ACTION_REQUIRED` surfaces work to Manav but does not automatically generate a tailored application pack.
9. **Potential race conditions**: multiple send/reply workers may read/write the same CRM/thread near the same time.
10. **Over-strict contact rule risk**: requiring an exact public personal email may miss legitimate company-designated careers/open-application routes.
11. **Stale-lead research waste**: recurring workers can spend cycles re-verifying prospects that are no longer decision-relevant.
12. **Scoring complexity**: score precision may exceed available evidence and may not correlate with internship conversion.
13. **Small-sample optimization**: experiment framework can appear rigorous while actual samples remain too small for stable inference.
14. **Manual application underinvestment**: system may spend more compute/research on speculative prospects than on high-quality advertised/open applications.
