# Exercise: Chaos Experiment & Runbook Workshop
**Time: 3.5 Hours**

## Phase 1: Experiment Design (45 mins)
Design 5 chaos experiments to run against your local application. For each experiment document:

*   **Name:** (e.g., "The Database Kill")
*   **Hypothesis:** "We believe that if the DB proxy is stopped, API requests will gracefully return 503 instead of hanging or 500ing."
*   **Method:** The exact command (e.g., `docker stop your-db-container`).
*   **Abort Condition:** When and how to revert the failure.

*Suggested Experiments:* kill the database, add artificial latency to an external API (300-1000ms), fill the connection pool, corrupt data input payload.

## Phase 2: Execution & Fix Sprint (2 hours)
1.  **Execute:** Run your top 3 experiments. 
    *   Verify steady state.
    *   Inject failure.
    *   Observe for 2-5 minutes.
    *   Remove failure.
    *   Document the reality. Did the system crash hard?
2.  **Fix:** Select the most critical finding (e.g., the system has zero graceful degradation for database failures). Implement a fix using the Claude Code CLI. 
3.  **Verify:** Re-run the experiment against the fixed code.

## Phase 3: The Incident Response Runbook (45 mins)
Create `runbook.md` in your repository. This is the document for the person paged at 3:00 AM. 

Include:
1.  **Service Overview:** What does it do? Dependencies?
2.  **Common Incidents:** Base this on your chaos findings. Include symptoms, diagnosis commands, and remediation steps.
3.  **Escalation Policy:** Who to contact when limits are breached.
