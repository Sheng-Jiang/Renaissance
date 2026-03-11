# Workshop: Architecture Decision Records (ADRs)

**Objective:** Practice writing formal ADRs for realistic engineering scenarios, focusing heavily on articulating trade-offs and consequences.

## Part 1: The Template
Use this template for all ADRs in this course and in your capstone.

```markdown
# [Short Title of the Record]

**Date:** YYYY-MM-DD
**Status:** [Proposed | Accepted | Rejected | Deprecated | Superseded]

## Context
Describe the forces at play, including technological, political, social, and project local. These forces are probably in tension, and should be called out as such. The language in this section is value-neutral.

## Decision
State what we will do. The language in this section is an active voice command.

## Consequences
What becomes easier or more difficult to do because of this change? Describe the positive and negative consequences.
```

## Part 2: The Scenarios

Choose one of the following scenarios to write an ADR for.

### Scenario A: The Frontend Framework Shift
**Context:** Your team has maintained a large, complex Vue 2 application for five years. Vue 2 has hit end-of-life. The team is torn between migrating to Vue 3 (which requires rewriting all components to the Composition API) or throwing it out and rewriting the app in React (Next.js) because it's easier to hire React developers in your market.
**Task:** Write an ADR choosing React. What are the severe negative consequences of this choice?

### Scenario B: Database for Analytics
**Context:** Your primary Postgres database is straining under the load of the data analytics team running heavy `GROUP BY` queries during business hours. You need to offload analytics.
**Task:** Write an ADR deciding to use a read-replica vs. implementing a dedicated Data Warehouse (like Snowflake or BigQuery). Choose one, justify it, detail the trade-offs.

## Part 3: Peer Review
Swap your ADR with a peer.
1. As the reviewer, try to find a "hidden cost" (a negative consequence) that the author missed.
2. Add it to the Consequences section.
