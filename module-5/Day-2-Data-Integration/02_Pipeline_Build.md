# Exercise: Data Pipeline Build Sprint
**Time: 3.5 Hours**

## Overview
You will design and implement a data pipeline that aggregates data from 3 distinct sources to power a unified dashboard.

## Phase 1: Design & ADR (60 mins)
1.  **The Goal:** Build an aggregated dashboard pulling from:
    *   Source 1: Your Module 3 database (user activity).
    *   Source 2: A public third-party API (e.g., weather, stocks).
    *   Source 3: A file-based source (e.g., a CSV file).
2.  **Trade-off Analysis:** Choose an integration pattern (API, Event-Driven, or Batch) for *each* source.
3.  **Write ADRs:** Document two Architecture Decision Records:
    *   ADR 1: Why you chose specific patterns for each source.
    *   ADR 2: Your error handling strategy (Circuit breaker vs. Retry vs. Dead Letter Queue).

## Phase 2: Pipeline Build - Extraction (90 mins)
Implement the extraction logic for your 3 sources. *Focus heavily on error handling.*

*   **API Source:** Implement exponential backoff retries, a circuit breaker (stop calling after 5 failures), and strict timeout handling.
*   **File Source:** Implement schema validation and handle malformed records without crashing the whole pipeline.

## Phase 3: Pipeline Build - Integration & Tests (60 mins)
1.  Combine the data into a unified view for a simple dashboard endpoint.
2.  **Idempotency Check:** Verify that running your pipeline twice with the exact same data does not result in duplicate records.
3.  **Integration Tests:** Write automated tests using mocked external sources to verify your circuit breakers and error handlers work locally.
