# Workshop: Setting SLOs and Building Dashboards
**Time: 3 Hours**

## Overview
You will define what "healthy" means for your Module 3 Full-Stack Application, instrument the codebase to measure it, and create a dashboard to visualize it in real time.

## Part 1: Define SLOs & Calculate Budgets (60 mins)
Write a Markdown document defining the following for your application:

1.  **Availability SLO:** Provide a target percentage and justify why you chose it. (e.g., "99.9% of requests will return non-5xx responses over a 28-day window").
2.  **Latency SLO:** Provide target milliseconds for p95.
3.  **Error Budget Calculation:** How many minutes of downtime per month does this allow?

*Note: The cost of each additional '9' of availability is exponential. Don't choose 99.999% unless your users truly require military-grade uptime.*

## Part 2: Implementation (90 mins)
Add instrumentation that measures your defined SLOs in real-time.

*   Add an availability SLI (middleware tracking successful vs error responses).
*   Add a latency SLI (middleware recording response time).
*   **Option A:** Add Prometheus-style metrics (e.g., `prom-client`).
*   **Option B:** Implement custom structured JSON logging middleware.

## Part 3: Dashboard & Alerting (30 mins)
1.  **Dashboard:** Build a `/dashboard` or use Grafana Cloud to display:
    *   Current availability (last 24 hours).
    *   Latency percentiles (p50, p95).
    *   A visual indicator of remaining Error Budget (Green/Yellow/Red).
2.  **Alert Definitions:** Write down 3 alert rules (Critical, Warning, Info) based on your metrics breaching thresholds.

## Testing Your Setup
Run your load testing tool (e.g., `hey`, `k6`) against your application. Verify that your metrics update accurately and that you can see the latency shift under load.
