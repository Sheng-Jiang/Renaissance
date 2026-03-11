# Exercise: ClawSwarm Multi-Agent Configuration
**Time: 75 Minutes**

## Overview
While the team polishes the hackathon codebase, take time individually to build a local multi-agent system using ClawSwarm. You will configure two specialized agents to communicate with each other to complete a small task.

## Phase 1: Configuration (30 mins)
1.  **Install:** Ensure ClawSwarm is running locally (via the provided Docker Compose file).
2.  **Define Agent 1 (The Researcher):**
    *   System Prompt: "You are an expert technical researcher. Your job is to read user prompts, search the provided documentation files, and output a structured JSON summary of the findings."
    *   Model: `gemini-1.5-flash` or `claude-3-haiku` (Fast, cheap, good for extraction).
3.  **Define Agent 2 (The Engineer):**
    *   System Prompt: "You are an expert software engineer. You receive JSON summaries from the Researcher. You write a complete, working Python script based *only* on the requirements in that JSON."
    *   Model: `claude-3-opus` or `gemini-1.5-pro` (Strong reasoning, excellent coding).

## Phase 2: Execution & Orchestration (20 mins)
1.  Set up the routing so Agent 1's standard output pipes directly into Agent 2's context window.
2.  **The Task:** Give Agent 1 the prompt: "Find the specifications for the data ingestion pipeline and tell the engineer to build it."
3.  Watch the swarm execute.

## Phase 3: Documentation & Comparison (25 mins)
Write a brief entry in your design journal comparing this multi-agent approach to a standard single-agent approach (like Antigravity Manager View). 

*   When would you recommend a ClawSwarm setup for a real development team?
*   What is the friction cost of setting up the integration?
