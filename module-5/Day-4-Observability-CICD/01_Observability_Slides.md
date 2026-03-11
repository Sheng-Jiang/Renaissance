---
marp: true
theme: default
paginate: true
---

![bg right:60% fit](cover.png)
# Module 5: Data, Integration & Reliability
## Day 4: Observability Deep Dive & CI/CD
**Renaissance Developer Academy**

---

# The Three Pillars of Observability

Observability answers: *Can you understand the internal state of your system solely from its external outputs?*

1.  **Logs:** Discrete events showing *what* happened. Must be structured.
2.  **Metrics:** Numerical measurements over time (Counters, Gauges, Histograms) showing *how often/much*.
3.  **Traces:** Following a request across service boundaries showing *where* the time went.

---

# Pillar 1: Structured Logging

Stop using `console.log("User logged in")`.
Start using JSON.

```json
{
  "timestamp": "2024-05-20T10:00:00Z",
  "level": "INFO",
  "event": "user.login_success",
  "correlation_id": "abc-123",
  "user_id": 994,
  "duration_ms": 42
}
```
*Why?* Because machines can instantly search, index, and alert on JSON.

---

# CI/CD: Reliability At The Gate

Your CI/CD pipeline should catch reliability regressions *before* they compile.

*   **Test Coverage Gates:** Drop below 85%? The build fails.
*   **Performance Regression Checks:** Run a quick 10-second load test in CI. If p95 latency > threshold, build fails.
*   **Security Scans:** `npm audit` / `pip-audit` failing? Build fails.
*   **Post-Deploy Health Check:** Deploy to staging, ping `/health`. If not 200 OK, trigger automated rollback.

---

# Today's Sprints

1.  **Structured Logging:** Rip out `console.log` entirely. Implement JSON logging and correlation IDs.
2.  **Metrics & Alerting:** Build on Day 1's SLIs. Add an automated alert hooking to Discord/Slack.
3.  **CI/CD Pipeline Integration:** Add an automated performance reliability regression check to your GitHub Actions.
4.  **Documentation Update:** Update your Architecture document to denote observability data flows.
