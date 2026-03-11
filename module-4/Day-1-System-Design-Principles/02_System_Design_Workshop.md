# Lab: System Design Workshop

**Objective:** Progressively design architectures for applications of increasing scale. Identify trade-offs, bottlenecks, and single points of failure.

*Note: Use a whiteboarding tool (Excalidraw, Miro, or a physical whiteboard) to draw these systems.*

## Scenario 1: The Internal Tool
**The Prompt:** Design an internal dashboard for HR to track employee vacation days. It has 50 users. It needs to be built by tomorrow.

**Constraints:**
- Speed of development is the #1 priority.
- High availability is not critical (if it goes down for 5 minutes, no one dies).

**Task:**
Draw the simplest possible architecture that satisfies this. (Hint: Think Monolith, SQLite or single DB instance, PaaS deployment).

## Scenario 2: The Viral E-Commerce Store
**The Prompt:** You run a boutique sneaker store online. Usually, you get 1,000 visitors a day. Tomorrow, you are dropping a new shoe collaboration with a celebrity. You expect 500,000 visitors in a 10-minute window.

**Constraints:**
- The site must not crash during the traffic spike.
- Inventory must be strictly consistent (we cannot sell shoe #100 to two different people).

**Task:**
Draw the architecture.
- *Where do you place the Load Balancer?*
- *How do you cache the product catalog page so the DB doesn't melt?*
- *How do you handle the checkout queue? (Hint: Message Queue).*

## Scenario 3: The Global Video Platform
**The Prompt:** Design a system like YouTube or Netflix. Users upload videos, the system transcodes them into different resolutions, and viewers stream them globally with low latency.

**Constraints:**
- Massive storage requirements.
- Async processing required for transcoding.
- Global latency must be minimal.

**Task:**
Draw the architecture.
- *Where is the video stored? (Object Storage like S3).*
- *How is it served fast in Tokyo vs. New York? (CDN).*
- *How does the web server tell the worker nodes to transcode a video? (Event Bus).*

## Peer Critique
Present your architecture for Scenario 2 or 3 to a peer. Have them find the **Single Point of Failure (SPOF)** in your diagram.
