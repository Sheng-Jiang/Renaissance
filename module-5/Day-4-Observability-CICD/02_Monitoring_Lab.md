# Exercise: Observability & CI/CD Lab
**Time: 4 Hours**

## Phase 1: Structured Logging Implementation (75 mins)
Replace all unstructured text logs in your Module 3/4 application with structured JSON logs.

1.  **Middleware:** Create logging middleware that executes on *every* request. It must log:
    *   `method`, `path`, `user_id`
    *   `correlation_id` (Generate a UUID for incoming requests, pass it to all subsequent functions).
    *   `duration_ms`, `status_code`
2.  **Scrubbing:** Ensure no passwords, tokens, or PII are logged.
3.  **Business Events:** Add targeted `INFO` logs for key actions (e.g., `user.created`, `payment.processed`).

## Phase 2: Metrics Expansion & Alerting (75 mins)
1.  **Expansion:** Add three new metrics to your system:
    *   `db_query_duration` (Histogram)
    *   `active_users_total` (Gauge)
    *   `pipeline_errors_total` (Counter from Day 2)
2.  **Automated Alert:** Implement an automated alert that fires when the system is in distress.
    *   Create a webhook integration (Slack, Discord, or generic testing endpoint).
    *   Trigger the webhook when the error rate exceeds 5% over a 1-minute window.
    *   *Test:* Deliberately break the system and verify the alert arrives.

## Phase 3: CI/CD Reliability Gates (90 mins)
Modify your GitHub Actions pipeline to prevent bad code from deploying.

1.  **Performance Regression Check:** 
    *   Add a step in your CI that starts the app locally.
    *   Run a small load test using `k6` or `hey` (e.g., 50 requests, 10 concurrency).
    *   Assert that the p95 latency is under a strict threshold. Fail the build if it is not.
2.  **Deployment Notification:** Add a GitHub Actions step to ping your webhook channel when a deployment successfully finishes to staging/production.
