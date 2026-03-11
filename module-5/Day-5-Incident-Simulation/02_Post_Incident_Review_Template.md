# Exercise: Post-Incident Review (PIR) Workshop
**Time: 2 Hours**

## Context
Following the live Incident Simulation, your team must draft a formal, blameless Post-Incident Review to document what happened, why it happened, and how to prevent it from ever happening again.

## The PIR Template

Please copy and fill out the following template into `pir-[date].md`:

```markdown
# Post-Incident Review: [Incident Title]
**Date:** [YYYY-MM-DD]
**Authors:** [Your Names]
**Status:** [Draft / Under Review / Final]

## Summary
*A 2-3 sentence summary of what happened, the user impact, and the duration.*

## Impact Breakdown
*   **SLO Breached:** [Which one?]
*   **Error Budget Impact:** [How many minutes burned?]
*   **User Experience:** [What specifically did users see? 500 errors? Lag?]

## Timeline
*(Use UTC or your local timezone consistently)*
*   **09:00:** Instructor injected Failure 1 (Slow Database).
*   **09:02:** First automated alert triggered via Slack.
*   **09:05:** Engineer acknowledged alert.
*   **09:15:** Dashboard confirmed spike in p95 latency...
*(Continue mapping out the detection, diagnosis, and mitigation timeline).*

## Blameless Root Cause Analysis (The Five Whys)
1. **Why did the API go down?** Because it ran out of memory.
2. **Why did it run out of memory?** Because the connection pool filled up with hung requests.
3. **Why did the requests hang?** Because the database query took 30 seconds.
4. **Why did the DB query take 30 seconds?** Because it was missing an index on a heavily joined table.
5. **Why was the index missing?** Because our DB migration review process doesn't require `EXPLAIN ANALYZE` outputs for new queries.

*Root Cause: Lack of automated query performance validation in the CI/CD pipeline.*

## Action Items
*(Must be specific, actionable, and assigned)*
*   [ ] Fix the specific issue (e.g., Add the missing index) - Owner: [Name]
*   [ ] Prevent recurrence (e.g., Add a GitHub Action to enforce `EXPLAIN` on migrations) - Owner: [Name]
*   [ ] Improve Observability (e.g., Add an alert for connection pool > 80%) - Owner: [Name]
```

## Review
Swap your PIR with another team. Could they understand what happened just by reading your document? Have they identified systemic fixes rather than human-blaming?
